# Python Code Snippets
 
 
## List
 
```python
# Create a list and iterate over it
 
numbers = []
numbers.append(1)
numbers.append(2)
numbers.append(3)
 
for num in numbers:
  print(num)
 
'''
1
2
3
'''
```
 
```python
# Create a list and iterate over it
 
numbers = [1, 2, 3]
length = len(numbers)
for i in range(length):
  print(numbers[i])
 
# Output
'''
1
2
3
'''
```
 
```python
# Modify values in a list
 
numbers = [1, 2, 3]
for i in range(len(numbers)):
   numbers[i] += 1
print(numbers)
 
'''
[2, 3, 4]
'''
```
 
```python
# Sort a list in-place in ascending order
 
a = [2, 4, 1, 9, 8]
a.sort()
print(a)
 
'''
[1, 2, 4, 8, 9]
'''
```
 
```python
# Sort a list in-place in descending order
 
a = [2, 4, 1, 9, 8]
a.sort(reverse = True)
print(a)
 
'''
[9, 8, 4, 2, 1]
'''
```
 
## Strings
 
```python
# Declare a string and iterate over the characters
 
string = 'Hello'
for c in string:
  print(c)
 
'''
H
e
l
l
o
'''
```
 
```python
# Declare a string and iterate over the characters
 
string = 'Hello'
for i in range(len(string)):
  print(string[i])
 
'''
H
e
l
l
o
'''
```
 
```python
# Modifying a string
 
string = 'hello'
string[0] = 'H'
 
'''
TypeError: 'str' object does not support item assignment
'''
```
 
```python
# Sort a string
 
s = 'shivam'
sorted_s = ''.join(sorted(s))
print(sorted_s)
 
'''
ahimsv
'''
```
 
 
## Tuples
 
```python
# Declare a tuple and iterate over it
 
vowels = ('a', 'e', 'i', 'o', 'u')
for v in vowels:
   print(v)
 
'''
a
e
i
o
u
'''
```
 
```python
# Declare a tuple and print elements
 
vowels = ('a', 'e', 'i', 'o', 'u')
print(vowels[0])
print(vowels[2])
print(vowels[-1])
 
'''
a
i
u
'''
```
 
```python
# Modify a tuple
 
vowels = ('a', 'e', 'i', 'o', 'u')
vowels[0] = 'b'
 
'''
TypeError: 'tuple' object does not support item assignment
'''
```
 
## Dictionary
 
```python
# Declare a dictionary and print key value pairs
 
d = {'1': 'Dhoni', '2': 'Sachin', '3': 'Dravid'}
 
for k,v in d.items():
  print(k,v)
 
'''
1 Dhoni
2 Sachin
3 Dravid
'''
```
 
```python
# Dynamically insert key values and print it
 
d = {}
 
# Store square of numbers from 1 to 5
for i in range(1, 6):
  d[i] = i*i
 
# Print the square
for k,v in d.items():
  print(k,v)
 
# Output
'''
1 1
2 4
3 9
4 16
5 25
'''
```
 
## Set
 
```python
# Declare a set, insert values and print it
 
s = set()
s.add(1)
s.add(4)
s.add(3)
s.add(1)
print(s)
 
'''
{1, 3, 4}
'''
```
 
## 2D list/array
 
```python
# Declare a 2D list
 
N = 5
M = 5
 
matrix = [0]*N
for i in range(N):
   col = [0]*M
   matrix[i] = col
print(matrix)
 
'''
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
'''
```
 
```python
# Declare a 2D list
 
N = 5
M = 5
 
matrix = [[0 for j in range(M)] for i in range(N)]
print(matrix)
 
'''
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
'''
```
 
```python
# Declare a 2D list
 
N = 5
M = 5
 
matrix = [[0]*M for i in range(N)]
print(matrix)
 
'''
[[0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0], [0, 0, 0, 0, 0]]
'''
```
 
```python
# Modify the values in a 2D list
 
matrix = [[0]*4 for i in range(3)]
for i in range(3):
   for j in range(4):
       matrix[i][j] += 1
print(matrix)
 
'''
[[1, 1, 1, 1], [1, 1, 1, 1], [1, 1, 1, 1]]
'''
```
 
## Deque
 
```python
# Operations on deque
 
from collections import deque
 
dq = deque([])
dq.append(1)
dq.append(2)
dq.appendleft(3)
dq.appendleft(4)
print(dq)
print(dq.pop())
print(dq.popleft())
 
'''
deque([4, 3, 1, 2])
2
4
'''
```
 
## Queue
 
```python
# Implement queue using deque
 
from collections import deque
 
q = deque([])
q.append(1)
q.append(2)
q.append(3)
print(q)
print(q.popleft())
print(q.popleft())
 
'''
deque([1, 2, 3])
1
2
'''
```
 
```python
# Implement queue using Queue
 
from queue import Queue
q = Queue()
q.put(1)
q.put(2)
q.put(2)
print(q.qsize())
print(q.get())
print(q.get())
print(q.qsize())
 
'''
3
1
2
1
'''
```
 
## Stack
 
