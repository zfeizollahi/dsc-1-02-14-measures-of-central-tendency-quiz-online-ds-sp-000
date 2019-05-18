
# Measures of Central Tendency - Quiz

## Objectives
You will be able to:
* Understand and describe the significance of measuring central tendency of continuous data
* Understand the formula and intuition behind the mean, median, mode and modal class
* Compare mean-median-mode, along with histograms to explain the central tendency of given data

**Note, for these exercises, you do not need to write code to answer them - we'll do that later. Just do them by hand or with a calculator to make sure you're comfortable with the process of calculating the answers!**

### Exercise 1
Calculate the mean, median and mode for this data set: 
```
19, 18, 21, 16, 15, 17, 20, 18
```
While comparing the results of three measures, comment about this distribution. 


```python
import numpy as np
from scipy import stats
```


```python
# Your answer here 
my_list = [19, 18, 21, 16, 15, 17, 20, 18]
print(sorted(my_list))
print("Mean is ", np.mean(my_list))
print("Median is ", np.median(my_list))
print("Mode is", stats.mode(my_list)[0][0])
```

    [15, 16, 17, 18, 18, 19, 20, 21]
    Mean is  18.0
    Median is  18.0
    Mode is 18


Taking the average/mean gives us 18.
There are 8 elements total, which means the median will be the average of the 4th and 5th elements, both of which are 18, making the median also 18.
18 occurs twice, making it the mode.
The dataset is perfectly normal distribution. Having the three different central tendency measures doesn't really show us how these measures are different. One might be tempted to not report all three metrics for other datasets if you based the difference off of these numbers for this dataset.

### Exercise 2

Calculate the mean, median and mode for given distribution and state which of these measures does not describe the "middle" of this data set? and why ?
```
100, 99, 97, 97, 96, 98, 95, 72
```


```python
# Your answer here 
my_list = [100, 99, 97, 97, 96, 98, 95, 72]
print(sorted(my_list))
print("Mean is ", np.mean(my_list))
print("Median is ", np.median(my_list))
print("Mode is", stats.mode(my_list)[0][0])
```

    [72, 95, 96, 97, 97, 98, 99, 100]
    Mean is  94.25
    Median is  97.0
    Mode is 97


The mean is much lower than the median and mode, suggesting a skewed distribution. We see that 72 is an outlier and is pulling the mean down. Median and Mode both show 97 as the "middle" measures, which more accurately shows the central tendency which is upper 90s.

### Exercise 3
On the first three days of his bookshop opening, Joe sold 15, 18, and 16 books (He initially hoped that he would sell 17 books every day).  How many books does he need to sell on the next day to have a mean sale of 17?


```python
# Your answer here 
#17 = (15 + 18 + 16 + X) / 4
#17 = (15 + 18 + 16) / 4 + X / 4
#- X / 4 + 17 = (15 + 18 + 16) / 4
#- X / 4 = (15 + 18 + 16) / 4 - 17
#X / 4 =  - (15 + 18 + 16) / 4 + 17
X =  - (15 + 18 + 16)  + 17 * 4
X
```




    19



### Exercise 4
The histograms show the amount of time (hours per day) spent on Facebook by 46 middle school girls and 40 middle school boys from a school in San Francisco. A total of 50 boys and 50 girls took the survey, 4 girls and 10 boys did not use Facebook at all. 
Each is graphed with a bin width of 0.25 hours.

![](boys.png)
![](girls.png)

Looking at these histograms, answer following questions. 

*Hint: For most parts, you will have to figure out the location of required bins and count the frequencies. *

#### How many boys spend more than 1.5 hours/day on Facebook?



```python
# Your answer here 
13
```




    13



#### Compare the percentage of boys and girls that spend more than zero but less than 1 hour/day on Facebook.


```python
# Your answer here 
boys = 20 / 40 * 100
girls = 10  / 46 * 100
print("Boys ", boys)
print("Girls ", girls)
```

    Boys  50.0
    Girls  21.73913043478261


#### Find the bin where the median of the boys' data set lies.

#### Your answer here 
Bin with 1 hour or average between .75 - 1, and 1-1.25. Making median 1 hour.

#### In terms of Facebook usage times based on given data, what can you conclude about usage habits of boys and girls?

#### Your answer here 
Girls spend more time on on facebook.


```python

```
