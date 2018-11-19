# js-excercise
## Question-1
Write a function called "getLargestNumberAmongMixedElements". 
Given any array, "getLargestNumberAmongMixedElements" returns the largest number in the given array.
Notes:
* The array might contain values of a type other than numbers.
* If the array is empty, it should return 0.
* If the array contains no numbers, it should return 0.

var output = getLargestNumberAmongMixedElements([3, 'word', 5, 'up', 3, 1]);
console.log(output); // --> 5
```js
function getLargestNumberAmongMixedElements(arr) {
    // your code here
    var filteredArray = arr.filter(function (ele) {
        return typeof (ele) === 'number';
    });
    if (filteredArray.length > 0) {
        return filteredArray.reduce(function (a, v) {
            if (v > a) {
                return v;
            }
          else{
            return a;
          }
        });
    }
  else{
    return 0;
  }
}
```