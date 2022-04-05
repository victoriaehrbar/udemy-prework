Question #1 Google Interview Question Two Sum (Easy)

Given an array of intergers, return the indices of the 2 numbers that add up to a given target
array = [1, 3, 7, 9, 2] 
target = 11


Rules:
-No duplicates
-Just positive numbers
-Not always a solution
-Return null when there is no solution
-Just 1 pair of numbers


How to solve:
-Ensure there is a pair that adds up to target (two pointer technique)
-p1 is the number you are testing, p2 is the number you are testing it against
-numberToFind = target - array[p1]


```
const findTwoSum = (array, target) => {
    for (let P1 = 0; P1 < array.length; P1++) {
        const numberToFind = target - array[P1];

    for(let P2 = P1 + 1; P2 < array.length; P2++) { //p1 + 1 to show one position to right
        if(numberToFind === array[P2]){ //verify if current number is value at p2
        return[P1, P2]; //display the two numbers from the array
           
        }
    }
}
return null; //part of rules to return null if no solution exists
};
```