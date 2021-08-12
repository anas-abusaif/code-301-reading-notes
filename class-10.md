# Understanding the JavaScript Call Stack
## 1.What is a ‘call’?
When a function is invoked (called), the function, its parameters, and variables are pushed into the call stack to form a stack frame.
## 2.How many ‘calls’ can happen at once?
one at a time
## 3.What does LIFO mean?
last in first out
## 4.Draw an example of a call stack and the functions that would need to be invoked to generate that call stack.
![https://res.cloudinary.com/practicaldev/image/fetch/s--LqQZAZPH--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/piahcfqczl77rulnqejf.png](https://res.cloudinary.com/practicaldev/image/fetch/s--LqQZAZPH--/c_limit%2Cf_auto%2Cfl_progressive%2Cq_auto%2Cw_880/https://thepracticaldev.s3.amazonaws.com/i/piahcfqczl77rulnqejf.png)
## 5.What causes a Stack Overflow?
A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. 
<hr>

# JavaScript error messages
## 1.What is a ‘refrence error’?
This is as simple as when you try to use a variable that is not yet declared you get this type os errors.
## 2.What is a ‘syntax error’?
this occurs when you have something that cannot be parsed in terms of syntax
## 3.What is a ‘range error’?
Trying to manipulate an object with some kind of length and give it an invalid length and this kind of errors will show up.
## 4.What is a ‘tyep error’?
 this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable.
 ## 5.What is a breakpoint?
 will make your program stop at that point only if a condition is met
 ## 6.What does the word ‘debugger’ do in your code?
 putting a breakpoint