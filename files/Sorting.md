# Sorting
## Sort 0:
* Until you make a whole pass through the array with no swaps:
  - until you make a whole pass through the array:
    * consider adjacent elements in pairs, if the earlier of the pair is bigger than the later of the pair, swap the elements
    * move on to the next pair of adjacent elements (the later of this pair should end up being the earlier of the next two pairs)


## Sort 1:
* Until your sub-array is the whole array:
    - expand your sub-array by one element
    - find the spot the new element belongs
    - move the elements in the sub-array that are greater than the new element (and thus must come after it)
    - put the new element in its rightful spot

## Sort 2:
* Starting at the beginning, until you pass through the whole array:
  - find the element that belongs in this spot by:  
  starting one right of the current spot until you make it through the rest of the array:
    * compare current to smallest yet and record the index of the smaller of the two
  - swap element in current spot with the smallest considered element