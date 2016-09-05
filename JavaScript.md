# JavaScript Reference

## Global functions
+ eval(string) function evaluates JavaScript code represented as a string.
  + Parameters: A string representing a JavaScript expression, statement, or sequence of statements. The expression can include variables and properties of existing objects.
  + Return value: A string representing the completion value of evaluating the given code. If the completion value is empty, undefined is returned.
+ isNaN(testValue) function determines whether a value is NaN or not.
    + Parameters: testValue
    + Return value: true if the given value is NaN; otherwise, false.
+ parseFloat(string) function parses a string argument and returns a floating point number.
    + Parameters: A string that represents the value you want to parse.
    + Return value: A floating point number parsed from the given string. If the first character cannot be converted to a number, NaN is returned.
+ parseInt(string, radix) function parses a string argument and returns an integer of the specified radix (the base in mathematical numeral systems).
    + Parameters: String - the value to parse. If string is not a string, then it is converted to a string. Radix - An integer between 2 and 36 that represents the radix (the base in mathematical numeral systems) of the above mentioned string.
    + Return value: An integer number parsed from the given string. If the first character cannot be converted to a number, NaN is returned.

***

## Number
+ numObj.toFixed([digits])
  + Parameters: digits (optional) - The number of digits to appear after the decimal point.
  + Return value: A string representing the given number using fixed-point notation.
+ numObj.toPrecision([precision])
  + Parameters: precision (optional) - an integer specifying the number of significant digits.
  + Return value: A string representing a Number object in fixed-point or exponential notation rounded to precision significant digits.
+ numObj.toString([radix])
  + Parameters: radix (optional) - an integer between 2 and 36 specifying the base to use for representing numeric values.
  + Return value: A string representing the specified Number object.

***

## Math
+ Math.PI
  + Ratio of the circumference of a circle to its diameter, approximately 3.14159.
+ Math.random()
  + Returns a pseudo-random number between 0 and 1.
  + Math.floor(Math.random()* y) + x returns a random number between x and y.
+ Math.floor(x)
  + Returns the largest integer less than or equal to a number.
+ Math.ceil(x)
  + Returns the smallest integer greater than or equal to a number.
+ Math.max([value1[, value2[, ...]]])
  + Returns the largest of zero or more numbers.
+ Math.min([value1[, value2[, ...]]])
  + Returns the smallest of zero or more numbers.
+ Math.round(x)
  + Returns the value of a number rounded to the nearest integer.
+ Math.pow(base, exponent)
  + Returns base to the exponent power, that is, base^exponent.
+ Math.sqrt(x)
  + Returns the sign of the x, indicating whether x is positive, negative or zero.
+ Math.abs(x)
  + Returns the absolute value of a number.

***

## String
+ str.length
    + Returns the length of a string.
+ str.charAt(index)
    + Returns the specified character from a string.
+ str.concat(string2[, string3, ..., stringN])
    + Combines the text of one or more strings and returns a new string.
+ str.includes(searchString[, position])
  + Determines whether one string may be found within another string.
+ str.indexOf(searchValue[, fromIndex])
  + Returns the index within the calling String object of the first occurrence of the specified value, or -1 if not found.
+ str.lastIndexOf(searchValue[, fromIndex])
  + Returns the index within the calling String object of the last occurrence of the specified value, or -1 if not found.
+ str.match(regexp)
  + Returns an Array containing the entire match result and any parentheses-captured matched results; null if there were no matches.
+ str.repeat(count)
  + Returns a string consisting of the elements of the object repeated the given times.
+ str.search(regexp)
  + Returns the index of the first match between the regular expression and the given string; if not found, -1.
+ str.slice(beginSlice[, endSlice])
  + Returns a new string containing the extracted section of the string.
+ str.split([separator[, limit]])
  + Returns an array of strings split at each point where the separator occurs in the given string.
+ str.toLowerCase()
  + Returns the calling string value converted to lower case.
+ str.toUpperCase()
  + Returns the calling string value converted to uppercase.

***

## Array
+ arr.length
  + Returns the number of elements in an array.

### Mutator methods - modify the array.
+ arr.pop()
  + Removes the last element from an array and returns that element.
+ arr.push(element1, ..., elementN)
  + Adds one or more elements to the end of an array and returns the new length of the array.
+ arr.reverse()
  + Reverses the order of the elements of an array in place — the first becomes the last, and the last becomes the first.
+ arr.shift()
  + Removes the first element from an array and returns that element.
+ arr.unshift([element1[, ...[, elementN]]])
  + Adds one or more elements to the front of an array and returns the new length of the array.
+ arr.sort([compareFunction])
  + Sorts the elements of an array in place and returns the array.
  + For numbers arr.sort(function(a, b) { return a - b; });
+ array.splice(start, deleteCount[, item1[, item2[, ...]]])
  + Returns an array containing the deleted elements.

### Accessor methods - do not modify the array and return some representation of the array.
+ var new_array = old_array.concat(value1[, value2[, ...[, valueN]]])
  + Returns a new array comprised of this array joined with other array(s) and/or value(s).
+ str = arr.join([separator = ','])
  + Joins all elements of an array into a string.
