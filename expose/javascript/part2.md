1. pritns 3
I is declared as a var hence it is assessible outside the for loop and remains available anywhere in the function. After loop, i is 3

2. the program wil print the currentvalue of discountePrice(150), there is no error on the code itself(idk about logic) as discountedPrice is declared as var. 

3.This will not cause an error, and it will log 150 . FinalPrice is declared with var on line 4, outside the loop. Due to var's function scope 7, it remains accessible anywhere within discountPricesincluding line 14 after the loop ends.Each iteration overwrites finalPrice with the latest discounted value and we end up with 150

4. Returns:[50, 100, 150]
The function applies a 50% discount (1 - 0.5 = 0.5) to each price in [100, 200, 300], rounds each result to 2 decimal places, and pushes it into the discounted array:

100 * 0.5 = 50
200 * 0.5 = 100
300 * 0.5 = 150

The Math.round(x * 100) / 100 step is for precisio and the final array is returned on line 16.

5. At line 12,the code will print the loop index i to the console on every iteration.
In the for loop , i is declared with let. Because i is block scoped within the loop, line 12 is inside the loop body, so i is defined and usable there.
With the example call discountPrices([100, 200, 300], 0.5), it will log:0,1,2

6. will throw error:discountedPrice is not defined
discountedPrice is declared with let on line  7,inside the for loophence it only exists within that loop's curly braces and is destroyed after each iteration ends.line 13 is outside the loop hence why error is thrown.

7. the code will print finalPrice exactly once after the loop finishes.
finalPrice is declared before the for loop with let and inside the loop, finalPrice gets reassigned every iteration.
Because line 14 is outside the loop, it runs after the loop ends, so finalPrice will be the value computed on the last iteration

8. [50, 100, 150]
All three console.log lines (12–14) are commented out, so no errors occur. The logic runs cleanly through the loop, and the function returns the same discounted array as before.
The use of let instead of var doesn't matter here because discountedPrice is only ever accessed inside the loop where it's declared.

9. will throw error:i is not defined
i is declared with let in the for loop header on line 6.Line 11 is outside the loop, so i is out of scope by the time it's reached, causing a refernce error. 

10.prints 3 with no error.
length is declared with const on line 4, inside the function body but outside the loop. it's accessible anywhere within the function, including line 12.
length was assigned prices.length, and since the input has 3 elements, it holds the value 3. 

11. returns [50, 100, 150].
The function loops through each price and multiplies it by (1 - 0.5) = 0.5, then pushes the result into the discounted array.No errors in code.

12. 
A. `student.name`
B. `student['Grad Year']`
C.`student.greeting()`
D. `student['Favorite Teacher'].name`
E.  `student.courseLoad[0]`

13.

A `'3' + 2`  
Output: `'32'`  
 `+` with a string does string concatenation

B. `'3' - 2`  
Output: `1`  
Why: `-` forces numeric conversion, so `'3'` becomes `3`.

C. `3 + null`  
Output: `3`  
Why: `null` converts to `0` in numeric addition.

D. `'3' + null`  
Output: `'3null'`  
Why: string concatenation; `null` converts to `'null'`.

E. `true + 3`  
Output: `4`  
Why: `true` converts to `1`.

F. `false + null`  
Output: `0`  
Why: `false` converts to `0`, and `null` converts to `0`.

G. `'3' + undefined`  
Output: `'3undefined'`  
Why: string concatenation; `undefined` converts to `'undefined'`.

H. `'3' - undefined`  
Output: `NaN`  
Why: `-` tries numeric conversion; `undefined` becomes `NaN`.

14.

A. `'2' > 1`  
Output: `true`  
Why: `'2'` converts to number `2`, and `2 > 1`.

B. `'2' < '12'`  
Output: `false`  
Why: both are strings, so JS does lexicographic comparison; `'2'` is greater than `'1'`.

C. `2 == '2'`  
Output: `true`  
Why: `==` allows type coercion; `'2'` is converted to `2`.

D. `2 === '2'`  
Output: `false`  
Why: `===` checks value and type; number and string are different types.

E. `true == 2`  
Output: `false`  
Why: `true` converts to `1`, then `1 == 2` is false.

F. `true === Boolean(2)`  
Output: `true`  
Why: `Boolean(2)` is `true`; both value and type are boolean `true`.

15. `==` compares after implicit type conversion, while `===` compares without conversion (type and value must both match).

17. modifyArray  returns `[2, 4, 6]`.
The function creates `newArr = []`, then for each element it calls the callback: `doSomething(1)=2`, `doSomething(2)=4`, `doSomething(3)=6`, pushes those into `newArr`, and finally returns `newArr`.

19.The output will be:
Lines 2 and 5 are synchronous so they run first in order, printing 1 then 4. The two setTimeout calls are asynchronous, so their callbacks are sent to the callback queue and only run after the main call stack is empty. The setTimeout with 0ms delay (prints 3) runs before the one with 1000ms delay (prints 2).