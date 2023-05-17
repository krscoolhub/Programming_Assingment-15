# Programming_Assingment-15


1. Please write a program using generator to print the numbers which can be divisible by 5 and 7 between 0 and n in comma separated form while n is input by console.
sol:
def task1(n):
    
    for i in range(n+1):
        if i % 5 == 0 and i % 7 == 0:
            yield str(i)+' '
task1(100)
<generator object task1 at 0x000001A94CD60430>
print(', '.join([i for i in task1(100)]))
0 , 35 , 70 




2. Please write a program using generator to print the even numbers between 0 and n in comma separated form while n is input by console.
sol:
def task2(n):

    for i in range(n+1):
        if i % 2 == 0:
            yield str(i)
print(', '.join([i for i in task2(10)]))
0, 2, 4, 6, 8, 10




3. Please write a program using list comprehension to print the Fibonacci Sequence in comma separated form with a given n input by console.
sol:
def fibo(n):
    i = 0
    j = 1
    for k in range(n+1):
        yield i
        i,j = j, i+j
print(','.join([str(num) for num in fibo(7)]))
0,1,1,2,3,5,8,13




4. Assuming that we have some email addresses in the "username@companyname.com" format, please write program to print the user name of a given email address. Both user names and company names are composed of letters only.
sol:
def username(email: str):
    return email.split('@')[0]
username('john@google.com')
'john'





5. Define a class named Shape and its subclass Square. The Square class has an init function which takes a length as argument. Both classes have a area function which can print the area of the shape where Shape's area is 0 by default.
sol:
class Shape:
    def __init__(self, length):
        self.length = length
        
    def area(self):
        return 0
    
class Square(Shape):
    def area(self):
        return self.length*self.length
shape_obj = Shape(10)

shape_obj.area()
0
square_obj = Square(13)

square_obj.area()
169



