# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
i)	#Use a linear search method to match the item in a list.
```
def linearSearch(array,n,k):
    array.sort()
    for i in range(n):
        if array[i]==k:
            return i
    return -1
            
array = eval(input())
k = eval(input()) # k-item to be seared for
n=len(array)
result =linearSearch(array,n,k) # use the function for linear search
if result!=-1:
    print(array,'\nElement found at index: ',result)
else:
    print(array,'\nElement not found')
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarySearchIter(array, k, low, high):
    while low<=high:
        mid=(high+low)//2
        if array[mid]==k:
            return mid+1
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    else:
        return -1
array = eval(input())
k = eval(input()) 
array.sort()
low,high=0,len(array)-1
result=binarySearchIter(array, k, low, high)
if result!=-1:
    print(array)
    print('Element found at index: ',result-1)
else:
    print(array)
    print('Element not found')
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def binarySearchIter(array, k, low, high):
    if low<=high:
        mid=(high+low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            return binarySearchIter(array, k,mid+1, high)
        else:
            return binarySearchIter(array, k,low,mid-1)
    else:
        return -1
array = eval(input())
k = eval(input()) 
array.sort()
low,high=0,len(array)-1
result=binarySearchIter(array, k, low, high)
if result!=-1:
    print(array)
    print('Element found at index: ',result)
else:
    print(array)
    print('Element not found')
```
## Sample Input and Output

PROGRAM 1

![Alt text](<Linear search 1.png>)

PROGRAM 2

![Alt text](<Linear search 2.png>)

PROGRAM 3

![Alt text](<Linear search 3.png>)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.