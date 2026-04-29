1. prints : values added:20

since add is true the fi statment is executed. Result is set to 0 on line 5 then assigned 10+10=20 on line 7 so values added: 20 is the outpput.

2. final result:20
Since add was true the else return on line 11 is skipped so program skips to line 13. Result is still 20 in that scope hence why it is printed.

3. Var ignores block statments like if for or while hence it can cause bugs. you can refrence var variable before declaration wihtout an error, makign bugs hard to track.You can declare same var variable twice in same scope without error,this will  overwrite values

4. values added:20
same as before.let being block scoped dosent affect anything inside the block.

5. thorws error:result not defined
since result is declared with let inside the if block, it cant exist outside that scope hence result no longer exitsts in line 13, makign the system throw an error.

6. system throws an error  to constant variable on line 7, before line 9 is ever reached.
That reassignment is illegal with const, so the engine throws a TypeError and execution stops hence line 9 never runs.

7. Nothing, line 13 is never reached either.
The error on line 7 stopped execution entirely, so neither line 9 nor line 13 produce any output.
