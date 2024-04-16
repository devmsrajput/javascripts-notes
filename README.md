# javascripts-notes

```javascript

// VAR vs LET: VAR is older(ECMA SCRIPT 5) JavaScript variable delaration method, in VAR there's no specific scope for variable. While let allows to declare variales scope wise.

"use strict"; // Treats all code as newer version of JS.

// alert(3 + 3) We are using Nodejs, not browser.

// console.log(3 + 3);

// Data types:
// number: 2 to power 53
// bigint
// string => ""
// boolean => true/false
// null => standalone value or empty value.
// undefined => declared variable but not defined yet.
// symbol => unique

//object

// console.log(typeof "Age")
// console.log(typeof NaN); // NaN is also a number type.
// console.log(typeof null) // Null is of object type.
// console.log(typeof undefined); // Undefined itself is a type.
// console.log("Code runner");

// let score = "37abc"

// console.log(typeof score);
// console.log(typeof(score));

// let valueInNumber = Number(score);
// console.log(typeof valueInNumber);
// console.log(valueInNumber); // NaN

// ********************CONVERSIONS********************
// IN NUMBER CONVERSION:
// "33" => 33
// "33abc" / undefined => NaN
// true => 1; false and null => 0;

// let num = Number(null)
// console.log(num)

// IN BOOLEAN CONVERSION:
// let someBool = Boolean(1)
// 1 => true;
// "" => false;
// "Demo" => true;

// IN STRING CONVERSION:
// let someNumber = 33;
// let stringNumber = String(someNumber);
// console.log(typeof stringNumber) // It gives string type.

// ************************OPERATIONS********************

// let value = 3;
// let negValue = -value;
// console.log(negValue); // Gives negative value.

// let str1 = "John";
// let str2 = " Doe";
// let str3 = str1 + str2;
// console.log(str3); // Output: John Doe.

// console.log("1" + 2); // Output => 12
// console.log(1 + "2"); // Output => 12
// console.log("1" + 2 + 2); // Output => 122
// console.log(1 + 2 + "2"); // Output => 32

// console.log(+true); // Output => 1
// console.log(+""); // Output => 0
// let num = '10'
// console.log(typeof num) // string
// console.log(typeof +num) // number

// let num1, num2, num3;
// num1 = num2 = num3 = 2 + 2; // This is not a good way to assign.

// let gameCounter = 100;
// ++gameCounter;
// console.log(gameCounter); // 101

// console.log(null > 0); // Comparision operators converts null into zero. false
// console.log(null == 0); // Equality check operator is different from comparison operators, it doesnt convert null into zero. false
// console.log(null >= 0); // Comparision operators converts null into zero. true
// console.log(false == '0')
// console.log(null == '0')

// console.log(undefined < 0); // false
// console.log(undefined > 0); // false
// console.log(undefined == 0); // false
// console.log(undefined >= 0); // false
// console.log('a' < 'A') // false, a is greater than A

// Comparison operators are different from Equility check operators.

// == / ===
// In Double Equality check(==) it just checks values but Triple Equality checks checks through Data Types as well.

// DATA TYPES:
// 1. Primitive Data Types
// 2. Non Primitive Data Types

// 1. Primitive Data Types(Call by value): There are 7 basic primitive data types, primitive data types are termed as call by value data types. In Call By Value(Primitive Data Types) we don't get value reference but a copy of that value, and when we make any change, it doesn't change original value but reflects changes to the copies of that value only.

// Following is types:
// 1 String
// 2 Number
// 3 Boolean
// 4 null
// 5 undefined
// 6 Symbol => This is used to make any component unique in all.
// 7 BigInt

// 2. Non Primitive Data Types(Reference types): When we do manipulations in Reference(Non Primitive Data Types), it directly allocates the reference to the memory.
// Following are the types:
// 1 Array
// 2 Objects
// 3 Functions

// JavaScript is Dynamically Typed language.

// Symbols
// const id = Symbol('123');
// const anotherId = Symbol('123');
// console.log(id == anotherId); // Output => false, Symbols are used for it's uniquiness, it guranttes the value uniquiness.

// BigInt:
// const bigNumber = 826493643647346181663437n; // To convert any number into BigInt, just add 'n' at last.
// console.log(typeof bigNumber); // Data type is BigInt.

// Data types from checking typeof:

// Undefined => "undefined"
// Null => "object"
// Boolean => "boolean"
// Number => "number"
// String => "string"
// Object => "object"
// Function => "object-function"
// Symbol => "symbol"

// Primitive Data Types gets allocate in STACK memory and on assigning it to other variables we just get their copies. But in case of Non Primitive Data Types it gets allocate in HEAP memory, on assigning one object or any other entity into another, we directly get same reference, so on manipulating in any of them changes reflects in both.

// Primitive Data Types => STACK Memory
// Non-Primitive Data Types => HEAP Memory

// String Interpolation:
// const langName = "JavaScript";
// console.log(`Language: ${langName}`);

// OTHER WAYS TO DECLARE STRING:
// const gameName = new String("pubg-game");

// anchor: ƒ anchor()
// at: ƒ at()
// big: ƒ big()
// blink: ƒ blink()
// bold: ƒ bold()
// charAt: ƒ charAt()
// charCodeAt: ƒ charCodeAt()
// codePointAt: ƒ codePointAt()
// concat: ƒ concat()
// constructor: ƒ String()
// endsWith: ƒ endsWith()
// fixed: ƒ fixed()
// fontcolor: ƒ fontcolor()
// fontsize: ƒ fontsize()
// includes: ƒ includes()
// indexOf: ƒ indexOf()
// isWellFormed: ƒ isWellFormed()
// italics: ƒ italics()
// lastIndexOf: ƒ lastIndexOf()
// length: 0
// link: ƒ link()
// localeCompare: ƒ localeCompare()
// match: ƒ match()
// matchAll: ƒ matchAll()
// normalize: ƒ normalize()
// padEnd: ƒ padEnd()
// padStart: ƒ padStart()
// repeat: ƒ repeat()
// replace: ƒ replace()
// replaceAll: ƒ replaceAll()
// search: ƒ search()
// slice: ƒ slice()
// small: ƒ small()
// split: ƒ split()
// startsWith: ƒ startsWith()
// strike: ƒ strike()
// sub: ƒ sub()
// substr: ƒ substr()
// substring: ƒ substring()
// sup: ƒ sup()
// toLocaleLowerCase: ƒ toLocaleLowerCase()
// toLocaleUpperCase: ƒ toLocaleUpperCase()
// toLowerCase: ƒ toLowerCase()
// toString: ƒ toString()
// toUpperCase: ƒ toUpperCase()
// toWellFormed: ƒ toWellFormed()
// trim: ƒ trim()
// trimEnd: ƒ trimEnd()
// trimLeft: ƒ trimStart()
// trimRight: ƒ trimEnd()
// trimStart: ƒ trimStart()
// valueOf: ƒ valueOf()
// Symbol(Symbol.iterator): ƒ [Symbol.iterator]()

// console.log(gameName.toUpperCase());
// console.log(gameName);

// console.log(gameName.charAt(2)); // Output => b
// console.log(gameName.indexOf('g')); // Output => 3

// const newString = gameName.substring(0, 3); // It doesn't obey negative indexes.
// console.log(newString);

// const anotherString = gameName.slice(-8, 4); // It obeys negative indexes.
// console.log(anotherString);

// const newString = "    PUBG        ";
// console.log(newString);
// console.log(newString.trim());

// const URL = "https://www.google.com/google%20docs";
// console.log(URL.replace('%20', '-'));
// console.log(URL.includes("google")); // It checks either this word present in the string object or not - true

// const newString = "PLAYER-UNKNOWN-BATTLEGROUNDS";
// console.log(newString.split('-'));

// MATHS:
// console.log(Math); // Object [Math] {}
// console.log(Math.abs(-5)); // Returns Absolute value => 5
// console.log(Math.round(4.6)); // Returns round value => 5
// console.log(Math.ceil(4.2)); // 5
// console.log(Math.floor(4.9)); // 4
// console.log(Math.min(4, 3, 6, 8)); // 3
// console.log(Math.max(4, 3, 6, 8)); // 8
// console.log((Math.random()*10) + 1)

// const min = 1;
// const max = 6;

// console.log(Math.floor(Math.random() * (max - min + 1) + min));

// TIME & DATES:
// let myDate = new Date();
// console.log(myDate); // 2024-02-08T12:20:37.776Z
// console.log(myDate.toString()); // Thu Feb 08 2024 17:53:46 GMT+0530 (India Standard Time)
// console.log(myDate.toLocaleString()) // 8/2/2024, 5:52:04 pm
// console.log(myDate.toLocaleDateString()); // 8/2/2024
// console.log(myDate.toDateString()) // Thu Feb 08 2024

// let createNewDate = new Date(2023, 0, 23); // Months start from 0;
// console.log(createNewDate.toDateString()); // Output => Mon Jan 23 2023

// Array:
const arr = [4, 3, 6, 8];
// const heroes = ["Shaktiman", "Nagraj", ];

// const newArr = new Array(1, 2, 3, 4);

// Array Method:
// console.log(arr);

// arr.push(9); // Add at last index of array.
// console.log(arr);

// arr.pop() // Eliminate one element from last index.
// console.log(arr);

// arr.unshift(5); // Adds at first index of array, from optimization point of view, this method is not recommended because it shifts up total elements from 1 index.
// console.log(arr);

// arr.shift() // It eliminates first index element from array, not good from optimization point of view.
// console.log(arr);

// console.log(arr.includes(9)); // Output => false
// console.log(arr.indexOf(4)); // Output => 1, if it returns -1, that means that index value doesn't exist in array. It takes string or value.

// console.log(arr); // Output => [ 4, 3, 6, 8 ]
// console.log(typeof arr); // Output=> object
// const newArr = arr.join();
// console.log(newArr); // Output => 4,3,6,8
// console.log(typeof newArr); // Output => string

// Slice, Splice:
// console.log("MAIN", arr);
// const myn1 = arr.slice(1, 3); // It'll return array element from the given starting index and would not consider last index.
// console.log("B", myn1);
// console.log("MAIN", arr);

// const myn2 = arr.splice(1, 3);
// console.log("C", myn2);
// console.log("MAIN", arr);

// SUMMARY: Slice doesn't effect original array, but Splice directly changes the original array.

// Arrays Merging:

// const marvel_heros = ["Thor", "Ironman", "Spiderman"];
// const dc_heros = ["Superman", "Flash", "Batman"];

// Push() not recommended for array merging.

// 1st way to merge array:
// const all_heros = marvel_heros.concat(dc_heros);
// console.log(all_heros);

// 2nd way to merge array(by using spread operator):
// const all_heros = [...marvel_heros, ...dc_heros]; // This is preferably more convinient and good way to merge array.
// console.log(all_heros);

// const another_array = [1, 2, 3, [4, 5, 6], 7, [8, 9, [4, 5]]];
// const real_another_array = another_array.flat(Infinity);
// console.log(another_array); // Output => [ 1, 2, 3, [ 4, 5, 6 ], 7, [ 8, 9, [ 4, 5 ] ] ]
// console.log(real_another_array); // Output => [1, 2, 3, 4, 5, 6, 7, 8, 9, 4, 5]

// console.log(Array.isArray("PUBG")); // Returns Boolean value, Output => false.
// console.log(Array.from("PUBG")); // Iterable strings are easily converted into Array. Output => [ 'P', 'U', 'B', 'G' ]
// console.log(Array.from({name: "PUBG"})); // Here it doesn't get converted into Array. Output => []

// let score1 = 100;
// let score2 = 200;
// let score3 = 300;
// console.log(Array.of(score1, score2, score3));

// let obj1 = {
//   model: "Samsung",
//   price: 5000
// }
// let obj2 = {
//   model: "Motrola",
//   price: 8000
// }
// let obj3 = {
//   model: "Nokia",
//   price: 5000
// }
// Practice
// const newArr = Array.of(obj1, obj2, obj3);
// newArr.map((item) => {
//   console.log(`${item.model}: ${item.price}`);
// })
// const totalPrice = newArr.reduce((accumulator, currentValue) => accumulator + currentValue.price, 0);
// console.log(totalPrice); // Output => 18000


// Objects: Objects are defined in two ways:
// 1 Object literals // It never forms Singleton Object.
// Eg. const userData = {first_name: "John", last_name: "Doe"};
// 2 Object Constructor // When we define Object through Constructor, it always forms Singleton Object.
// Eg. Object.create()


// const mySym = Symbol("key1");
// const User = {
//   name: "John",
//   "full name": "John Doe",
//   age: 18,
//   location: "Jaipur",
//   email: "john@doe.com",
//   isLoggedIn: false,
//   lastLoggedIn: ["Monday", "Saturday"],
//   [mySym]: "mykey1", // A symbol only can be accessed as a Symbol when enclosed within Square Brackets.
// };

// console.log(User.name);
// console.log(User["email"]);
// console.log(User["full name"]);
// console.log(User.mySym);
// console.log(typeof User.mySym); // Without quoting into Square brackets, we can't access Symbol. Output => undefined
// console.log(typeof User[mySym]); // Output => string
// console.log(User[mySym]);

// User.email = "johndoe@google.com";
// Object.freeze(User);
// User.email = "google@com";
// console.log(User);

// User.greeting = function() {
//     console.log("Hello JS user.");
// }

// console.log(User.greeting());

// User.greeting2 = function() {
//     console.log(`Hi ${this["full name"]}`)
// }

// console.log(User.greeting2());

// const regularUser = {
//     first_name: "John",
//     last_name: "Doe",
//     fullname: function(){
//         return this.first_name + ' ' + this.last_name;
//     }
// }

// console.log(regularUser.fullname());

// Merging of Arrays:
// const obj1 = {1: "a", 2: "b"}
// const obj2 = {3: "a", 4: "b"}
// const allObj = Object.assign({}, obj1, obj2); // Assign takes two parameter, first one is target parameter in which we have to assign the values, second one is source from which values will be assigned.
// const allObj = {...obj1, ...obj2} // This way is more convinient and recomended to use.
// console.log(allObj);

// const userData = [
//   {
//     name: "John Doe",
//     age: 21,
//     city: "Delhi",
//   },
//   {
//     name: "Rahul",
//     age: 23,
//     city: "Agra",
//   },
//   {
//     name: "Sumit",
//     age: 22,
//     city: "Dhanbad",
//   },
// ];

// const regularUser = {
//   first_name: "John",
//   last_name: "Doe",
// };

// console.log(Object.keys(regularUser)); // Output => [ 'first_name', 'last_name' ]
// console.log(Object.values(regularUser)); // Output => [ 'John', 'Doe' ]
// console.log(Object.entries(regularUser)); // Output => [ [ 'first_name', 'John' ], [ 'last_name', 'Doe' ] ]

// We can ask an Object regarding a property:
// console.log(regularUser.hasOwnProperty('first_name')); // Output => true

// Object Destructuring:
// const course = {
//   coursename: "JavaScript",
//   price: 999,
//   courseInstructor: "YT"
// }

// const {courseInstructor} = course;

// console.log(courseInstructor);

// Functions:
// function addTwoNumbers(num1, num2) {
//   console.log(num1 + num2);
// }

// function addTwoNumbers(num1, num2) {
//   return (num1 + num2);
// }

// const result = addTwoNumbers(2, 5);
// console.log(result);

// function loginMessage (username = "Unknown") {
//   return `${username} is just logged in.`
// }

// console.log(loginMessage("Demo"));

// Rest Operator:
// function calculateCartPrice (...prices) {
//   return prices;
// }

// console.log(calculateCartPrice(200, 300, 500)); // Output => [ 200, 300, 500 ]

// Passing Object as function parameter:
// const user = {
//   username: "John",
//   price: 199
// }

// function handleObject (anyObject) {
//   console.log(`Username is ${anyObject.username} and price is ${anyObject.price}`);
// }

// handleObject(user);
// Similarly, we can pass arrays as well.

// if (true) {
//   let a = 10;
//   const b = 20;
//   var c = 30;
// }

// console.log(a);
// console.log(b);
// console.log(c);

// Hoisting:

// console.log(addOne(5));
// function addOne (num) { // If we declare function in this way, we may call before it's initialisation. This Hoisting feature of Function.
//   return num + 1;
// }

// // console.log(addTwo(5)); // It'll throw an error.
// const addTwo = function (num) { // "addTwo" is called as expression of function. Dunctions which get declared through a expression can't be accessed before initialisation. This is called Hoisting.
//   return num + 2;
// }

// THIS and ARROW function:

// THIS: We dont use THIS in arrow function, but we can use in functions which are declared in other ways. THIS just refers the one scope above variables, objects, etc anything that lies.

// If we check THIS in node environment globally, it returns empty object but in browser console we get Window objects or methods.

// Arrow
// const addOne = (num) => { // This simple declaration of Arrow function.
//   return num + 1;
// }

// const addOne = (num) => num + 1; // This is implicite declaration of Arrow function in one line, where function returns the value by default. For the extra safty we can wrap our code in paranthesis, especially in case when we'll be returning an Object. Below is an example.
// const addTwo = () => ({username: "John"});

// console.log(addTwo(5));

// Immediately Invoked Functions Expression: We use IIFE to avoid global scope pollutions. In certain cases we encounter issues cause of global scope's variable declarations, to avoid such issues we prefer to use IIFE.
// (function IIFE () { // Declaration IIFE in simple function.
//   console.log(`DB Connected.`);
// }())

// (function IIFE () { // Declaration IIFE in simple function.
//   // We call it named IIFE
//   console.log(`DB Connected.`);
// }()); // In case of IIFE declaration, we must have to put semi-colon at the end of the function, otherwise it'll give error on next function declaration because it would not understand where it has to end.

// ((username)=>{
//   // Unammed IIFE
//   console.log(`DB Connected2 ${username}.`);
// })("Demi");

// Switch Case Statements:
// const month = 5;
// switch(month) {
//   case 1:
//     console.log("Jan");
//     break;
//   case 2:
//     console.log("Feb");
//     break;
//   case 3:
//     console.log("Mar");
//     break;
//   case 4:
//     console.log("Apr");
//     break;
//   case 5:
//     console.log("May");
//     break;
//   case 6:
//     console.log("Jun");
//     break;
//   case 7:
//     console.log("Jul");
//     break;

//   default:
//     console.log("This month not valid");
// }

// TRUTHY AND FALSY VALUES:
// Truthy values: true, "0", 'false', " ", [], {}, function(){}
// Falsy values: false, 0, -0, BigInt, "", null, undefined, NaN

// Nullish Coalescing Operator (??): null / undefined
// const val1 = null ?? 10;
// console.log(val1);

// Terniary Operator: condition ? true : false
// const iceTeaPrice = 100;
// iceTeaPrice <= 80 ? console.log("Less than 80.") : console.log("More than 80.");

// Control statements: IF ELSE / SWITCH

// LOOPS:
// const arr = [];
// for(let i = 0; i <= 5; i++) {
//   const elm = i;
//   arr.push(elm);
// }
// console.log(arr); // Output => [ 0, 1, 2, 3, 4, 5 ]

// Printing Table:
// for(let i = 1; i <= 10; i++) {
//   for(let j = 1; j <= 10; j++) {
//     console.log(`${i} x ${j} = ${i * j}`);
//   }
//   console.log("\n")
// }

// While:
// let i = 0;
// const heros = ["Superman", "Batman", "Spiderman"];
// console.log(heros.length);
// while (i < heros.length) {
//   console.log(heros[i]);
//   i++;
// }

// Do While:
// let score = 1;
// do {
//   console.log(`Score is ${score}`);
//   score++;
// } while (score <= 10);

// Higher Order Array Loops:

// For Of Loop: Applicable on Arrays and Maps
// const arr = [1, 2, 3, 4, 5];
// for (const value of arr) {
//   console.log(value);
// }

// Map
// const map = new Map();
// map.set("IN", "India");
// map.set("USA", "United States Of America");
// map.set("FR", "France");
// // console.log(map);
// for(let [key, value] of map) {
//   console.log(`${key}: ${value}`);
// }

// For In Loop: Good for objects, we can iterate arrays but it'll give keys of array not the value. Map is not iteratable object, so we can not use Map in For in loop.

// For Each: It's callback function, always takes callback as input.
// const coding = ["js", "ruby", "java", "python"];
// coding.forEach (function (item) {
//   console.log(item);
// })

// coding.forEach ((item) => {
//   console.log(item);
// })

// function printMe (item) {
//   console.log(item);
// }
// coding.forEach(printMe);

// coding.forEach((item, index, arr) => {
//   console.log(item, index, arr);
// })

// const mobiles = [
//   {
//     brand: "Samsung",
//     price: 5000,
//   },
//   {
//     brand: "Intex",
//     price: 4000,
//   },
//   {
//     brand: "Xiaomi",
//     price: 3000,
//   },
// ]
// mobiles.forEach((item)=>{
//   console.log(item.brand);
// })

// forEach loop never return any value.

// const myNums = [1, 2, 3, 4, 5, 6, 7];
// const newNums = myNums.filter((num)=> num > 4);
// console.log(newNums);

// Map: It's callback function, always takes callback as input.
// const myNums = [1, 2, 3, 4, 5, 6, 7];
// const newNum = myNums.map((num) => num + 10);
// console.log(newNum);

// Chaining
// const myNums = [1, 2, 3, 4, 5, 6, 7];
// const newNums = myNums
//                 .map((num) => num * 10)
//                 .map((num) => num + 1)
//                 .filter((num) => num >= 50);
// console.log(newNums);

// Reduce:
// const myNums = [1, 2, 3];
// const total = myNums.reduce(function (accumulator, currentValue){
//   console.log(`Acc: ${accumulator}, CurrVal: ${currentValue}`);
//   return accumulator + currentValue; // Here first time acc value will be 3, and currVal will be 1 as from Array, and on 2nd time returned value will get stored in acc, and currVal will be next element of Array, similarly it will go on.
// }, 3); // <-- 3 will go into accumulator value as first initialisation.

// Reduce in arrow function:
// const total = myNums.reduce((accumulator, currentValue) => accumulator + currentValue, 2);
// console.log(total);

// const courses = [
//   {
//     language: "JS Course",
//     price: 3999,
//   },
//   {
//     language: "Python Course",
//     price: 5999,
//   },
//   {
//     language: "Java Course",
//     price: 999,
//   },
//   {
//     language: "Data Science Course",
//     price: 12999,
//   },
// ]

// const total_price = courses.reduce((accumulator, prices) => accumulator + prices.price, 0);

// console.log(total_price);

```
