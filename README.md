Interview Questions
===================

This repo contails READMEs and solutions as well as 4 interview problems. Their basic problem statements are also below.

Please choose a problem that you feel comfortable with and that you think is appropriate for the candidate. 

Most of the solutions provided are more efficient than a naive or brute force solution, but the candidate may start with a brute force solution. Ask the candidate to run through some test cases to check that their solution works.

## Standard JS Questions
- Explain javascript closures
- Explain event bubbling
- Explain event delegation
- What does apply() do
- What does bind() do
- Explain what the js map function does provide an example
- What is strict mode
- Whats the difference between a promise and a callback

## Angular JS Questions

- What is scope
- What is a directive
- What is the link function in the directive
- What is the digest cycle (after I mentioned it in giving another answer)
- What is $scope.$apply
- What are the most commonly used out of the box directives
- What does transclude do on directives
- Tell me about a time you had problems with state in angular
- Have you ever had performance issues in angular and how did you tackle them
- What do you like about angular, what do you dislike about angular
- Why use a q promise as opposed to just returning $http’s promise
- What does $resource do

## General/Presentation Layer Questions

- What is a model in mvc
- Explain css specificity
- How do you centre something horizontally
- Explain what media queries are
- What are the pros and cons of a single page app
- How could you improve performance of a single page app
- Whats the difference between inline-block and inline
- How would you develop a mobile site for a website that didn’t already have one
- What is jsonp
- What is a doctype
- On a unix command line how would you run a long command you typed out already an hour ago
- What frontend tools do you normally use
- Where do you think ui’s are heading
- What motivates you, how do you learn

## JS Challenge Type Questions

- The first few the employer stole from You Can't JavaScript Under Pressure :)
- Write a function that takes an integer and returns it doubled
`function doubleInteger(i) {    
//your code here 
}`

- Write a function that takes a number and returns true if it's even and false if not
`function isNumberEven(i) {
// i will be an integer. Return true if it's even, and false if it isn't.
}`
- Write a function that returns a file extension
`function getFileExtension(i) {
   // i will be a string, but it may not have a file extension.
   // return the file extension (with no period) if it has one, otherwise false
}`
- What will be printed on the console? Why?
`( function( ) { var a = b = 5; } ) ( );
console.log(b);`
- Define a repeatify function on the String object. The function accepts an integer that specifies how many times the string has to be repeated. The function returns the string repeated the number of times specified.
For example:
`console.log('hello'.repeatify(3));
//Should print hellohellohello.`
- What will log out here?
`function test() {
console.log(a);
console.log(foo());
var a = 1;
function foo() {
return 2; } }
test();`
- What will log out here?
`var fullname = 'John Doe';
var obj = {
fullname: 'Colin Ihrig', 
prop: { 
fullname: 'Aurelio De Rosa',
getFullname: function( ) {
return this.fullname; } } };
console.log(obj.prop.getFullname());
var test = obj.prop.getFullname;
console.log(test()
);`
- Fix the previous question’s issue so that the last `console.log( )` prints Aurelio De Rosa.
- The following recursive code will cause a stack overflow if the array list is too large. How can you fix this and still retain the recursive pattern?
`var list = readHugeList();
var nextListItem = function() {
   var item = list.pop();
   if (item) {
// process the list item...
nextListItem( ) } 
};`
- What will alert out here:
`var a = 'value';
( function( ) {
alert(a);
var a = 'value2';
} ) ( );`
- The following code will output "my name is rex, Woof!" and then "my name is, Woof!" one second later, fix it so prints correctly the second time
`var Dog = function (name) {
this.name = name };
Dog.prototype.bark = function ( ) {
console.log('my name is '+ this.name + ', Woof!') }
var rex = new Dog('rex');
rex.bark();
setTimeout(rex.bark, 1000);`
- The following code outputs 100, a hundred times, fix it so it outputs every number with a 100ms delay between each
`for (var i = 0; i < 100; ++i) {
setTimeout(function() {
console.log(i);
}, 100) 
}`
- The following code is outputting the array but it's filled with every number, we just want the even numbers, - what's gone wrong?
`var evenNumbers = []
var findEvenNumbers = function (i) {
if (i % 2 === 0)
console.log(i, 'is an even number, adding to array!');
evenNumbers.push(i) }
for (var i = 0; i < 10; i++) {
findEvenNumbers(i) }
console.log(evenNumbers);
//outputs:
//0 "is an even number, adding to array!"
//2 "is an even number, adding to array!"
//4 "is an even number, adding to array!"
//6 "is an even number, adding to array!"
//8 "is an even number, adding to array!"
//[0, 1, 2, 3, 4, 5, 6, 7, 8, 9]`
- The following is outputting 0, but if 42 = 16 and 22 = 4 then the result should be 12
`var square = function (number) {
result = number * number;
return result }
result = square(4);
result2 = square(2);
difference = result - result2;
console.log(difference);`
- Write a function that when passed an array of numbers it gives you the max difference between the largest and smallest number ONLY if the small number is in front of the large number, not behind it, so for example: [3,4,8,1] = 5, notice how the biggest difference is between 8 and 1, but because the 1 is after the 8 in the array it shouldn't count, so really the biggest gap is the 3 and the 8.
fizzbuzz (lol)
- Presented with a html element with a border, and asked to animate it left to right - full width of browser
- Presented with another html box and asked to centre it both horizontally and vertically

