
### [Remove Element](https://leetcode.com/problems/remove-element/)

var removeElement = function(nums, val) {
    var i=0;
    for(var j=0;j<nums.length;j++){
        if(nums[j] !== val){
            nums[i] = nums[j]
            i++
        }
    }
    return i
};

### [Sort Color](https://leetcode.com/problems/sort-colors/)

var sortColors = function(nums) {
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