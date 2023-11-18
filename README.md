# Move Zeroes Problem

## Problem Statement

The "Move Zeroes Problem" is a common algorithmic challenge that involves rearranging an array of integers by moving all zeros (`0`) to the end of the array while maintaining the relative order of the non-zero elements. The goal is to perform this operation in-place with minimal extra memory usage.

## Approach

The solution to this problem uses a two-pointer technique. The main idea is to iterate over the array and for each non-zero element found, swap it with a zero element, identified by a second pointer. This effectively pushes all zeros to the end of the array while keeping the original order of non-zero elements.

## Implementation

The implementation involves the following steps:

1. **Initialize Two Pointers**: Two pointers, `i` and `j`, are initialized at the start of the array. Pointer `i` is used for the array traversal, while `j` keeps track of the position to swap non-zero elements.

2. **Traverse and Swap**: As we iterate through the array with `i`, whenever a non-zero element is encountered, it is swapped with the element at the `j`th position, and `j` is incremented.

3. **Result**: The end result is that all zeros are moved to the end of the array, and the relative order of non-zero elements is maintained.

## Code Example (Python)

```python
def move_zeros(arr):
    i, j = 0, 0
    while i < len(arr):
        if arr[i] != 0:
            arr[i], arr[j] = arr[j], arr[i]
            j += 1
        i += 1
    return arr

# Example usage
arr = [0, 1, 0, 3, 12]
print("Original array:", arr)
print("Array after moving zeros:", move_zeros(arr))
```

## Usage

To use this code, simply call the `move_zeros` function with an array of integers as an argument. The function returns a new array with all zeros moved to the end.

## Complexity

- **Time Complexity**: O(n) - where `n` is the number of elements in the array. The array is traversed once.
- **Space Complexity**: O(1) - as the rearrangement is done in-place with no additional data structures used.

## Conclusion

This solution efficiently solves the Move Zeroes Problem with optimal time and space complexity, demonstrating the effectiveness of the two-pointer technique in array manipulation tasks.