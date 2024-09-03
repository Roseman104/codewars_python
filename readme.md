# CodeWars repo for CodeWars things

Trying CodeWars everyday to re-remember best practices, virtual environments etc. 

## Multiples of 3 or 5
01/Sep/2024
<br>
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
<br>
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. 

```python
def solution(number):
    print(f'The number input is: {number}')
    list = range(1, number)
    #print(list)
    sum = 0
    for int in list:
        if int % 3 == 0 or int % 5 == 0:
            print(int)
            sum += int
    print(f'The Sum is {sum}')
    return sum
```



## Outliers
01/Sept/2024
<br>
If we list all the natural numbers below 10 that are multiples of 3 or 5, we get 3, 5, 6 and 9. The sum of these multiples is 23.
<br>
Finish the solution so that it returns the sum of all the multiples of 3 or 5 below the number passed in. 







```python
def find_outlier(list):
    evens = 0
    odds = 0
    if len(list) >= 3:
        for item in list:
            if item % 2 == 0:
                evens += 1
        for item in list:
            if item % 2 != 0:
                odds += 1                    
    if evens > 1:
        print('EvenList')
        return outlier_odd(list)
    else: 
        print('OddList')
        return outlier_even(list)

def outlier_even(list):
    for item in list:
        if item % 2 == 0:
            return item

def outlier_odd(list):
    for item in list:
        if item % 2 != 0:
            return item
```


## persistence bugger
Write a function, `persistence`, that takes in a positive parameter `num` and returns its multiplicative persistence, which is the number of times you must multiply the digits in `num` until you reach a single digit.

<br>

39 --> 3 (because 3*9 = 27, 2*7 = 14, 1*4 = 4 and 4 has only one digit, there are 3 multiplications)
<br>
999 --> 4 (because 9*9*9 = 729, 7*2*9 = 126, 1*2*6 = 12, and finally 1*2 = 2, there are 4 multiplications)
<br>
4 --> 0 (because 4 is already a one-digit number, there is no multiplication)



```python
def pos_primer(num):
    result = 1
    num_str = str(num)
    for d in str(num_str):
        n = int(d)
        result *= n  
    return result

def persistence(num):
    if num < 10:
        return 0
    count = 1
    x = pos_primer(num)
    print(x)
    while x > 9:
        count +=1
        x = pos_primer(x)
        print(x)
    return count
```