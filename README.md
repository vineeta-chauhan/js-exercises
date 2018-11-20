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
## Question-2

Write a function called "getLongestWordOfMixedElements".

Given an array of mixed types, "getLongestWordOfMixedElements" returns the longest string in the given array.

Notes:
* If the array is empty, it should return an empty string (""). 
* If the array contains no strings; it should return an empty string.

var output = getLongestWordOfMixedElements([3, 'word', 5, 'up', 3, 1]);
console.log(output);
```js
function getLongestWordOfMixedElements(arr) {
    var filtredArray=[];
  for(var i=0;i<arr.length;i++){
    if(typeof(arr[i])==='string'){
      filtredArray.push(arr[i]);
    }
  }
   
    
      if(filtredArray.length>0){
        var longestWord = filtredArray[0];
        for (i = 1; i < filtredArray.length; i++) {
                if (filtredArray[i].length > longestWord.length) {
                    longestWord = filtredArray[i];
                }
        }
        return longestWord;
      }
  else{
    return "";
  }
    
}```
## question-3
Write a function called "convertScoreToGrade".

Given a score, "convertScoreToGrade" returns a string representing the letter grade corresponding to the given score.

Notes:
* (100 - 90) --> 'A'
* (89  - 80) --> 'B'
* (79  - 70) --> 'C'
* (69  - 60) --> 'D'
* (59  -  0) --> 'F'
* If the given score is greater than 100 or less than 0, it should return 'INVALID SCORE'.

var output = convertScoreToGrade(91);
console.log(output); // --> 'A'
