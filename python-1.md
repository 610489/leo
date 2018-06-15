# 輸入與輸出
## 輸入:input 
```
#!/usr/bin/env python
#coding=utf-8

# radius = 25 
# Input(輸入):Prompt the user to enter a radius
radius = eval(input("Enter a number for radius: "))

# Processing(處理):Compute area
area = radius * radius * 3.1415962

# Output(輸出):Display results
print("The area for the circle of radius", radius, "is", area)

```
python3 a1.py
```
Enter a number for radius: 12
The area for the circle of radius 12 is 452.38985279999997
```
python2 a1.py
```
Enter a number for radius: 12
Traceback (most recent call last):
  File "a1.py", line 6, in <module>
    radius = eval(input("Enter a number for radius: "))
TypeError: eval() arg 1 must be a string or code object
```
## 同時指定
```
#!/usr/bin/env python
#coding=utf-8

# Prompt the user to enter three numbers
number1, number2, number3 = eval(input("Enter three numbers separated by commas: "))

# Compute average
average = (number1 + number2 + number3) / 3

# Display result
print("The average of", number1, number2, number3, "is", average)
```
## 格式化輸出
方法1:使用format()
"{0} love {1}......{2}".format("I","listening","classical Music")
方法2:使用%
```
'%c' % 97
'%c %c %c %c %c'% (97,98,99,100,101)
'%d 八進位是%0 , 十六進位是  %x' % (97,97, 97)
符  號	描述
```







































