## Welcome to my Demo:

### Here is what happens when I import the Jupyter notebook:


```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import scipy.stats
```


```python
# Reading in the data
df = pd.read_csv('happy2019.csv')
# Subselecting the happiest and saddest countries
happy = df.head(5)
sad = df.tail(5)
all = happy.append(sad, ignore_index=True)
all
```




<div>
<style scoped>
    .dataframe tbody tr th:only-of-type {
        vertical-align: middle;
    }

    .dataframe tbody tr th {
        vertical-align: top;
    }

    .dataframe thead th {
        text-align: right;
    }
</style>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Overall rank</th>
      <th>Country or region</th>
      <th>Score</th>
      <th>GDP per capita</th>
      <th>Social support</th>
      <th>Healthy life expectancy</th>
      <th>Freedom to make life choices</th>
      <th>Generosity</th>
      <th>Perceptions of corruption</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1</td>
      <td>Finland</td>
      <td>7.769</td>
      <td>1.340</td>
      <td>1.587</td>
      <td>0.986</td>
      <td>0.596</td>
      <td>0.153</td>
      <td>0.393</td>
    </tr>
    <tr>
      <th>1</th>
      <td>2</td>
      <td>Denmark</td>
      <td>7.600</td>
      <td>1.383</td>
      <td>1.573</td>
      <td>0.996</td>
      <td>0.592</td>
      <td>0.252</td>
      <td>0.410</td>
    </tr>
    <tr>
      <th>2</th>
      <td>3</td>
      <td>Norway</td>
      <td>7.554</td>
      <td>1.488</td>
      <td>1.582</td>
      <td>1.028</td>
      <td>0.603</td>
      <td>0.271</td>
      <td>0.341</td>
    </tr>
    <tr>
      <th>3</th>
      <td>4</td>
      <td>Iceland</td>
      <td>7.494</td>
      <td>1.380</td>
      <td>1.624</td>
      <td>1.026</td>
      <td>0.591</td>
      <td>0.354</td>
      <td>0.118</td>
    </tr>
    <tr>
      <th>4</th>
      <td>5</td>
      <td>Netherlands</td>
      <td>7.488</td>
      <td>1.396</td>
      <td>1.522</td>
      <td>0.999</td>
      <td>0.557</td>
      <td>0.322</td>
      <td>0.298</td>
    </tr>
    <tr>
      <th>5</th>
      <td>152</td>
      <td>Rwanda</td>
      <td>3.334</td>
      <td>0.359</td>
      <td>0.711</td>
      <td>0.614</td>
      <td>0.555</td>
      <td>0.217</td>
      <td>0.411</td>
    </tr>
    <tr>
      <th>6</th>
      <td>153</td>
      <td>Tanzania</td>
      <td>3.231</td>
      <td>0.476</td>
      <td>0.885</td>
      <td>0.499</td>
      <td>0.417</td>
      <td>0.276</td>
      <td>0.147</td>
    </tr>
    <tr>
      <th>7</th>
      <td>154</td>
      <td>Afghanistan</td>
      <td>3.203</td>
      <td>0.350</td>
      <td>0.517</td>
      <td>0.361</td>
      <td>0.000</td>
      <td>0.158</td>
      <td>0.025</td>
    </tr>
    <tr>
      <th>8</th>
      <td>155</td>
      <td>Central African Republic</td>
      <td>3.083</td>
      <td>0.026</td>
      <td>0.000</td>
      <td>0.105</td>
      <td>0.225</td>
      <td>0.235</td>
      <td>0.035</td>
    </tr>
    <tr>
      <th>9</th>
      <td>156</td>
      <td>South Sudan</td>
      <td>2.853</td>
      <td>0.306</td>
      <td>0.575</td>
      <td>0.295</td>
      <td>0.010</td>
      <td>0.202</td>
      <td>0.091</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Barplot
barplot = sns.catplot(kind='bar', data= all, y='Score', x = 'Country or region')
```




    
![png](Demo_files/Demo_2_0.png)
    




```python
# Barplot
barplot = sns.catplot(kind='bar', data= all, y='Score', x = 'Country or region')
# Modifying X-Labels to avoid overlapping country names
plt.xticks(
    rotation=45, #degrees
    horizontalalignment='right',
    fontweight='bold', # or 'light'
    fontsize='small'  # or large
)
plt.title('Happiness Scores')
plt.show()
```




    
![png](Demo_files/Demo_3_0.png)
    





### Here is what happens when I import a photo of the barplot

<img width="250" alt="demobarplot" src="https://user-images.githubusercontent.com/73716282/97893309-7f246400-1d07-11eb-8c31-f4768352fec5.png">


### Here, I change the size of the image:

<img width="550" alt="demobarplot" src="https://user-images.githubusercontent.com/73716282/97893309-7f246400-1d07-11eb-8c31-f4768352fec5.png">


[Questions?](mailto:al962601@dal.ca)