```python
# Implement stack using list
 
stack = []
stack.append(1)
stack.append(2)
stack.append(3)
 
print(stack)
print(stack.pop())
print(stack.pop())
print(stack)
 
'''
[1, 2, 3]
3
2
[1]
'''
```
 
```python
# Implement stack using deque
 
from collections import deque
 
stack = deque([])
stack.append(1)
stack.append(2)
stack.append(3)
 
print(stack)
print(stack.pop())
print(stack.pop())
print(stack)
 
'''
deque([1, 2, 3])
3
2
deque([1])
'''
```
 
## Ordered dictionary
 
```python
# Operations on ordereddict
 
from collections import OrderedDict
 
d = OrderedDict()
d[1] = 2
d[2] = 3
d[3] = 4
 
# If we print the dictionary now, the keys will be printed in order of insertion.
for k,v in d.items():
  print(k,v)
 
print(d.popitem(last=False))
print(d.popitem())
 
'''
1 2
2 3
3 4
(1, 2)
(3, 4)
'''
```
 
## Defaultdict
 
```python
# Operations on defaultdict
 
from collections import defaultdict
 
numbers = [1, 1, 2, 5, 2, 8]
d = defaultdict(int)
 
for num in numbers:
   d[num] += 1
 
for k,v in d.items():
   print(k, v)
 
'''
1 2
2 2
5 1
8 1
'''
```
 
## Counters
 
```python
from collections import Counter
 
numbers = [1, 1, 2, 5, 2, 8]
cntr = Counter(numbers)
 
for k,v in cntr.items():
   print(k, v)
 
'''
1 2
2 2
5 1
8 1
'''
```
 
## Namedtuples
 
```python
from collections import namedtuple
 
Point = namedtuple('Point', ['x', 'y'])
p1 = Point(1, 2)
print(p1.x, p1.y)
 
'''
1 2
'''
```
 
## Heaps
 
```python
# Min heap usage
 
import heapq
 
L = []
heapq.heapify(L) # Min heap
heapq.heappush(L, 3) # Pushing 3 into heap
heapq.heappush(L, 2) # Pushing 2 into heap
print(L)
print(heapq.heappop(L)) # Popping the minimum element
print(L)
 
'''
[2, 3]
2
[3]
'''
```
 
## Binary search
 
```python
# Check if an elements is present or not and return the index if element is present
 
from bisect import bisect_left
a = [1, 2, 4, 4, 5]
x = 4
idx = bisect_left(a, x)
if idx != len(a) and a[idx] == x:
   print(f'{x} is present at index {idx}')
else:
   print('Element not found')
 
'''
4 is present at index 2
'''
```
 
```python
# Find index of first element greater than or equal to target(x)
 
from bisect import bisect_left
a = [1, 2, 4, 4, 5]
x = 6
idx = bisect_left(a, x)
if idx == len(a):
   print('All elements are smaller than the target element')
else:
   print(idx)
 
'''
All elements are smaller than the target element
'''
```
 
```python
# Find index of first element greater than target(x)
 
from bisect import bisect_right
a = [1, 2, 4, 4, 5]
x = 4
idx = bisect_right(a, x)
if idx == len(a):
   print('All elements are smaller than the target element')
else:
   print(idx)
 
'''
4
'''
```
 
## Linked list
 
```python
# Create a singly linked list and traverse it
 
class Node:
  def __init__(self, data):
      self.data = data
      self.next = None
 
class LinkedList:
  def __init__(self):
      self.head = None
   def insert_at_end(self, data):
      new_node = Node(data)
      if self.head is None:
          self.head = new_node
      else:
          temp = self.head
          while(temp.next):
              temp = temp.next
          temp.next = new_node
   def traverse(self):
      temp = self.head
      while(temp):
          print(temp.data)
          temp = temp.next
 
ll = LinkedList()
ll.insert_at_end(1)
ll.insert_at_end(2)
ll.insert_at_end(3)
ll.traverse()
 
'''
1
2
3
'''
```
 
## Binary Tree
 
```python
# Create a binary tree and traverse it
 
class Node:
  def __init__(self, data):
      self.data = data
      self.left = None
      self.right = None
 
root = Node(1)
root.left = Node(2)
root.right = Node(3)
root.left.left = Node(4)
root.right.left = Node(5)
 
# Binary tree created from the above code
'''
              1
             / \
            2   3
           /     \
          4       5
'''
 
def inorder(root):
  if not root:
      return
  print(root.data)
  inorder(root.left)
  inorder(root.right)
 
inorder(root)
 
'''
1
2
4
3
5
'''
```
 
## Graph
 
```python
# Create a graph and traverse it
 
from collections import defaultdict
 
graph = defaultdict(list)
graph[1].append(2) # 1 -> 2
graph[2].append(3) # 1 -> 2 -> 3
graph[4].append(1) # 4 -> 1 -> 2 -> 3

 
def dfs(node, graph, visited=set()):
  if node not in visited:
      print(node)
      visited.add(node)
      for v in graph[node]:
          dfs(v, graph, visited)
 
dfs(4, graph, visited)
 
'''
4
1
2
3
'''
```