## Rainy City

**Difficulty**: Medium-Hard    
**Concepts**: Looping and Arrays

You have an array of numbers representing the heights of buildings on a perfectly-packed city block.  Assuming infinite rain is available, how much rain water will collect on top of the roofs of the city block?

```
 __
|  |      __
|  |__   |  |
|     |__|  |
|           |
[4, 2, 1, 3]
```



## Choose Your Earliest Win

**Difficulty**: Hard    
**Concept**: Trees, Breadth First Search     
**Extension**: Directed Acyclic Graphs   

A choose your own adventure book is composed of chunks of a story.   The book gives readers a choice at the end of each chunk about what the main character in the story should do.  Each option sends the reader to a different page to read another chunk of the story that says what happens based on their decision.

```
...

What will you do?
To release the fairy from the jar, go to page 89.
To ask the fairy about the Sword of Truth, go to page 43.
To run back to the clearing, go to page 200.
```

Choose your own adventure books can usually either end happily, or end badly (with the main character's death/capture/etc).  Write a program to find the minimum number of decisions that could lead to a happy ending, in a choose your own adventure book. Assume that there is only one path to each ending.  Assume also that no story choices lead back to pages that have already been read.



**Bonus**: Sometimes authors do want to have two paths through the story converge. Modify your approach to let multiple paths lead to the same ending. Still assume that no story choices lead back to pages that have already been read.


## Smart Substring

**Difficulty**: Easy   
**Concepts**: Strings, Looping   
**Optional**: Regex   

Write a function that takes maximum 40 characters from a string, without breaking words.  

```
A star is a luminous sphere of plasma held together by its own gravity. The nearest star to Earth is the Sun. Other stars, mostly in the Milky Way, are visible from Earth during the night, appearing as a multitude of fixed luminous points in the sky due to their immense distance from Earth.
  - Wikipedia
```
First 40 characters: `"A star is a luminous sphere of plasma he"`.

Smarter approach: `"A star is a luminous sphere of plasma"`.




**Bonus**: Modify your function so that we can use shorthand to save characters, by replacing the word "and" with "&".





## Step Hop

**Difficulty**: Easy, then Harder   
**Concepts**: Recursion   
**Extension**: Dynamic Programming  

Sam loves to hop up stairs. Each time she moves up stairs, she either hops up one step, or hops up two steps.  For 4 stairs, two possible paths she might take are:


* ground, to first, to third, to fourth
```
                  __3__
              _2_|
          ___|
      _1_|
 ____|
```

* ground, to second, to fourth
```
                  __2__
              ___|
          _1_|
      ___|
 ____|
```

Write a function that, given a number of stairs, calculates how many ways Sam could possibly hop up that many stairs. 



**Bonus**: Sam has learned to hop 3 steps at a time (so, for example, she could go from the ground to the third step!).  Write a function to calculate how many ways Sam could hop up a given number of stairs with this new skill.
