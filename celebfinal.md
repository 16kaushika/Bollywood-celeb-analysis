## importing libraries and dataset


```python
#import data set
import pandas as pd
dataframe = pd.read_csv(r'C:\Users\Lenovo\Desktop\bollywood-celebs.csv')
dataframe
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Arjun Rampal</td>
      <td>Male</td>
      <td>26/11/1972</td>
      <td>Jabalpur</td>
      <td>48</td>
      <td>1.81</td>
      <td>Yes</td>
      <td>Mehr Jesia</td>
      <td>2001</td>
      <td>46</td>
      <td>15.0</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Bobby Deol</td>
      <td>Male</td>
      <td>27/1/1969</td>
      <td>Mumbai</td>
      <td>52</td>
      <td>1.80</td>
      <td>Yes</td>
      <td>Tanya Deol</td>
      <td>1977</td>
      <td>46</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>97</th>
      <td>R.Madhavan</td>
      <td>Male</td>
      <td>1/6/1970</td>
      <td>Jamshedpur</td>
      <td>51</td>
      <td>1.77</td>
      <td>Yes</td>
      <td>Sarita Birje</td>
      <td>1993</td>
      <td>52</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Mahesh Manjrekar</td>
      <td>Male</td>
      <td>16/8/1958</td>
      <td>Mumbai</td>
      <td>62</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Medha Manjrekar</td>
      <td>1975</td>
      <td>80</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Rani Mukerji</td>
      <td>Female</td>
      <td>21/3/1978</td>
      <td>Calcutta</td>
      <td>43</td>
      <td>1.56</td>
      <td>Yes</td>
      <td>Aditya Chopra</td>
      <td>1996</td>
      <td>55</td>
      <td>12.0</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 11 columns</p>
</div>



### getting basic information about data


```python
dataframe.head()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataframe.tail()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>95</th>
      <td>Arjun Rampal</td>
      <td>Male</td>
      <td>26/11/1972</td>
      <td>Jabalpur</td>
      <td>48</td>
      <td>1.81</td>
      <td>Yes</td>
      <td>Mehr Jesia</td>
      <td>2001</td>
      <td>46</td>
      <td>15.0</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Bobby Deol</td>
      <td>Male</td>
      <td>27/1/1969</td>
      <td>Mumbai</td>
      <td>52</td>
      <td>1.80</td>
      <td>Yes</td>
      <td>Tanya Deol</td>
      <td>1977</td>
      <td>46</td>
      <td>8.0</td>
    </tr>
    <tr>
      <th>97</th>
      <td>R.Madhavan</td>
      <td>Male</td>
      <td>1/6/1970</td>
      <td>Jamshedpur</td>
      <td>51</td>
      <td>1.77</td>
      <td>Yes</td>
      <td>Sarita Birje</td>
      <td>1993</td>
      <td>52</td>
      <td>14.0</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Mahesh Manjrekar</td>
      <td>Male</td>
      <td>16/8/1958</td>
      <td>Mumbai</td>
      <td>62</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Medha Manjrekar</td>
      <td>1975</td>
      <td>80</td>
      <td>5.0</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Rani Mukerji</td>
      <td>Female</td>
      <td>21/3/1978</td>
      <td>Calcutta</td>
      <td>43</td>
      <td>1.56</td>
      <td>Yes</td>
      <td>Aditya Chopra</td>
      <td>1996</td>
      <td>55</td>
      <td>12.0</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataframe.shape
```




    (100, 11)




```python
dataframe.size
```




    1100




```python
dataframe.columns
```




    Index(['Name', 'gender', 'born_date', 'born_city', 'Age', 'height_in_m',
           'married', 'Spouse_or_Ex.partner', 'Debut_year', 'total_films_aprox',
           'USD_NetWorth_Million'],
          dtype='object')




```python
dataframe.dtypes
```




    Name                     object
    gender                   object
    born_date                object
    born_city                object
    Age                       int64
    height_in_m             float64
    married                  object
    Spouse_or_Ex.partner     object
    Debut_year                int64
    total_films_aprox         int64
    USD_NetWorth_Million    float64
    dtype: object




```python
dataframe.info()
```

    <class 'pandas.core.frame.DataFrame'>
    RangeIndex: 100 entries, 0 to 99
    Data columns (total 11 columns):
     #   Column                Non-Null Count  Dtype  
    ---  ------                --------------  -----  
     0   Name                  100 non-null    object 
     1   gender                100 non-null    object 
     2   born_date             100 non-null    object 
     3   born_city             100 non-null    object 
     4   Age                   100 non-null    int64  
     5   height_in_m           100 non-null    float64
     6   married               100 non-null    object 
     7   Spouse_or_Ex.partner  71 non-null     object 
     8   Debut_year            100 non-null    int64  
     9   total_films_aprox     100 non-null    int64  
     10  USD_NetWorth_Million  100 non-null    float64
    dtypes: float64(2), int64(3), object(6)
    memory usage: 8.7+ KB
    

### task 1 find any duplicate record in database


```python
dataframe[dataframe.duplicated()]
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
  </tbody>
</table>
</div>



### check for null values


```python
dataframe.isnull()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>1</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>2</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>3</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>True</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>4</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>95</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>96</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>97</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>98</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
    <tr>
      <th>99</th>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
      <td>False</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 11 columns</p>
</div>




```python
dataframe.isnull().sum()
```




    Name                     0
    gender                   0
    born_date                0
    born_city                0
    Age                      0
    height_in_m              0
    married                  0
    Spouse_or_Ex.partner    29
    Debut_year               0
    total_films_aprox        0
    USD_NetWorth_Million     0
    dtype: int64



#### show missing values with heat-map


```python
import seaborn as sns
sns.heatmap(dataframe.isnull())
```




    <AxesSubplot:>




    
![png](output_16_1.png)
    


### Q.1 For "Madhuri Dixit" ,show gender and year of debut .


```python
#showing gender and year of debut,we solve this question by isin()method
#we can also use str.contains() method
dataframe[dataframe['Name'].isin(['Madhuri Dixit'])]
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>16</th>
      <td>Madhuri Dixit</td>
      <td>Female</td>
      <td>15/5/1967</td>
      <td>Mumbai</td>
      <td>54</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Shriram Madhav Nene</td>
      <td>1984</td>
      <td>70</td>
      <td>35.0</td>
    </tr>
  </tbody>
