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