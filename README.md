# DATE
# EX-07 Linear Search and Binary search
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
#developed by:Bhuvaneshwari M
#register number:212223230033

def search(array,key,n):
    for i in range(0,n):
        if key==array[i]:
            return i
    return -1
array=eval(input())
key=int(input())
array.sort()
n=len(array)
print(array)
result=search(array,key,n)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
#developed by:Bhuvaneshwari M
#register number:212223230033

def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found ")
else:
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
#developed by: Bhuvaneshwari M
#register number:212223230033

def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
## Sample Input and Output
![Screenshot 2024-10-04 101444](https://github.com/user-attachments/assets/f9a8431b-2536-4c3b-b2b2-f4ef3a89783d)
![Screenshot 2024-10-04 101552](https://github.com/user-attachments/assets/c325e660-a13d-40db-8c8f-53ae05d7cb50)
![Screenshot 2024-10-04 101601](https://github.com/user-attachments/assets/c7b9b4c0-8bb5-41a2-a408-5c7d8b2606d9)
![Screenshot 2024-10-04 101613](https://github.com/user-attachments/assets/8fff7709-09b5-4fbb-aef4-ef4c86d29bba)
![Screenshot 2024-10-04 101622](https://github.com/user-attachments/assets/e44cab45-44b4-4e6d-8a11-5c1516855ce4)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