</table>
</div>



###  Q.2 In which year highest number of celebrities born ?

#### Q2.1 In which year highest number of celebrities Debut?


```python
dataframe.dtypes
```




    Name                     object
    gender                   object
    born_date                object
    born_city                object
    Age                       int64
    height_in_m             float64
    married                  object
    Spouse_or_Ex.partner     object
    Debut_year                int64
    total_films_aprox         int64
    USD_NetWorth_Million    float64
    dtype: object




```python
#Q.2 answer: we are creating new coulmn for date time
dataframe['New_Date'] = pd.to_datetime(dataframe['born_date'])
dataframe.head()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
      <td>1967-09-09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
      <td>1965-02-11</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
      <td>1986-05-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>1965-12-27</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
      <td>1965-03-14</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataframe.dtypes
```


```python
dataframe['New_Date'].dt.year.value_counts()
```




    1985    7
    1987    6
    1990    5
    1974    5
    1956    4
    1976    4
    1988    4
    1967    3
    1965    3
    1970    3
    1973    3
    1969    3
    1975    3
    1983    2
    1984    2
    1978    2
    1979    2
    1980    2
    1972    2
    1986    2
    1982    2
    1959    2
    1957    2
    1955    2
    1989    2
    1992    2
    1950    2
    1942    2
    1981    2
    1995    1
    1997    1
    1922    1
    1935    1
    1971    1
    1968    1
    1963    1
    1961    1
    1958    1
    1954    1
    1952    1
    1951    1
    1948    1
    1945    1
    1998    1
    Name: New_Date, dtype: int64



<b> from the output we can see that in year 1985 highest number of celebrities born .number of celebs are 7</b>


```python
#Q2.1 answer: 
dataframe.value_counts('Debut_year')
```




    Debut_year
    2012    6
    1991    5
    2010    5
    1999    4
    1982    4
    2000    4
    2009    4
    1996    4
    2001    4
    2011    3
    1988    3
    2007    3
    2014    3
    1997    3
    2005    3
    2002    2
    2003    2
    1992    2
    1993    2
    2004    2
    1983    2
    1978    2
    1977    2
    1969    2
    2015    2
    2018    2
    2006    2
    2008    1
    1944    1
    1998    1
    1995    1
    1958    1
    1986    1
    1984    1
    1980    1
    1979    1
    1976    1
    1975    1
    1974    1
    1973    1
    1972    1
    1968    1
    1964    1
    1960    1
    2019    1
    dtype: int64



<b> as shown in output, highest number of celebrities debut in 2012</b>

### Q.3 how many marital status are there in dataset ?show with the bar graph.


```python
dataframe.groupby('married').married.count()
```




    married
    Divorced     9
    No          29
    Yes         62
    Name: married, dtype: int64



#### output shows the Yes if married and No for not married and Divorced ,there are 62 celebrities who married in current date.

### Bar Graph


```python
import seaborn as sns
from matplotlib import pyplot as plt
```