+ arr.slice([begin[, end]])
  + Extracts a section of an array and returns a new array.
+ arr.toString()
  + Returns a string representing the array and its elements.\
+ arr.indexOf(searchElement[, fromIndex = 0])
  + Returns the first (least) index of an element within the array equal to the specified value, or -1 if none is found.
+ arr.lastIndexOf(searchElement[, fromIndex = arr.length - 1])
  + Returns the last (greatest) index of an element within the array equal to the specified value, or -1 if none is found.

### Iteration methods
+ arr.forEach(callback[, thisArg])
  + Calls a function for each element in the array.
  + Callback parameters: currentValue, index, array.
  + Returns undefined.
+ arr.map(callback[, thisArg])
  + Creates a new array with the results of calling a provided function on every element in this array.
  + Callback parameters: currentValue, index, array.
+ arr.every(callback[, thisArg])
  + Returns true if every element in this array satisfies the provided testing function.
  + Callback parameters: currentValue, index, array.
+ arr.some(callback[, thisArg])
  + Returns true if at least one element in this array satisfies the provided testing function
  + Callback parameters: currentValue, index, array.
+ var new_array = arr.filter(callback[, thisArg])
  + Creates a new array with all of the elements of this array for which the provided filtering function returns true.
  + Callback parameters: currentValue, index, array.
+ arr.findIndex(callback[, thisArg])
  + Returns the found index in the array, if an element in the array satisfies the provided testing function or -1 if not found.
  + Callback parameters: currentValue, index, array.
+ arr.reduce(callback[, initialValue])
  + Apply a function against an accumulator and each value of the array (from left-to-right) as to reduce it to a single value.
  + Callback parameters: previousValue, currentValue, index, array.
+ arr.reduceRight(callback[, initialValue])
  + Apply a function against an accumulator and each value of the array (from right-to-left) as to reduce it to a single value.
  + Callback parameters: previousValue, currentValue, index, array.

***

## Control flow
+ Block - A block statement is used to group zero or more statements. The block is delimited by a pair of curly brackets.
+ break - Terminates the current loop, switch, or label statement and transfers program control to the statement following the terminated statement.
+ continue - Terminates execution of the statements in the current iteration of the current or labeled loop, and continues execution of the loop with the next iteration.
+ if...else - Executes a statement if a specified condition is true. If the condition is false, another statement can be executed.
+ switch - evaluates an expression, matching the expression's value to a case clause, and executes statements associated with that case.
```javascript
switch (expression) {
    case value1:
      //Statements executed when the result of expression matches value1
      [break;]
    case value2:
      //Statements executed when the result of expression matches value2
      [break;]
    ...
    case valueN:
      //Statements executed when the result of expression matches valueN
      [break;]
    default:
      //Statements executed when none of the values match the value of the expression
      [break;]
}
```

***

## Declarations
+ var - Declares a variable, optionally initializing it to a value.
+ let - Declares a block scope local variable, optionally initializing it to a value.
+ const - Declares a read-only named constant.

***

## Iterations
+ do...while statement creates a loop that executes a specified statement until the test condition evaluates to false. The condition is evaluated after executing the statement, resulting in the specified statement executing at least once.
```javaScript
do
    statement
while (condition);
```
+ for statement creates a loop that consists of three optional expressions, enclosed in parentheses and separated by semicolons, followed by a statement (usually a block statement) to be executed in the loop.
```javaScript
for ([initialization]; [condition]; [final-expression])
    statement
   ```
+ for...in statement iterates over the enumerable properties of an object, in arbitrary order. For each distinct property, statements can be executed.
```javaScript
for (variable in object) {...
}
```
+ for...of statement creates a loop iterating over iterable objects (including Array, Map, Set, String, TypedArray, arguments object and so on), invoking a custom iteration hook with statements to be executed for the value of each distinct property.
```javaScript
for (variable of iterable) {
    statement
}
```
+ while statement creates a loop that executes a specified statement as long as the test condition evaluates to true. The condition is evaluated before executing the statement.
```javascript
while (condition) {
    statement
}
```

***

+ A closure is a special kind of object that combines two things: a function, and the environment in which that function was created. The environment consists of any local variables that were in-scope at the time that the closure was created.

```javascript
function adder(x) {
  return function(y) {
    return x + y;
  };
}
let add5 = adder(5);
```

+ Encapsulation - ability of an object to be a container (or capsule) for its member properties, including variables and methods
  + fundamental principle of object oriented programming

```javascript
  function Person() {
    //properties/fields
    var name = "Travis";
    var age = 30;

    //methods/actions
    this.setName = function(newName) {name=newName;}
    this.getName   = function() { return name; }
    this.setAge = function(newAge) { age=newAge; }
    this.getAge = function() { return age; }

    return this;
  }
  let me = new Person();
  let myName = me.name;  //this no longer works
  let myName = me.getName();  //this does

// - or -
 let person = (function () {

   let fullName = "Travis Shields";

   return {
     setName : function (newValue) {
         fullName = newValue;
     },
     getFullName : function () {
      return fullName;
     }
   }; // end of the return
 }());
 console.log(person.getFullName());
 console.log(person.setName("Steven"));
 console.log(person.getFullName());
```
