## List Methods :

###  list :
* In Python, a list is a built-in data structure used to store a collection of items or elements. Lists are ordered and mutable, which means you can change their content by adding, removing, or modifying elements. Each element in a list is assigned an index, starting from 0 for the first element.

#####   Now we discuss about some list methods in python

### Sort :
* In Python, sorting a list means arranging the elements in the list in a particular order, either in ascending (smallest to largest) or descending (largest to smallest) order. You can sort a list using the sort() method or the sorted() function. Both methods will rearrange the elements of the list in a sorted order without altering the original list.
  

<b> Syntax : </b>  my_list = [3, 1, 4, 1, 5, 9, 2, 6, 5, 3, 5]

my_list.sort()


  


```python
help(list.sort)
```

    Help on method_descriptor:
    
    sort(self, /, *, key=None, reverse=False)
        Sort the list in ascending order and return None.
        
        The sort is in-place (i.e. the list itself is modified) and stable (i.e. the
        order of two equal elements is maintained).
        
        If a key function is given, apply it once to each list item and sort them,
        ascending or descending, according to their function values.
        
        The reverse flag can be set to sort in descending order.
    
    


```python
m=[10,9,8,7,6,5,4,3,2,1]
m.sort() ##-->it will prints asscending order
m
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]




```python
m,n=[1,2,3,4,5],['aaa','AAA','a.appadam','aniii']
c=m+n ##--> concatinating 2 lists (adding)
c
```




    [1, 2, 3, 4, 5, 'aaa', 'AAA', 'a.appadam', 'aniii']




```python
c
```




    [1, 2, 3, 4, 5, 'aaa', 'AAA', 'a.appadam', 'aniii']




```python
c=['AAA','aaa','a.anii','abhilash']
c.sort() ##-> it gives ascending order as alphabetical order (follows ascii)
c
```




    ['AAA', 'a.anii', 'aaa', 'abhilash']



###  Reverse sorting ( ) 

* Reverse sorting in Python refers to arranging the elements of a sequence, such as a list, tuple, or other iterable, in descending order. When you reverse sort a sequence, the largest elements come first, and the order is reversed compared to the default ascending (smallest to largest) order. You can achieve reverse sorting by specifying the reverse=True argument when using sorting functions or methods.

<b> Syntax : </b> my_list.sort(reverse=True)

where;

* The sorted() function with the reverse=True argument to create a new list sorted in reverse order:



```python
bb=[2,-8,10,-5,26,-22,90,-90,100,-3]
bb.sort(reverse=True) ###-->it gives descending order
bb
```




    [100, 90, 26, 10, 2, -3, -5, -8, -22, -90]



### Index 
* Indexing in Python refers to the process of accessing individual elements within a data structure, such as a list, tuple, or string, by their position or index. In Python, indexing starts at 0 for the first element, so the index 0 refers to the first element, index 1 to the second element, and so on.


```python
help(list.index)
```

    Help on method_descriptor:
    
    index(self, value, start=0, stop=9223372036854775807, /)
        Return first index of value.
        
        Raises ValueError if the value is not present.
    
    


```python
bb
```




    [100, 90, 26, 10, 2, -3, -5, -8, -22, -90]




```python
c
```




    ['AAA', 'a.anii', 'aaa', 'abhilash']




```python
c.index('a.anii') ##--> accesing the index number of given word
```




    1




```python
c[-1]  ##---> Reverse indexing
```




    'abhilash'




```python
c[0:4] ##--->slicing
```




    ['AAA', 'a.anii', 'aaa', 'abhilash']




```python
c
```




    ['AAA', 'a.anii', 'aaa', 'abhilash']



### Reverse 

* In Python, you can reverse a list in-place using the reverse() method. The reverse() method is a built-in method that belongs to the list data type, and it reverses the order of elements within the list without creating a new list.

<b>Syntax : </b> my_list.reverse()



```python
help(list.reverse)
```

    Help on method_descriptor:
    
    reverse(self, /)
        Reverse *IN PLACE*.
    
    


```python
c=[5, 4, 3, 2, 1,'string','tuple','list']
c.reverse() ##-->it prints the given list in reverse
c

```




    ['list', 'tuple', 'string', 1, 2, 3, 4, 5]



### Clear ( )

* In Python, the term "clear" typically refers to removing all the elements from a data structure, such as a list. You can clear a list by using the clear() method. This method removes all elements from the list, leaving it empty.

<b> Syntax : </b> my_list.clear()


```python
help(list.clear)
```

    Help on method_descriptor:
    
    clear(self, /)
        Remove all items from list.
    
    


```python
a = [1, 2, 3, 4, 5]

a.clear() ##-->it clears all the elements in list and gives an empty list

print(a)

