# sentianalyse
--------------

A simple python library that generates sentiment type(positive,negetive,neutral)
pie chart, percentage,number and ternary value for pandas dataframe text portion.

The code is Python 2 and 3 compatible.

# Installation
--------------

Fast install:
-------------

```
        pip install sentianalyse
```

For a manual install get this package:
--------------------------------------

```bash

        $wget https://github.com/garain/sentianalyse/archive/master.zip
        $unzip master.zip
        $rm master.zip
        $cd sentianalyse-master
```

Install the package:
--------------------

```

        python setup.py install    
```

# The library is pandas dataframe dependent.
--------------------------------------------

Have to get dataframe('text columns') and give to command.
Like df['text']


# Example
---------

```python

        import sentianalyse as sa
		# Features
		
        # - sentiment type pie chart :
        sa.pie()

        
        # sentiment type amount : 
        # - Get the sentiment type(postive,negetive,neutral numbers)
        sa.number()
               
        
        # sentiment percentage :
        # - Get the percentage of sentiment type
        sa.percentage() 
                
        
        # sa.ternary_analysis
        # - Get the type of all text, here -1:negetive, 0:neutral, 1:positive
        sa.ternary_analysis()
        
                    
        import pandas as pd
        
        df=pd.read_csv("/home/samin/anaconda3/dataset_2.csv")
        
        percent=at.percentage(df['text'])
        
        print(percent)
        
        
        number = sa.number(df['text'])
        
        print(number)
        
        
        analysis = sa.analysis_ternary(df['text'])
        
        print(analysis)
        
        
        #sa.pie(df['text'])
		
        # Pass list of texts as input
		
		df=pd.DataFrame(["I love you very much."],columns=['text'])
```

Here is the output:
-------------------

```

    Positve : 33.31 %, Negetive 20.96 %, Neutral : 45.72 %
    {'positive  ': 1087, 'negetive': 684, 'neutral': 1492}
	[-1, 1, 0.0, 0.0, 0.0, 0.0,.......,1]
```