```python
sns.countplot(dataframe['married'])
```

    C:\Users\Lenovo\anaconda3\lib\site-packages\seaborn\_decorators.py:36: FutureWarning: Pass the following variable as a keyword arg: x. From version 0.12, the only valid positional argument will be `data`, and passing other arguments without an explicit keyword will result in an error or misinterpretation.
      warnings.warn(
    




    <AxesSubplot:xlabel='married', ylabel='count'>




    
![png](output_33_2.png)
    


### Q.4 Show data of the celebrities who born in Mumbai and have networth above 30 million.

#### Q.4.1 Show only the Female celebrities name who has given more than 40 number of films.

#### Q.4.2 Show name of the celebrities who divorced and also show with whom they divorced

##### Filtering


```python
dataframe.head()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
      <td>1967-09-09</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
      <td>1965-02-11</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
      <td>1986-05-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>1965-12-27</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
      <td>1965-03-14</td>
    </tr>
  </tbody>
</table>
</div>




```python
#Q.4 answer:
#we will use filtering for this
dataframe[(dataframe['born_city']=='Mumbai') & (dataframe['USD_NetWorth_Million']>30.0)]
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
      <td>1965-03-14</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Hritik Roshan</td>
      <td>Male</td>
      <td>10/1/1974</td>
      <td>Mumbai</td>
      <td>47</td>
      <td>1.80</td>
      <td>Divorced</td>
      <td>Sussanne Khan</td>
      <td>1980</td>
      <td>37</td>
      <td>370.0</td>
      <td>1974-10-01</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Madhuri Dixit</td>
      <td>Female</td>
      <td>15/5/1967</td>
      <td>Mumbai</td>
      <td>54</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Shriram Madhav Nene</td>
      <td>1984</td>
      <td>70</td>
      <td>35.0</td>
      <td>1967-05-15</td>
    </tr>
    <tr>
      <th>23</th>
      <td>Ranbir Kapoor</td>
      <td>Male</td>
      <td>28/9/1982</td>
      <td>Mumbai</td>
      <td>38</td>
      <td>1.81</td>
      <td>No</td>
      <td>NaN</td>
      <td>2007</td>
      <td>27</td>
      <td>45.0</td>
      <td>1982-09-28</td>
    </tr>
    <tr>
      <th>39</th>
      <td>John Abraham</td>
      <td>Male</td>
      <td>17/12/1972</td>
      <td>Mumbai</td>
      <td>48</td>
      <td>1.85</td>
      <td>Yes</td>
      <td>Priya Runchal</td>
      <td>1999</td>
      <td>63</td>
      <td>34.0</td>
      <td>1972-12-17</td>
    </tr>
    <tr>
      <th>75</th>
      <td>Arshad Warsi</td>
      <td>Male</td>
      <td>19/4/1968</td>
      <td>Mumbai</td>
      <td>53</td>
      <td>1.68</td>
      <td>Yes</td>
      <td>Maria Goretti</td>
      <td>1996</td>
      <td>62</td>
      <td>40.0</td>
      <td>1968-04-19</td>
    </tr>
  </tbody>
</table>
</div>



#### filtering


```python
#Q.4.1 answer using filtering
dataframe[(dataframe['gender']=='Female') & (dataframe['total_films_aprox']>40)]['Name']
```




    5            Priyanka Chopra
    8               Katrina Kaif
    14           Kareena Kapoor 
    16             Madhuri Dixit
    18    Aishwarya Rai Bachchan
    26            Karisma Kapoor
    30             Shruti Haasan
    46             Shilpa Shetty
    56                   Kajol  
    57            Kajal Aggarwal
    71                     Rekha
    87               Hema Malini
    90                 Tamannaah
    99              Rani Mukerji
    Name: Name, dtype: object




```python
#Q.4.2 answer
dataframe[dataframe['married']=='Divorced']
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>6</th>
      <td>Hritik Roshan</td>
      <td>Male</td>
      <td>10/1/1974</td>
      <td>Mumbai</td>
      <td>47</td>
      <td>1.80</td>
      <td>Divorced</td>
      <td>Sussanne Khan</td>
      <td>1980</td>
      <td>37</td>
      <td>370.0</td>
      <td>1974-10-01</td>
    </tr>
    <tr>
      <th>13</th>
      <td>Arbazz Khan</td>
      <td>Male</td>
      <td>4/8/1967</td>
      <td>Pune</td>
      <td>53</td>
      <td>1.73</td>
      <td>Divorced</td>
      <td>Malaika Arora</td>
      <td>1996</td>
      <td>43</td>
      <td>73.0</td>
      <td>1967-04-08</td>
    </tr>
    <tr>
      <th>26</th>
      <td>Karisma Kapoor</td>
      <td>Female</td>
      <td>25/6/1974</td>
      <td>Mumbai</td>
      <td>46</td>
      <td>1.63</td>
      <td>Divorced</td>
      <td>Sunjay Kapur</td>
      <td>1991</td>
      <td>64</td>
      <td>12.0</td>
      <td>1974-06-25</td>
    </tr>
    <tr>
      <th>53</th>
      <td>Dilip Kumar</td>
      <td>Male</td>
      <td>11/12/1922</td>
      <td>Pakistan</td>
      <td>98</td>
      <td>1.78</td>
      <td>Divorced</td>
      <td>Asma Rehman,Saira Banu</td>
      <td>1944</td>
      <td>33</td>
      <td>85.0</td>
      <td>1922-11-12</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Mithun Chakraborty</td>
      <td>Male</td>
      <td>16/6/1950</td>
      <td>Bangladesh</td>
      <td>70</td>
      <td>1.83</td>
      <td>Divorced</td>
      <td>Sridevi,Yogeeta Balli</td>
      <td>1976</td>
      <td>173</td>
      <td>40.0</td>
      <td>1950-06-16</td>
    </tr>
    <tr>
      <th>65</th>
      <td>Farhan Akhtar</td>
      <td>Male</td>
      <td>9/1/1974</td>
      <td>Mumbai</td>
      <td>47</td>
      <td>1.70</td>
      <td>Divorced</td>
      <td>Adhuna Bhabani</td>
      <td>2001</td>
      <td>33</td>
      <td>2.5</td>
      <td>1974-09-01</td>
    </tr>
    <tr>
      <th>66</th>
      <td>Anupam Kher</td>
      <td>Male</td>
      <td>7/3/1955</td>
      <td>Shimla</td>
      <td>66</td>
      <td>1.68</td>
      <td>Divorced</td>
      <td>Kirron rao,Madhumalti Kapoor</td>
      <td>1982</td>
      <td>200</td>
      <td>70.0</td>
      <td>1955-07-03</td>
    </tr>
    <tr>
      <th>68</th>
      <td>Malaika Arora</td>
      <td>Female</td>
      <td>23/10/1973</td>
      <td>Thane</td>
      <td>47</td>
      <td>1.60</td>
      <td>Divorced</td>
      <td>Arbaaz Khan</td>
      <td>1997</td>
      <td>18</td>
      <td>10.0</td>
      <td>1973-10-23</td>
    </tr>
    <tr>
      <th>71</th>
      <td>Rekha</td>
      <td>Female</td>
      <td>10/10/1954</td>
      <td>Chennai</td>
      <td>66</td>
      <td>1.65</td>
      <td>Divorced</td>
      <td>Mukesh Aggarwal</td>
      <td>1958</td>
      <td>113</td>
      <td>40.0</td>
      <td>1954-10-10</td>
    </tr>
  </tbody>
</table>
</div>



### Q.5 show top 10 celebrity who gave more than 100 movies in their career


```python
dataframe.sort_values(by=['total_films_aprox'],inplace=True,ascending=False)
dataframe[(dataframe['total_films_aprox']>100)].head(10)
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>20</th>
      <td>Amitabh Bachchan</td>
      <td>Male</td>
      <td>11/10/1942</td>
      <td>Prayagraj</td>
      <td>78</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Jaya Bhaduri</td>
      <td>1969</td>
      <td>200</td>
      <td>400.0</td>
      <td>1942-11-10</td>
    </tr>
    <tr>
      <th>91</th>
      <td>Johnny Lever</td>
      <td>Male</td>
      <td>14/8/1957</td>
      <td>Kanigiri</td>
      <td>63</td>
      <td>1.60</td>
      <td>Yes</td>
      <td>Sujatha Lever</td>
      <td>1982</td>
      <td>200</td>
      <td>30.0</td>
      <td>1957-08-14</td>
    </tr>
    <tr>
      <th>66</th>
      <td>Anupam Kher</td>
      <td>Male</td>
      <td>7/3/1955</td>
      <td>Shimla</td>
      <td>66</td>
      <td>1.68</td>
      <td>Divorced</td>
      <td>Kirron rao,Madhumalti Kapoor</td>
      <td>1982</td>
      <td>200</td>
      <td>70.0</td>
      <td>1955-07-03</td>
    </tr>
    <tr>
      <th>93</th>
      <td>Shakti Kapoor</td>
      <td>Male</td>
      <td>3/9/1952</td>
      <td>Delhi</td>
      <td>68</td>
      <td>1.75</td>
      <td>Yes</td>
      <td>Shivangi Kapoor</td>
      <td>1974</td>
      <td>200</td>
      <td>30.0</td>
      <td>1952-03-09</td>
    </tr>
    <tr>
      <th>83</th>
      <td>Paresh Rawal</td>
      <td>Male</td>
      <td>30/5/1955</td>
      <td>Mumbai</td>
      <td>66</td>
      <td>1.73</td>
      <td>Yes</td>
      <td>Swaroop Sampat</td>
      <td>1982</td>
      <td>192</td>
      <td>13.0</td>
      <td>1955-05-30</td>
    </tr>
    <tr>
      <th>63</th>
      <td>Mithun Chakraborty</td>
      <td>Male</td>
      <td>16/6/1950</td>
      <td>Bangladesh</td>
      <td>70</td>
      <td>1.83</td>
      <td>Divorced</td>
      <td>Sridevi,Yogeeta Balli</td>
      <td>1976</td>
      <td>173</td>
      <td>40.0</td>
      <td>1950-06-16</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Dharmendra</td>
      <td>Male</td>
      <td>8/12/1935</td>
      <td>Nasrali</td>
      <td>85</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Hema Malini</td>
      <td>1960</td>
      <td>149</td>
      <td>60.0</td>
      <td>1935-08-12</td>
    </tr>
    <tr>
      <th>82</th>
      <td>Jackie Shroff</td>
      <td>Male</td>
      <td>1/2/1957</td>
      <td>Mumbai</td>
      <td>64</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Ayesha Shroff</td>
      <td>1978</td>
      <td>147</td>
      <td>26.0</td>
      <td>1957-01-02</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
      <td>1967-09-09</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>1965-12-27</td>
    </tr>
  </tbody>
</table>
</div>



### Q.6 Show top 5 celebrities who are not born in Mumbai and net worth is above 300million.


```python
dataframe.sort_values(by=['USD_NetWorth_Million'],inplace=True,ascending=False)
dataframe[(dataframe['born_city']!='Mumbai') & (dataframe['USD_NetWorth_Million']>300)].head(5)
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
      <td>1965-02-11</td>
    </tr>
    <tr>
      <th>74</th>
      <td>Shatrughan Sinha</td>
      <td>Male</td>
      <td>9/12/1945</td>
      <td>patna</td>
      <td>75</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Poonam Sinha</td>
      <td>1969</td>
      <td>75</td>
      <td>500.0</td>
      <td>1945-09-12</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Amitabh Bachchan</td>
      <td>Male</td>
      <td>11/10/1942</td>
      <td>Prayagraj</td>
      <td>78</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Jaya Bhaduri</td>
      <td>1969</td>
      <td>200</td>
      <td>400.0</td>
      <td>1942-11-10</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>1965-12-27</td>
    </tr>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
      <td>1967-09-09</td>
    </tr>
  </tbody>
</table>
</div>



### Q.7 Show all the records ,where "gender is Female and she is married " or "height is greater than 1.7 meter ".


```python
#here we will use filtering with And,Or operator
dataframe.head()
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
      <td>1965-02-11</td>
    </tr>
    <tr>
      <th>74</th>
      <td>Shatrughan Sinha</td>
      <td>Male</td>
      <td>9/12/1945</td>
      <td>patna</td>
      <td>75</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Poonam Sinha</td>
      <td>1969</td>
      <td>75</td>
      <td>500.0</td>
      <td>1945-09-12</td>
    </tr>
    <tr>
      <th>20</th>
      <td>Amitabh Bachchan</td>
      <td>Male</td>
      <td>11/10/1942</td>
      <td>Prayagraj</td>
      <td>78</td>
      <td>1.83</td>
      <td>Yes</td>
      <td>Jaya Bhaduri</td>
      <td>1969</td>
      <td>200</td>
      <td>400.0</td>
      <td>1942-11-10</td>
    </tr>
    <tr>
      <th>6</th>
      <td>Hritik Roshan</td>
      <td>Male</td>
      <td>10/1/1974</td>
      <td>Mumbai</td>
      <td>47</td>
      <td>1.80</td>
      <td>Divorced</td>
      <td>Sussanne Khan</td>
      <td>1980</td>
      <td>37</td>
      <td>370.0</td>
      <td>1974-10-01</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>1965-12-27</td>
    </tr>
  </tbody>
</table>
</div>




```python
dataframe[(dataframe['gender']=='Female') & (dataframe['married']=='Yes') | (dataframe['height_in_m']>=1.86)]
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>87</th>
      <td>Hema Malini</td>
      <td>Female</td>
      <td>16/10/1948</td>
      <td>Ammankundi</td>
      <td>72</td>
      <td>1.68</td>
      <td>Yes</td>
      <td>Dharmendra</td>
      <td>1968</td>
      <td>73</td>
      <td>60.0</td>
      <td>1948-10-16</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
      <td>1986-05-01</td>
    </tr>
    <tr>
      <th>16</th>
      <td>Madhuri Dixit</td>
      <td>Female</td>
      <td>15/5/1967</td>
      <td>Mumbai</td>
      <td>54</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Shriram Madhav Nene</td>
      <td>1984</td>
      <td>70</td>
      <td>35.0</td>
      <td>1967-05-15</td>
    </tr>
    <tr>
      <th>10</th>
      <td>Anushka Sharma</td>
      <td>Female</td>
      <td>1/5/1988</td>
      <td>Ayodhya</td>
      <td>33</td>
      <td>1.75</td>
      <td>Yes</td>
      <td>Virat Kohli</td>
      <td>2007</td>
      <td>21</td>
      <td>35.0</td>
      <td>1988-01-05</td>
    </tr>
    <tr>
      <th>18</th>
      <td>Aishwarya Rai Bachchan</td>
      <td>Female</td>
      <td>1/11/1973</td>
      <td>Mangalore</td>
      <td>47</td>
      <td>1.70</td>
      <td>Yes</td>
      <td>Abhishek Bachchan</td>
      <td>1991</td>
      <td>51</td>
      <td>31.0</td>
      <td>1973-01-11</td>
    </tr>
    <tr>
      <th>5</th>
      <td>Priyanka Chopra</td>
      <td>Female</td>
      <td>18/7/1982</td>
      <td>Jamshedpur</td>
      <td>38</td>
      <td>1.65</td>
      <td>Yes</td>
      <td>Nick Jones</td>
      <td>2000</td>
      <td>73</td>
      <td>30.0</td>
      <td>1982-07-18</td>
    </tr>
    <tr>
      <th>35</th>
      <td>Sushmita Sen</td>
      <td>Female</td>
      <td>19/11/1975</td>
      <td>Hyderabad</td>
      <td>45</td>
      <td>1.71</td>
      <td>Yes</td>
      <td>Rohman Shawl</td>
      <td>1996</td>
      <td>25</td>
      <td>25.0</td>
      <td>1975-11-19</td>
    </tr>
    <tr>
      <th>56</th>
      <td>Kajol</td>
      <td>Female</td>
      <td>5/8/1974</td>
      <td>Mumbai</td>
      <td>46</td>
      <td>1.60</td>
      <td>Yes</td>
      <td>Ajay Devgan</td>
      <td>1992</td>
      <td>41</td>
      <td>24.0</td>
      <td>1974-05-08</td>
    </tr>
    <tr>
      <th>27</th>
      <td>Vidya Balan</td>
      <td>Female</td>
      <td>1/1/1979</td>
      <td>Palakkad</td>
      <td>42</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Siddharth Roy Kapur</td>
      <td>1995</td>
      <td>39</td>
      <td>18.0</td>
      <td>1979-01-01</td>
    </tr>
    <tr>
      <th>46</th>
      <td>Shilpa Shetty</td>
      <td>Female</td>
      <td>8/6/1975</td>
      <td>Mangalore</td>
      <td>46</td>
      <td>1.67</td>
      <td>Yes</td>
      <td>Raj Kundra</td>
      <td>1993</td>
      <td>45</td>
      <td>18.0</td>
      <td>1975-08-06</td>
    </tr>
    <tr>
      <th>38</th>
      <td>Sonu Sood</td>
      <td>Male</td>
      <td>30/7/1973</td>
      <td>Punjab</td>
      <td>47</td>
      <td>1.88</td>
      <td>Yes</td>
      <td>Sonali Sood</td>
      <td>1999</td>
      <td>57</td>
      <td>17.0</td>
      <td>1973-07-30</td>
    </tr>
    <tr>
      <th>14</th>
      <td>Kareena Kapoor</td>
      <td>Female</td>
      <td>21/9/1980</td>
      <td>Mumbai</td>
      <td>40</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Saif Ali Khan</td>
      <td>2000</td>
      <td>72</td>
      <td>16.0</td>
      <td>1980-09-21</td>
    </tr>
    <tr>
      <th>17</th>
      <td>Sonam Kapoor</td>
      <td>Female</td>
      <td>9/6/1985</td>
      <td>Mumbai</td>
      <td>36</td>
      <td>1.75</td>
      <td>Yes</td>
      <td>Anand Ahuja</td>
      <td>2007</td>
      <td>23</td>
      <td>13.0</td>
      <td>1985-09-06</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Sunny Leone</td>
      <td>Female</td>
      <td>13/5/1981</td>
      <td>Sarnia</td>
      <td>40</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Daniel Weber</td>
      <td>2012</td>
      <td>36</td>
      <td>13.0</td>
      <td>1981-05-13</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Rani Mukerji</td>
      <td>Female</td>
      <td>21/3/1978</td>
      <td>Calcutta</td>
      <td>43</td>
      <td>1.56</td>
      <td>Yes</td>
      <td>Aditya Chopra</td>
      <td>1996</td>
      <td>55</td>
      <td>12.0</td>
      <td>1978-03-21</td>
    </tr>
    <tr>
      <th>57</th>
      <td>Kajal Aggarwal</td>
      <td>Female</td>
      <td>19/6/1985</td>
      <td>Mumbai</td>
      <td>35</td>
      <td>1.68</td>
      <td>Yes</td>
      <td>Gautam Kitchlu</td>
      <td>2004</td>
      <td>59</td>
      <td>12.0</td>
      <td>1985-06-19</td>
    </tr>
    <tr>
      <th>89</th>
      <td>Preity Zinta</td>
      <td>Female</td>
      <td>31/1/1975</td>
      <td>Shimla</td>
      <td>46</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Gene Goodenough</td>
      <td>1998</td>
      <td>38</td>
      <td>10.0</td>
      <td>1975-01-31</td>
    </tr>
    <tr>
      <th>73</th>
      <td>Yami Gautam</td>
      <td>Female</td>
      <td>28/11/1988</td>
      <td>Bilaspur</td>
      <td>32</td>
      <td>1.61</td>
      <td>Yes</td>
      <td>Aditya Dhar</td>
      <td>2008</td>
      <td>22</td>
      <td>5.0</td>
      <td>1988-11-28</td>
    </tr>
    <tr>
      <th>88</th>
      <td>Neena Gupta</td>
      <td>Female</td>
      <td>4/6/1959</td>
      <td>Delhi</td>
      <td>62</td>
      <td>1.61</td>
      <td>Yes</td>
      <td>Vivek Mehra</td>
      <td>1982</td>
      <td>38</td>
      <td>3.5</td>
      <td>1959-04-06</td>
    </tr>
  </tbody>
</table>
</div>



### Q.8 What are the different ages of celebrities


```python
#we will use nunique()  and unique()
dataframe['Age'].nunique()
```




    45




```python
dataframe['Age'].unique()
```




    array([55, 75, 78, 47, 53, 79, 56, 50, 98, 66, 85, 72, 70, 35, 38, 52, 40,
           54, 33, 48, 63, 68, 37, 34, 45, 64, 46, 42, 57, 44, 65, 31, 51, 36,
           29, 43, 59, 32, 24, 30, 62, 22, 28, 25, 61], dtype=int64)



### Q.9 Show top 5 city in which celebrities born, show in percentage with pie chart.

#### Q.9.1 Make a histogram for Age.

#### Q.9.2 show line plot for age,networth and married status.


```python
dataframe.value_counts('born_city')[0:5]
```




    born_city
    Mumbai       39
    New Delhi     7
    Delhi         3
    Punjab        3
    Chennai       2
    dtype: int64




```python
my_labels=['Mumbai','New Delhi','Delhi','Punjab','Chennai']
no_celeb=[39,7,3,3,2]
plt.pie(no_celeb,labels=my_labels,autopct='%0.1f%%')
plt.show()
```


    
![png](output_57_0.png)
    



```python
plt.hist(dataframe['Age'],color="silver")
plt.show()
```


    
![png](output_58_0.png)
    



```python
sns.lineplot(x="Age",y="USD_NetWorth_Million",data=dataframe,hue="married",style="married")
plt.show()
```


    
![png](output_59_0.png)
    


### Q.10 In last ten years how many celebs make debut show all data of them.


```python
dataframe[(dataframe['Debut_year']>=2011) & (dataframe['Debut_year']<=2021)]
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>New_Date</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>11</th>
      <td>Varun Dhavan</td>
      <td>Male</td>
      <td>24/4/1987</td>
      <td>Mumbai</td>
      <td>34</td>
      <td>1.75</td>
      <td>Yes</td>
      <td>Natasha Dalal</td>
      <td>2012</td>
      <td>27</td>
      <td>29.0</td>
      <td>1987-04-24</td>
    </tr>
    <tr>
      <th>7</th>
      <td>Tiger Shroff</td>
      <td>Male</td>
      <td>2/3/1990</td>
      <td>Mumbai</td>
      <td>31</td>
      <td>1.75</td>
      <td>No</td>
      <td>NaN</td>
      <td>2014</td>
      <td>13</td>
      <td>14.0</td>
      <td>1990-02-03</td>
    </tr>
    <tr>
      <th>55</th>
      <td>Sunny Leone</td>
      <td>Female</td>
      <td>13/5/1981</td>
      <td>Sarnia</td>
      <td>40</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Daniel Weber</td>
      <td>2012</td>
      <td>36</td>
      <td>13.0</td>
      <td>1981-05-13</td>
    </tr>
    <tr>
      <th>43</th>
      <td>Arjun Kapoor</td>
      <td>Male</td>
      <td>26/6/1985</td>
      <td>Mumbai</td>
      <td>35</td>
      <td>1.78</td>
      <td>No</td>
      <td>NaN</td>
      <td>2012</td>
      <td>24</td>
      <td>12.0</td>
      <td>1985-06-26</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Disha Patani</td>
      <td>Female</td>
      <td>13/6/1992</td>
      <td>Bareilly</td>
      <td>29</td>
      <td>1.70</td>
      <td>No</td>
      <td>NaN</td>
      <td>2015</td>
      <td>11</td>
      <td>12.0</td>
      <td>1992-06-13</td>
    </tr>
    <tr>
      <th>59</th>
      <td>Sidharth Malhotra</td>
      <td>Male</td>
      <td>16/1/1985</td>
      <td>Delhi</td>
      <td>36</td>
      <td>1.80</td>
      <td>No</td>
      <td>NaN</td>
      <td>2012</td>
      <td>14</td>
      <td>10.0</td>
      <td>1985-01-16</td>
    </tr>
    <tr>
      <th>47</th>
      <td>Parineeti Chopra</td>
      <td>Female</td>
      <td>22/10/1988</td>
      <td>Ambala</td>
      <td>32</td>
      <td>1.60</td>
      <td>No</td>
      <td>NaN</td>
      <td>2011</td>
      <td>19</td>
      <td>8.0</td>
      <td>1988-10-22</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Janhavi Kapoor</td>
      <td>Female</td>
      <td>6/3/1997</td>
      <td>Mumbai</td>
      <td>24</td>
      <td>1.63</td>
      <td>No</td>
      <td>NaN</td>
      <td>2018</td>
      <td>8</td>
      <td>8.0</td>
      <td>1997-06-03</td>
    </tr>
    <tr>
      <th>9</th>
      <td>Kartik Aaryan</td>
      <td>Male</td>
      <td>22/11/1990</td>
      <td>Gwallior</td>
      <td>30</td>
      <td>1.73</td>
      <td>No</td>
      <td>NaN</td>
      <td>2011</td>
      <td>12</td>
      <td>5.2</td>
      <td>1990-11-22</td>
    </tr>
    <tr>
      <th>42</th>
      <td>Kriti Senon</td>
      <td>Female</td>
      <td>27/7/1990</td>
      <td>New Delhi</td>
      <td>30</td>
      <td>1.71</td>
      <td>No</td>
      <td>NaN</td>
      <td>2014</td>
      <td>20</td>
      <td>4.0</td>
      <td>1990-07-27</td>
    </tr>
    <tr>
      <th>70</th>
      <td>Ananya Pandey</td>
      <td>Female</td>
      <td>30/10/1998</td>
      <td>Mumbai</td>
      <td>22</td>
      <td>1.70</td>
      <td>No</td>
      <td>NaN</td>
      <td>2019</td>
      <td>3</td>
      <td>3.2</td>
      <td>1998-10-30</td>
    </tr>
    <tr>
      <th>51</th>
      <td>Vicky Kaushal</td>
      <td>Male</td>
      <td>16/5/1988</td>
      <td>Mumbai</td>
      <td>33</td>
      <td>1.83</td>
      <td>No</td>
      <td>NaN</td>
      <td>2012</td>
      <td>16</td>
      <td>3.0</td>
      <td>1988-05-16</td>
    </tr>
    <tr>
      <th>25</th>
      <td>Kiara Advani</td>
      <td>Female</td>
      <td>31/7/1992</td>
      <td>Mumbai</td>
      <td>28</td>
      <td>1.57</td>
      <td>No</td>
      <td>NaN</td>
      <td>2014</td>
      <td>17</td>
      <td>3.0</td>
      <td>1992-07-31</td>
    </tr>
    <tr>
      <th>31</th>
      <td>Pooja Hegde</td>
      <td>Female</td>
      <td>13/10/1990</td>
      <td>Mumbai</td>
      <td>30</td>
      <td>1.68</td>
      <td>No</td>
      <td>NaN</td>
      <td>2012</td>
      <td>19</td>
      <td>2.5</td>
      <td>1990-10-13</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Sara Ali Khan</td>
      <td>Female</td>
      <td>12/8/1995</td>
      <td>Mumbai</td>
      <td>25</td>
      <td>1.63</td>
      <td>No</td>
      <td>NaN</td>
      <td>2018</td>
      <td>7</td>
      <td>2.0</td>
      <td>1995-12-08</td>
    </tr>
    <tr>
      <th>69</th>
      <td>Bhumi Pednekar</td>
      <td>Female</td>
      <td>18/7/1989</td>
      <td>Mumbai</td>
      <td>31</td>
      <td>1.57</td>
      <td>No</td>
      <td>NaN</td>
      <td>2015</td>
      <td>13</td>
      <td>1.5</td>
      <td>1989-07-18</td>
    </tr>
    <tr>
      <th>12</th>
      <td>Vidyut Jammwal</td>
      <td>Male</td>
      <td>10/12/1980</td>
      <td>Kanpur</td>
      <td>40</td>
      <td>1.80</td>
      <td>No</td>
      <td>NaN</td>
      <td>2011</td>
      <td>21</td>
      <td>1.0</td>
      <td>1980-10-12</td>
    </tr>
  </tbody>
</table>
</div>



### Q.11 Show displot for net worth.

#### Q.11.1 show box plot for Age,marital status,and gender.


```python
sns.displot(dataframe['USD_NetWorth_Million'])
plt.show()
```


    
![png](output_64_0.png)
    



```python
sns.boxplot(x='married',y='Age',data=dataframe,hue='gender')
plt.show
```




    <function matplotlib.pyplot.show(close=None, block=None)>




    
![png](output_65_1.png)
    


<b>Output shows there are avarage age of married Male celebrities is 53 and for Female 45.age between 30 to 40 ,female and male both celebrities are not married.avarage age of divorced celebrities are 60 for male and 50 for female.</b>

### Q.12 Find from how many years(from highest to lowest) stars/celebrities are active in the bollywood film industry  as an actor.


```python
dataframe['Present_year'] = pd.Series([2021 for x in range(len(dataframe.index))])
print("Final dataframe")
display(dataframe)
```

    Final dataframe
    


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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>Present_year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>Akshay Kumar</td>
      <td>Male</td>
      <td>9/9/1967</td>
      <td>Amritsar</td>
      <td>53</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Twinkle Khanna</td>
      <td>1991</td>
      <td>143</td>
      <td>350.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>1</th>
      <td>Shah Rukh Khan</td>
      <td>Male</td>
      <td>2/11/1965</td>
      <td>New Delhi</td>
      <td>55</td>
      <td>1.69</td>
      <td>Yes</td>
      <td>Gauri Khan</td>
      <td>1988</td>
      <td>107</td>
      <td>600.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>2</th>
      <td>Deepika Padukone</td>
      <td>Female</td>
      <td>5/1/1986</td>
      <td>Denmark</td>
      <td>35</td>
      <td>1.74</td>
      <td>Yes</td>
      <td>Ranveer Singh</td>
      <td>2005</td>
      <td>39</td>
      <td>48.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>3</th>
      <td>Salman Khan</td>
      <td>Male</td>
      <td>27/12/1965</td>
      <td>Indore</td>
      <td>55</td>
      <td>1.74</td>
      <td>No</td>
      <td>NaN</td>
      <td>1988</td>
      <td>124</td>
      <td>360.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>4</th>
      <td>Amir Khan</td>
      <td>Male</td>
      <td>14/3/1965</td>
      <td>Mumbai</td>
      <td>56</td>
      <td>1.63</td>
      <td>Yes</td>
      <td>Kiran rao</td>
      <td>1973</td>
      <td>62</td>
      <td>180.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>95</th>
      <td>Arjun Rampal</td>
      <td>Male</td>
      <td>26/11/1972</td>
      <td>Jabalpur</td>
      <td>48</td>
      <td>1.81</td>
      <td>Yes</td>
      <td>Mehr Jesia</td>
      <td>2001</td>
      <td>46</td>
      <td>15.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>96</th>
      <td>Bobby Deol</td>
      <td>Male</td>
      <td>27/1/1969</td>
      <td>Mumbai</td>
      <td>52</td>
      <td>1.80</td>
      <td>Yes</td>
      <td>Tanya Deol</td>
      <td>1977</td>
      <td>46</td>
      <td>8.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>97</th>
      <td>R.Madhavan</td>
      <td>Male</td>
      <td>1/6/1970</td>
      <td>Jamshedpur</td>
      <td>51</td>
      <td>1.77</td>
      <td>Yes</td>
      <td>Sarita Birje</td>
      <td>1993</td>
      <td>52</td>
      <td>14.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>98</th>
      <td>Mahesh Manjrekar</td>
      <td>Male</td>
      <td>16/8/1958</td>
      <td>Mumbai</td>
      <td>62</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Medha Manjrekar</td>
      <td>1975</td>
      <td>80</td>
      <td>5.0</td>
      <td>2021</td>
    </tr>
    <tr>
      <th>99</th>
      <td>Rani Mukerji</td>
      <td>Female</td>
      <td>21/3/1978</td>
      <td>Calcutta</td>
      <td>43</td>
      <td>1.56</td>
      <td>Yes</td>
      <td>Aditya Chopra</td>
      <td>1996</td>
      <td>55</td>
      <td>12.0</td>
      <td>2021</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 12 columns</p>
</div>



```python
dataframe.dtypes
```




    Name                     object
    gender                   object
    born_date                object
    born_city                object
    Age                       int64
    height_in_m             float64
    married                  object
    Spouse_or_Ex.partner     object
    Debut_year                int64
    total_films_aprox         int64
    USD_NetWorth_Million    float64
    Present_year              int64
    Active_year               int64
    dtype: object




```python
dataframe['Active_year']=dataframe['Present_year'] -  dataframe['Debut_year']
dataframe.sort_values(by=['Active_year'],inplace=True,ascending=False)
dataframe
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
      <th>gender</th>
      <th>born_date</th>
      <th>born_city</th>
      <th>Age</th>
      <th>height_in_m</th>
      <th>married</th>
      <th>Spouse_or_Ex.partner</th>
      <th>Debut_year</th>
      <th>total_films_aprox</th>
      <th>USD_NetWorth_Million</th>
      <th>Present_year</th>
      <th>Active_year</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>53</th>
      <td>Dilip Kumar</td>
      <td>Male</td>
      <td>11/12/1922</td>
      <td>Pakistan</td>
      <td>98</td>
      <td>1.78</td>
      <td>Divorced</td>
      <td>Asma Rehman,Saira Banu</td>
      <td>1944</td>
      <td>33</td>
      <td>85.0</td>
      <td>2021</td>
      <td>77</td>
    </tr>
    <tr>
      <th>71</th>
      <td>Rekha</td>
      <td>Female</td>
      <td>10/10/1954</td>
      <td>Chennai</td>
      <td>66</td>
      <td>1.65</td>
      <td>Divorced</td>
      <td>Mukesh Aggarwal</td>
      <td>1958</td>
      <td>113</td>
      <td>40.0</td>
      <td>2021</td>
      <td>63</td>
    </tr>
    <tr>
      <th>61</th>
      <td>Dharmendra</td>
      <td>Male</td>
      <td>8/12/1935</td>
      <td>Nasrali</td>
      <td>85</td>
      <td>1.78</td>
      <td>Yes</td>
      <td>Hema Malini</td>
      <td>1960</td>
      <td>149</td>
      <td>60.0</td>
      <td>2021</td>
      <td>61</td>
    </tr>
    <tr>
      <th>67</th>
      <td>Jeetendra</td>
      <td>Male</td>
      <td>7/4/1942</td>
      <td>Punjab</td>
      <td>79</td>
      <td>1.75</td>
      <td>Yes</td>
      <td>Shobha Kapoor</td>
      <td>1964</td>
      <td>109</td>
      <td>200.0</td>
      <td>2021</td>
      <td>57</td>
    </tr>
    <tr>
      <th>87</th>
      <td>Hema Malini</td>
      <td>Female</td>
      <td>16/10/1948</td>
      <td>Ammankundi</td>
      <td>72</td>
      <td>1.68</td>
      <td>Yes</td>
      <td>Dharmendra</td>
      <td>1968</td>
      <td>73</td>
      <td>60.0</td>
      <td>2021</td>
      <td>53</td>
    </tr>
    <tr>
      <th>...</th>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
      <td>...</td>
    </tr>
    <tr>
      <th>41</th>
      <td>Disha Patani</td>
      <td>Female</td>
      <td>13/6/1992</td>
      <td>Bareilly</td>
      <td>29</td>
      <td>1.70</td>
      <td>No</td>
      <td>NaN</td>
      <td>2015</td>
      <td>11</td>
      <td>12.0</td>
      <td>2021</td>
      <td>6</td>
    </tr>
    <tr>
      <th>69</th>
      <td>Bhumi Pednekar</td>
      <td>Female</td>
      <td>18/7/1989</td>
      <td>Mumbai</td>
      <td>31</td>
      <td>1.57</td>
      <td>No</td>
      <td>NaN</td>
      <td>2015</td>
      <td>13</td>
      <td>1.5</td>
      <td>2021</td>
      <td>6</td>
    </tr>
    <tr>
      <th>24</th>
      <td>Janhavi Kapoor</td>
      <td>Female</td>
      <td>6/3/1997</td>
      <td>Mumbai</td>
      <td>24</td>
      <td>1.63</td>
      <td>No</td>
      <td>NaN</td>
      <td>2018</td>
      <td>8</td>
      <td>8.0</td>
      <td>2021</td>
      <td>3</td>
    </tr>
    <tr>
      <th>32</th>
      <td>Sara Ali Khan</td>
      <td>Female</td>
      <td>12/8/1995</td>
      <td>Mumbai</td>
      <td>25</td>
      <td>1.63</td>
      <td>No</td>
      <td>NaN</td>
      <td>2018</td>
      <td>7</td>
      <td>2.0</td>
      <td>2021</td>
      <td>3</td>
    </tr>
    <tr>
      <th>70</th>
      <td>Ananya Pandey</td>
      <td>Female</td>
      <td>30/10/1998</td>
      <td>Mumbai</td>
      <td>22</td>
      <td>1.70</td>
      <td>No</td>
      <td>NaN</td>
      <td>2019</td>
      <td>3</td>
      <td>3.2</td>
      <td>2021</td>
      <td>2</td>
    </tr>
  </tbody>
</table>
<p>100 rows × 13 columns</p>
</div>


