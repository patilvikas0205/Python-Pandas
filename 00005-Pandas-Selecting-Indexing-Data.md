# Pandas selecting and indexing data
#pandas support three type of multiaxes indexing

 <h4>.loc[] ==> Label Based</h4>
 <h4>.iloc ==> integer based</h4>
 <h4>.xloc[] ==>both label and integer based</h4>


```python
data=[["A",40,50,60,30],["B",85,45,79,12],["C",42,15,60,24],
      ["D",25,78,45,62],["E",45,85,24,56],["F",52,48,56,74],
      ["G",56,87,45,58],["H",56,48,89,52],["I",58,45,66,55],
      ["J",56,87,25,45]]
```


```python
data
```




    [['A', 40, 50, 60, 30],
     ['B', 85, 45, 79, 12],
     ['C', 42, 15, 60, 24],
     ['D', 25, 78, 45, 62],
     ['E', 45, 85, 24, 56],
     ['F', 52, 48, 56, 74],
     ['G', 56, 87, 45, 58],
     ['H', 56, 48, 89, 52],
     ['I', 58, 45, 66, 55],
     ['J', 56, 87, 25, 45]]




```python
import pandas as pd
```


```python
df1=pd.DataFrame(data=data,columns=["Name","Maths","Physics","Chemistry","English"])
```


```python
df1
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
      <th>Name</th>
      <th>Maths</th>
      <th>Physics</th>
      <th>Chemistry</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>A</td>
      <td>40</td>
      <td>50</td>
      <td>60</td>
      <td>30</td>
    </tr>
    <tr>
      <td>1</td>
      <td>B</td>
      <td>85</td>
      <td>45</td>
      <td>79</td>
      <td>12</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
      <td>42</td>
      <td>15</td>
      <td>60</td>
      <td>24</td>
    </tr>
    <tr>
      <td>3</td>
      <td>D</td>
      <td>25</td>
      <td>78</td>
      <td>45</td>
      <td>62</td>
    </tr>
    <tr>
      <td>4</td>
      <td>E</td>
      <td>45</td>
      <td>85</td>
      <td>24</td>
      <td>56</td>
    </tr>
    <tr>
      <td>5</td>
      <td>F</td>
      <td>52</td>
      <td>48</td>
      <td>56</td>
      <td>74</td>
    </tr>
    <tr>
      <td>6</td>
      <td>G</td>
      <td>56</td>
      <td>87</td>
      <td>45</td>
      <td>58</td>
    </tr>
    <tr>
      <td>7</td>
      <td>H</td>
      <td>56</td>
      <td>48</td>
      <td>89</td>
      <td>52</td>
    </tr>
    <tr>
      <td>8</td>
      <td>I</td>
      <td>58</td>
      <td>45</td>
      <td>66</td>
      <td>55</td>
    </tr>
    <tr>
      <td>9</td>
      <td>J</td>
      <td>56</td>
      <td>87</td>
      <td>25</td>
      <td>45</td>
    </tr>
  </tbody>
</table>
</div>




```python
#using .loc[]
# access all rows and all column
df1.iloc[:]
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
      <th>Name</th>
      <th>Maths</th>
      <th>Physics</th>
      <th>Chemistry</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>A</td>
      <td>40</td>
      <td>50</td>
      <td>60</td>
      <td>30</td>
    </tr>
    <tr>
      <td>1</td>
      <td>B</td>
      <td>85</td>
      <td>45</td>
      <td>79</td>
      <td>12</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
      <td>42</td>
      <td>15</td>
      <td>60</td>
      <td>24</td>
    </tr>
    <tr>
      <td>3</td>
      <td>D</td>
      <td>25</td>
      <td>78</td>
      <td>45</td>
      <td>62</td>
    </tr>
    <tr>
      <td>4</td>
      <td>E</td>
      <td>45</td>
      <td>85</td>
      <td>24</td>
      <td>56</td>
    </tr>
    <tr>
      <td>5</td>
      <td>F</td>
      <td>52</td>
      <td>48</td>
      <td>56</td>
      <td>74</td>
    </tr>
    <tr>
      <td>6</td>
      <td>G</td>
      <td>56</td>
      <td>87</td>
      <td>45</td>
      <td>58</td>
    </tr>
    <tr>
      <td>7</td>
      <td>H</td>
      <td>56</td>
      <td>48</td>
      <td>89</td>
      <td>52</td>
    </tr>
    <tr>
      <td>8</td>
      <td>I</td>
      <td>58</td>
      <td>45</td>
      <td>66</td>
      <td>55</td>
    </tr>
    <tr>
      <td>9</td>
      <td>J</td>
      <td>56</td>
      <td>87</td>
      <td>25</td>
      <td>45</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Only Column no 2
