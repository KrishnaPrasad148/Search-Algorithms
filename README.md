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
```
Developed By: S.Krishna Prasad
Register No: 212223230108
```
i)	#Use a linear search method to match the item in a list.
```
lst = eval(input())
num = int(input())
index = 0
check = 0
lst = sorted(lst)
print(lst)
for i in range(len(lst)):
    if lst[i]==num:
        check = 1
        index = i
if(check==True):
    print(f"Element found at index:  {index}")
else:
    print("Element not found")
        


```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```


def binary_search(arr, x):
	low = 0
	high = len(arr) - 1
	mid = 0

	while low <= high:

		mid = (high + low) // 2

		if arr[mid] < x:
			low = mid + 1

		elif arr[mid] > x:
			high = mid - 1

		else:
			return mid

	return -1


lst = eval(input())
lst = sorted(lst)
x = int(input())
print(lst)

result = binary_search(lst, x)

if result != -1:
	print("Element found at index: ", str(result))
else:
	print("Element not found")




```
iii)	# Find the element in a list using Binary Search (recursive Method).
```


def binary_search(arr, low, high, x):

	if high >= low:

		mid = (high + low) // 2

		if arr[mid] == x:
			return mid

		elif arr[mid] > x:
			return binary_search(arr, low, mid - 1, x)

		else:
			return binary_search(arr, mid + 1, high, x)

	else:
		return -1

lst = eval(input())
lst = sorted(lst)
x = int(input())
print(lst)

result = binary_search(lst, 0, len(lst)-1, x)

if result != -1:
	print("Element found at index: ", str(result))
else:
	print("Element not found")




```
## Sample Input and Output
# i)
![image](https://github.com/KrishnaPrasad148/Search-Algorithms/assets/147332763/3b5e1a9d-a7c7-4eef-8462-9b864b40c1d3)


# ii)
![image](https://github.com/KrishnaPrasad148/Search-Algorithms/assets/147332763/5af89332-b60b-4660-880f-cc8c36797413)

![image](https://github.com/KrishnaPrasad148/Search-Algorithms/assets/147332763/ef517f75-542e-4ca2-aaf3-b7c1ee1ac10f)


# iii)
![image](https://github.com/KrishnaPrasad148/Search-Algorithms/assets/147332763/2be2f04f-580b-4506-82e0-62447a21b928)

![image](https://github.com/KrishnaPrasad148/Search-Algorithms/assets/147332763/dd0ef17c-ad5b-4e5d-a516-c63dec21991c)




## Result
Thus the linear search and binary search algorithm is implemented using python programming.
