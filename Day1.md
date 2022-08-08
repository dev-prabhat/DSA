
## [Remove Element](https://leetcode.com/problems/remove-element/)

```
Step are:
1- Take two pointer one at i=0 (outside of for loop) and other j=0 (for loop pointer)
2- Loop on the Array
3- If(nums[j] !== val) make change to the prev position of i index and i++ 
4- Return i
```

```var removeElement = function(nums, val) {
    var i=0;
    for(var j=0;j<nums.length;j++){
        if(nums[j] !== val){
            nums[i] = nums[j]
            i++
        }
    }
    return i
};
```
## [Sort Color](https://leetcode.com/problems/sort-colors/)

```
Step are:
1- Create three counter for zero, one and two
2- Loop through the array and increase the count of one, two and three
3- Now put zero, one and two in the array according to non-decreasing order
```

```var sortColors = function(nums) {
    var zero = 0, one = 0, two = 0
    for(var i=0;i<nums.length;i++){
        if(nums[i] === 0) zero++
        if(nums[i] === 1) one++
        if(nums[i] === 2) two++
    }
    
    for(var i=0;i<zero;i++) nums[i] = 0
    for(var i=zero;i<zero+one;i++) nums[i] = 1
    for(var i=zero+one;i<zero+one+two;i++) nums[i] = 2
};
```