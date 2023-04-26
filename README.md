# binary_search

A binary search algorithm is used to find the position of a specific value contained in a sorted array. Working with the principle of divide and conquer, this search algorithm can be quite fast, but the caveat is that the data has to be in a sorted form. It works by starting the search in the middle of the array and working going down the first lower or upper half of the sequence. If the median value is lower than the target value, that means that the search needs to go higher, if not, then it needs to look on the descending portion of the array.

Binary Search Working:-
1.The array in which searching is to be performed is:
![image](https://user-images.githubusercontent.com/127819492/234486055-61f9d04e-b1b9-4cd3-a3e5-0a70d67abe57.png)

Let x = 4 be the element to be searched.
2.Set two pointers low and high at the lowest and the highest positions respectively.
![image](https://user-images.githubusercontent.com/127819492/234486134-2e287604-7799-4aec-9ef6-1413ce68c002.png)

3.Find the middle element mid of the array ie. arr[(low + high)/2] = 6
![image](https://user-images.githubusercontent.com/127819492/234486209-361350cc-2b0c-4a05-84cd-becbdd840c34.png)

4.If x == mid, then return mid.Else, compare the element to be searched with m.

5.If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.

6.Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
![image](https://user-images.githubusercontent.com/127819492/234486281-3bd214f1-bf52-4410-a343-354c9744d3eb.png)

7.Repeat steps 3 to 6 until low meets high
![image](https://user-images.githubusercontent.com/127819492/234486357-8c2d1cd4-1a35-48d2-b65c-6421c599c494.png)

8.x = 4 is found.
![image](https://user-images.githubusercontent.com/127819492/234486410-b7e5664f-69e5-4362-b060-838c36c02da3.png)

Binary Search Algorithm:-

binarySearch(arr, x, low, high)
if low > high
return False
else
mid = (low + high) / 2
if x == arr[mid]
return mid
else if x > arr[mid] // x is on the right side
return binarySearch(arr, x, mid + 1, high)
else // x is on the left side
return binarySearch(arr, x, low, mid - 1)


Time Complexities

Best case complexity:
O(1)

Average case complexity:
O(log n)

Worst case complexity:
O(log n)

Space Complexity

The space complexity of the binary search is O(1).

