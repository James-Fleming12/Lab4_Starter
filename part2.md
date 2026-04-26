1. Line 12 will print the value 3. Since the iteration variable `i` is defined with `var`, it exist outside of the scope of the loop.
2. Line 14 will print out 150 since that's the final state of `discountedPrice`. Since the variable is defined with `var`, it exists outside of the scope of the loop.
3. Line 13 will print out 150 since that's the final state of `finalPrice`, which is defined within the same scope as the print.
4. The function will return `[50, 100, 150]` since we applying a 50% discount, and the rounding done in `finalPrice` does not affect the cases here since they all lead to whole numbers.
5. The code causes an error. Since the iteration variable `i` is defined with `let`, it only exists within the scope of the loop, so no variable named `i` exists for the print.
6. The code causes an error. Since `discountedPrice` is defined with `let`, it only exists within the scope of the loop, so no variable named `i` exists for the print.
7. The code prints out 150 since that's the final state of `finalPrice`. Even though `finalPrice` is defined with `let`, it's defined within the same block as the print statement so it exists for the print.
8. The code will return the same output of `[50, 100, 150]`. Since both `i` and `discountedPrice` have no interactions outside of the loop, the difference between `let` and `var` changes nothing as long as the prints are commented out.
9. An error will occur for the same reason as in question 5, since `i` is defined with `let` again.
10. Line 12 will print `3` since the declaration using `const` doesn't change the behavior of printing that it did with `var` or `let` since `length` is defined within the same block as the print.
11. The code will return the same output of `[50, 100, 150]` since the removal of the rounding step and storing the length used in the loop in a variable don't change the behavior of the function (with the removal of the rounding step not changing the behavior being specific to our case of nicely defined values and discounts).
12a. `student.name`
12b. `student["Grad Year"]`
12c. `student.greetings()`
12d. `student["Favorite Teacher"].name`
12e. `student.courseLoad[0]`
13a. `"32"`, since when `+` is used with a string it performs string concatenation, and the number `2` is coerced into a string `"2"`.
13b. `1`. The `-` operator does not have an associated operation with strings, so `"3"` is coerced into the number `3` to perform mathematical subtraction.
13c. `3`, since in numeric operations `null` is coerced to the value `0`.
13d. `"3null"` since in string operations `null` is coerced to the string `"null"`.
13e. `4`, since in numeric operations `true` is coerced to the value `1`.
13f. `0`, since `false` and `null` are coerced to `0` in numerica operations.
13g. `"3undefined"` since in string operations `undefined` is concatenated to the string `"undefined"`.
13h. `NaN` since numeric coercion is attempted for the same reason as in 13b, `undefined` is coerced into `NaN`, and any operations with `NaN` result in `NaN`.
14a. `true`, since when comparing a string to a number the string is converted to a number.
14b. `false`, since when comparing two strings, the lexicographical order is used.
14c. `true`, since loose equality `==` is used the datatypes do not matter, only the values when coerced.
14d. `false`, since strict equality `===` is used the datatypes need to match as well.
14e. `true`, since `Boolean(2)` evaluates to `true` since `2` is a truthy value.
15. The `==` (loose equality) operator checks for equality after performing type coercion, and `===` (strict equality) operator checks for equality in both value and type.
16. Contained in `part2-question16.js`
17. The function will return `[2, 4, 6]` since at each iteration of the loop, we're taking the value of the input array `array` and calling `callback` on it, which in our case is the function `doSomething` which double the value, and adding it to the result array.
18. Contained in `part2-question18.js`
19. The outputs printed in order are `1`, `4`, `3`, and `2`. The `3` and `2` are printed last since all synchronous code has to finish in the call stack until asynchronous code can be handled, and the timeout on `2` causes it to print after `3`.