```

    []
    

* In the example, we start with a list called <b>a</b> containing elements. When we call the clear() method on <b>a</b> , it removes all the elements, leaving an empty list ([]). This is a way to efficiently clear the contents of a list without needing to create a new list or assign an empty list to the variable.

### Copy :
* In Python, the "copy" method for lists usually refers to creating a new copy of a list, which is independent of the original list. You can create a shallow copy of a list using the copy() method or the list() constructor. A shallow copy creates a new list, but the elements themselves are not deeply copied; they are references to the same objects as the original list.

<b>Syntax : </b> my_list = my_list.copy()



```python
help(list.copy)
```

    Help on method_descriptor:
    
    copy(self, /)
        Return a shallow copy of the list.
    
    


```python
a=[1,2,3,4,5,[6,7,8]]
b=a
b.append(6)  ##-->adding an element to the list by using append
b
```




    [1, 2, 3, 4, 5, [6, 7, 8], 6]




```python
a
```




    [1, 2, 3, 4, 5, [6, 7, 8], 6]




```python
id (a)
```




    2858093805632




```python
id(b)           ##--> memory location of variable 'b'
```




    2858093805632




```python
hex(id(a[0]))
```




    '0x7ffea2429328'




```python
hex(id(b[0]))
```




    '0x7ffea2429328'




```python
hex(id(a[5]))
```




    '0x29973a63b40'




```python
hex(id(b[5])) ##--> finding memory location of a particular position of index number
```




    '0x29973a63b40'




```python
hex(id(a[5][2]))
```




    '0x7ffea2429408'




```python
hex(id(b[5][2]))  ##--> finding memory location of list with in a list
```




    '0x7ffea2429408'




```python
import copy
from copy import deepcopy
```


```python
a=[1,[4,5,6]]
b=deepcopy(a)
print(a,id(a),id(a[1]))
print(b,id(b),id(b[1]))
```

    [1, [4, 5, 6]] 2858093740096 2858079093760
    [1, [4, 5, 6]] 2858093713088 2858093723584
    

### Tuple ( )

* A tuple in Python is an ordered, immutable collection of elements. Unlike lists, which are mutable (meaning their contents can be modified), tuples are immutable, which means that once you create a tuple, you cannot change its elements or their order. Tuples are often used to store related pieces of data as a single unit.

<b> Syntax : </b>  my_tuple = (element1, element2, element3, ...)

where;

my_tuple is the name of the tuple variable.
(...) denotes a tuple, and inside the parentheses, you can include the elements you want to store in the tuple, separated by commas.



```python
my_tuple = (1, "apple", 3.14, "banana", True)

```


```python
## help(tuple)
```

* Tuples can contain elements of different data types, as shown in the example above. You can access elements within a tuple using indexing, just like you would with a list. The key distinction is that you cannot modify the elements or the order of a tuple once it's created, making tuples suitable for situations where data should remain constant and not be accidentally changed.

### Unpacking :

* Unpacking in Python, often referred to as tuple unpacking, is the process of extracting individual elements from a tuple and assigning them to separate variables. Tuple unpacking allows you to access and work with the elements of a tuple conveniently. You can assign the elements of a tuple to multiple variables in a single line of code.

<b>Syntax </b> variable1, variable2, variable3, ... = my_tuple

Where;

variable1, variable2, variable3, etc. are the variables where you want to store the individual elements from the tuple.
my_tuple is the tuple from which you want to unpack the elements.


```python
h,g=(5,6)
h
```




    5




```python
g
```




    6




```python
z=(5,)
print(z,type(z),len(z))
```

    (5,) <class 'tuple'> 1
    


```python
a=tuple(range(1))
a
```




    (0,)




```python
dir(tuple)
```




    ['__add__',
     '__class__',
     '__class_getitem__',
     '__contains__',
     '__delattr__',
     '__dir__',
     '__doc__',
     '__eq__',
     '__format__',
     '__ge__',
     '__getattribute__',
     '__getitem__',
     '__getnewargs__',
     '__getstate__',
     '__gt__',
     '__hash__',
     '__init__',
     '__init_subclass__',
     '__iter__',
     '__le__',
     '__len__',
     '__lt__',
     '__mul__',
     '__ne__',
     '__new__',
     '__reduce__',
     '__reduce_ex__',
     '__repr__',
     '__rmul__',
     '__setattr__',
     '__sizeof__',
     '__str__',
     '__subclasshook__',
     'count',
     'index']




```python
a=(1,3,5)
a
```




    (1, 3, 5)




```python
a[0] ##--> indexing
```




    1




```python
## a[0]=5 uncomment to see the error
# a
```


```python
x=(1,2,3,4,[5,6])
x
```




    (1, 2, 3, 4, [5, 6])




```python
x[4].append(7)  ##--> adding one element by using append
x
```




    (1, 2, 3, 4, [5, 6, 7])




```python

```