df1.iloc[:,2]
```




    0    50
    1    45
    2    15
    3    78
    4    85
    5    48
    6    87
    7    48
    8    45
    9    87
    Name: Physics, dtype: int64




```python
#row 5,6,7 all column
df1.iloc[5:8,:]
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
      <th>Name</th>
      <th>Maths</th>
      <th>Physics</th>
      <th>Chemistry</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>5</td>
      <td>F</td>
      <td>52</td>
      <td>48</td>
      <td>56</td>
      <td>74</td>
    </tr>
    <tr>
      <td>6</td>
      <td>G</td>
      <td>56</td>
      <td>87</td>
      <td>45</td>
      <td>58</td>
    </tr>
    <tr>
      <td>7</td>
      <td>H</td>
      <td>56</td>
      <td>48</td>
      <td>89</td>
      <td>52</td>
    </tr>
  </tbody>
</table>
</div>




```python
#row 5,6,7 all column Maths and English
df1.iloc[5:8,1::3] #==> [row,column]==>[start(incl):end(excl):step , start(incl):end(excl):step]
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
      <th>Maths</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>5</td>
      <td>52</td>
      <td>74</td>
    </tr>
    <tr>
      <td>6</td>
      <td>56</td>
      <td>58</td>
    </tr>
    <tr>
      <td>7</td>
      <td>56</td>
      <td>52</td>
    </tr>
  </tbody>
</table>
</div>




```python
# alternate row all column Maths and English
df1.iloc[0::2,0::2] #==> [row,column]==>[start(incl):end(excl):step , start(incl):end(excl):step]
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
      <th>Name</th>
      <th>Physics</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>0</td>
      <td>A</td>
      <td>50</td>
      <td>30</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
      <td>15</td>
      <td>24</td>
    </tr>
    <tr>
      <td>4</td>
      <td>E</td>
      <td>85</td>
      <td>56</td>
    </tr>
    <tr>
      <td>6</td>
      <td>G</td>
      <td>87</td>
      <td>58</td>
    </tr>
    <tr>
      <td>8</td>
      <td>I</td>
      <td>45</td>
      <td>55</td>
    </tr>
  </tbody>
</table>
</div>




```python
#using loc[] #Access a group of rows and columns by label(s) or a boolean array
'''
Allowed inputs are:

- A single label, e.g. ``5`` or ``'a'``, (note that ``5`` is
  interpreted as a *label* of the index, and **never** as an
  integer position along the index).
- A list or array of labels, e.g. ``['a', 'b', 'c']``.
- A slice object with labels, e.g. ``'a':'f'``
'''    
df1.loc[1:2]
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
      <th>Name</th>
      <th>Maths</th>
      <th>Physics</th>
      <th>Chemistry</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>B</td>
      <td>85</td>
      <td>45</td>
      <td>79</td>
      <td>12</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
      <td>42</td>
      <td>15</td>
      <td>60</td>
      <td>24</td>
    </tr>
  </tbody>
</table>
</div>




```python
df1.ix[1:]
```

    C:\ProgramData\Anaconda3\lib\site-packages\ipykernel_launcher.py:1: FutureWarning: 
    .ix is deprecated. Please use
    .loc for label based indexing or
    .iloc for positional indexing
    
    See the documentation here:
    http://pandas.pydata.org/pandas-docs/stable/user_guide/indexing.html#ix-indexer-is-deprecated
      """Entry point for launching an IPython kernel.
    




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
      <th>Name</th>
      <th>Maths</th>
      <th>Physics</th>
      <th>Chemistry</th>
      <th>English</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>1</td>
      <td>B</td>
      <td>85</td>
      <td>45</td>
      <td>79</td>
      <td>12</td>
    </tr>
    <tr>
      <td>2</td>
      <td>C</td>
      <td>42</td>
      <td>15</td>
      <td>60</td>
      <td>24</td>
    </tr>
    <tr>
      <td>3</td>
      <td>D</td>
      <td>25</td>
      <td>78</td>
      <td>45</td>
      <td>62</td>
    </tr>
    <tr>
      <td>4</td>
      <td>E</td>
      <td>45</td>
      <td>85</td>
      <td>24</td>
      <td>56</td>
    </tr>
    <tr>
      <td>5</td>
      <td>F</td>
      <td>52</td>
      <td>48</td>
      <td>56</td>
      <td>74</td>
    </tr>
    <tr>
      <td>6</td>
      <td>G</td>
      <td>56</td>
      <td>87</td>
      <td>45</td>
      <td>58</td>
    </tr>
    <tr>
      <td>7</td>
      <td>H</td>
      <td>56</td>
      <td>48</td>
      <td>89</td>
      <td>52</td>
    </tr>
    <tr>
      <td>8</td>
      <td>I</td>
      <td>58</td>
      <td>45</td>
      <td>66</td>
      <td>55</td>
    </tr>
    <tr>
      <td>9</td>
      <td>J</td>
      <td>56</td>
      <td>87</td>
      <td>25</td>
      <td>45</td>
    </tr>
  </tbody>
</table>
</div>


