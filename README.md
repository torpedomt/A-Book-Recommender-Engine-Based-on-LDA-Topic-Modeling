# A-Book-Recommender-Engine-Based-on-LDA-Topic-Modeling
ANLY580
Asian-Fusion-66


## Project Report
Our project report is in _Project Report.ipynb_.

## Data
We used book name data from _Book.csv_. And the wikipedia content text for each book can be extracted by using wikipedia API to query the book name. Below is the example code for *python*.

```
import wikipedia
import pandas as pd
book = pd.read_csv('/Users/zmt/Desktop/Book_Recommender/Book.csv')
books = book['name']
for i in range(len(books)):
    try:
        page = wikipedia.page(books[i][0])
        text.append(page.content)
        ind.append(i)
    except:
        pass
```
