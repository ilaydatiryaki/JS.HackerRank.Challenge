##### Objective

Today, we're discussing JavaScript functions. Check out the attached tutorial for more details.

##### Task

Implement a function named factorial that has one parameter: an integer, n. It must return the value of n!  (i.e., n factorial).

#### Input Format

Locked stub code in the editor reads a single integer, , from stdin and passes it to a function named factorial.

Constraints
1 ≤ n ≤ 10

#### Output Format

The function must return the value of n!.

#### Sample Input 0

4

#### Sample Output 0

24


```
'use strict';

process.stdin.resume();
process.stdin.setEncoding('utf-8');

let inputString = '';
let currentLine = 0;

process.stdin.on('data', inputStdin => {
    inputString += inputStdin;
});

process.stdin.on('end', _ => {
    inputString = inputString.trim().split('\n').map(string => {
        return string.trim();
    });
    
    main();    
});

function readLine() {
    return inputString[currentLine++];
}

/*
 * Create the function factorial here
 */

function factorial(n) {
    var fact=1;
    
    for (var i = n; i > 0; i--) {
        fact *= i;
        
    }
    
    return fact;    
}

function main() {
    const n = +(readLine());
    
    console.log(factorial(n));
}

```
