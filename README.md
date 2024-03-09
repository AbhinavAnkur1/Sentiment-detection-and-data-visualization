# Sentiment-detection-and-data-visualization

## We Import the book for basic analysis
```
import os
for root, dirs, files in os.walk("/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text"):
    for file in files:
        if file.endswith(".txt"):
             print(os.path.join(root, file))
```
>/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text/Book2.txt  
>/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text/Book3.txt  
>/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text/Book1.txt  
>/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text/Book4.txt

## Distribute the dataset into paragraph  
```
import os
hp_paragraphs = []
for root, dirs, files in os.walk("/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text"):
    for file in files:
        if file.endswith(".txt"):
            print(os.path.join(root, file))
            with open(os.path.join(root, file), "r", encoding="utf8", errors='ignore') as input:
                paragraphs = input.read().split("\n\n")   #\n\n denotes there is a blank line in between paragraphs.
            #print(paragraphs[0])
            hp_paragraphs.extend(paragraphs)
            
print(len(hp_paragraphs))
```

## Seperate the paragraph into sentences  
```
import os
hp_sentences = []
for root, dirs, files in os.walk("/Users/animeshgiri/Desktop/Animesh/INFO 6105/finalproject/sample_text"):
    for file in files:
        if file.endswith(".txt"):
            print(os.path.join(root, file))
            with open(os.path.join(root, file), "r", encoding="utf8", errors='ignore') as input:
                sentences = input.read().split(". ")   #. denotes end of sentence
            hp_sentences.extend(sentences)
            
print(len(hp_sentences))
```

## Converting the data into DataFrame using pandas
```
import pandas as pd
hp_df = pd.DataFrame(hp_sentences, columns = ['Sentence'])
hp_df.head()
```  


