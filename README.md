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
