### Contents:
- [Data Structures](#data-structures)
  - [Lists](#lists)
  - [Dictionaries](#dictionaries)
  - [Sets](#sets)
- [Algorithms](#algorithms)
  - [Search Sort](#search-sort)
- [Programming Techniques](#programming-techniques)
  - [Strings](#strings)
  - [Tuples](#tuples)
  - [Enumerate](#enumerate)

# *Data Structures*
## Lists
### Initialising a List
```python
# Empty list
new_list = []
# Populated list
new_list = [1, 2, 3]
# Fixed length list
new_list = [-1] * list_length
# Fixed length list of lists
new_list = [[] for _ in range(list_length)]
```
### List Indexing and Slicing
```python
# First item
first_item = my_list[0]
# Nested list value
nested_item = my_list[0][1]
# Negative indexing
last_item = my_list[-1]

# my_list = ['a', 'b', 'c', 'd', 'e', 'f', 'g']
# Index 2 to index 4
sliced_list = my_list[2:5] # returns ['c', 'd', 'e']
# Index 5 to end
sliced_list = my_list[5:] # returns ['f', 'g']
# Start to index 5
sliced_list = my_list[:-2] # returns ['a', 'b', 'c', 'd', 'e']
# list[start:stop:step]
my_list[::2] # returns ['a', 'c', 'e', 'g']
```
   
### List Methods
```python
# INDEX() gets index of 'elem', from indexes start to (end-1), PROBS better to slice before
index = my_list.index('elem', start(optional), end(optional))

# APPEND() an elem to end of list
my_list.append('elem')

# EXTEND() multiple elems (synthesize into) end of list - elems is any iterable
my_list.extend(['elem1', 'elem2'])
# alternatives to extend()
my_list += extension_list
my_list[len(my_list):] = extension_list

# INSERT() an elem into index i, shifting values after to the right. i=0 inserts at list start
my_list.insert(i, 'elem')
# inserting multiple elems (synthesize into existing list) into index 2
my_list[2:2] = ['elem1', 'elem2']

# REMOVE() the first occurence of elem
my_list.remove('elem')

# POP() removes the element at given index, returning the elem
removed_element = my_list.pop(index)

# COUNT() returns the number of occurences of an elem
occurences = my_list.count('elem')

# REVERSE() the order of list elements (mutates)
my_list.reverse()

# SORT() the list elements ascending, optional params (key=..., reverse=...) (mutates)
my_list.sort()

# COPY() creates a shallow copy the list 
new_list = my_list.copy()
  # new_list changes NOT reflected in my_list, except for objects, as shallow copy uses O.G. references
  # A deep copy would construct new objects
  
# CLEAR() removes every elem in a list
my_list.clear()
```

### Advanced List Techniques
```python
# Compare every element in list to one another, no repetition
 for i in range(len(my_list)):
  for j in range(i + 1, len(my_list)):
      compare(mylist[i], mylist[j])
 ```
## Dictionaries 
   
## Sets  
```python
# Initialise
my_set = {1, 2, 3}
# Initialise empty
x = set()
```
- Sets are iterable, unordered, with no duplicates.
- Cannot use indexing
- Can turn into ordered with `list(my_set)`
- add(), update() - *multiple*, discard(), remove() - *throws err*, pop() - *random*, clear(), copy()
- union(), intersection(), difference(), symmetric_difference(), issubset(), issuperset()

```python
# Get every unique subset of a set (Powerset)
  my_list = list(s) 
  powerset = [[]]
  for num in my_list:
      powerset += [prev_item + [num] for prev_item in powerset]
```

## Linked Lists 
### Detecting cycles
```python
# Compare nodes with a visited set
    if head == None:
        return False
        
    visited = set()
    curr = head
    while curr:
        if curr in visited:
            return 1
        visited.add(curr)
        curr = curr.next
    return 0
    
# Floyd cycle detection algorithm (Tortoise-and-Hare) 
    if head == None:
        return False
        
    slow = head
    fast = head.next # WHY
    while (slow != fast):
        if (fast == None or fast.next == None):
            return False
        else:
            slow = slow.next
            fast = fast.next.next
    return True
```
   
# *Algorithms*
## Search Sort
   
# *Programming Techniques*
## Iterator

## Strings
   
## Tuples  
   
## Enumerate
   

# Heading 1
## Heading 2
### Heading 3

**bold text** 
*italicized text*

`print("INLINE CODE")`

```
print("BLOCK CODE")
```

> blockquote

That is so funny! :joy:

X<sup>2</sup>

1. First item
2. Second item
3. Third item

- First item
- Second item
- Third item

---

[Link to section](#section-id)
  
[HackerRank](https://www.hackerrank.com/dashboard)

Here's a sentence with a citation. [^1]
[^1]: [wikipedia](https://www.wikipedia.org/)

### Section id

