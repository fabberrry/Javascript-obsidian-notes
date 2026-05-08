
## BASICS
### Values and Variables 
1. what are **values**:  (literal value)
is a piece of data . Most fndamental unit of info in our program
```js
console.log("jonas");
console.log(33);
```

2. declaring variable :
will create a real variable in our computer memory

3. variable :
is like a box that contain something (book)  ie object and 
and we can write a label (variable name) on the box and 
later find the object(book) by using the label name
[[Js note Colt]]
### Naming convention
3. variable naming CONTAIN ONLY (num,letter,dollar,underscore) 
shouldnt start with : num
shouldnt start with : uppercase letter (not illegal but jst a convntion)
shouldnt be a : reserve keyWORD
shouldnt be a : name keyword (not illegal but dont do )

: **UPPERCASE** only for const  VARIABLES  eg (PI)

5. Make once and refer the same infinite times
ADVantages : **TO use the value over and over** 
: **easy to maintain** if i want to chnege the value i dont need to do change everywther i have used that value just channge the variable 's  one at a time and reflect everywhere it s used  

---
### Data types 
1. Number : int - float  all considered number date type only 
2. String : Seq of chars , single quotes or double quotes both work 
3. Boolean: Logical type ie oonly T or F
4. Undefined: Value taken by Variable ie not yet defined( EMPTY VALUE)
5. NULL : also means EMPTY but used in diff circumstances 
6. Symbol:  unique value that cannot be changed (introduced in **ES2015** )
7. BigInt: Large integers than the Number type can hold (**ES2020**)
```js
let age =23;
let name = 'Jonas';
let adult =true;
let child; // undefined 
let objct=NULL;
```

JS has a Dynamic typing feature : 
Dynamic Typing : 
**data types of a variable are determined automatically** . In js 
the value which has a data type , not the variable name , so 
variable only stores the value that have a type
so we do not have to manually define the data type of a variable 
```js
let x= 7777; was initially a num (x was a number type)
x='Rahul'; but now string can also be stored into it (x is a string type)
```
**pros : can change the type of a value ie hold by a variable with no issue**
cons: hard to debug 

---
1. undefined: when you declare only then it has undefined stored in it 
and thus the type of that is undefined
2. NULL: 
```js
let year;
console.log(year); // undefined ie a value inside year
console.log(typeof year) // undefined ie a typeof year 

// reassing a new value to year that used to be undefined type 
year=2002
console.log(typeof year) // gives number

```

---

Type of operator :
```js
console.log(typeof true); 
console.log(typeof varname);
console.log(typeof 'Jonas');
// bug
console.log(typeof null); // WRONG it says Null is a object type WRONG 
// CORRECT 
console.log(typeof null); // type is undefined 
```
Bug in typeof operator  

---
### Let Const Var 

**Let** 
For those variables so we **can change that during runtime**
ie allow reassigning - mutation to a variables
- **its a block - scoped**


Const used for those variable whose value cannot be mutated. Means we cannot do , we need a initial value when declaring const .
const: value in the const variable cannnot be changed
If even try then error: type error .
- also a block scoped 
- `const` variables **must be initialized at the time of declaration**
```js
const job; // missing initialiser  , ERROR
```


var : just like let we can mutate the value in it but
--- just dont use  it 
--- is fn-scoped


EXTRA : variable without decalring WRONG PRACTISE although it would run 
```js
name = "rahul"
console.log(name)
```


### Basic operatores
Math operaors. asignmendt operators, comparision operators
```js
////////////////////////////////////

// Basic Operators

// Math operators

const now = 2037;

const ageJonas = now - 1991;

const ageSarah = now - 2018;

console.log(ageJonas, ageSarah);

  

console.log(ageJonas * 2, ageJonas / 10, 2 ** 3);

// 2 ** 3 means 2 to the power of 3 = 2 * 2 * 2

  

const firstName = 'Jonas';

const lastName = 'Schmedtmann';

console.log(firstName + ' ' + lastName);

  

// Assignment operators

let x = 10 + 5; // 15

x += 10; // x = x + 10 = 25

x *= 4; // x = x * 4 = 100

x++; // x = x + 1

x--;

x--;

console.log(x);

  

// Comparison operators

console.log(ageJonas > ageSarah); // >, <, >=, <=

console.log(ageSarah >= 18);

  

const isFullAge = ageSarah >= 18;

  

console.log(now - 1991 > now - 2018);

  

////////////////////////////////////

// Operator Precedence

const now = 2037;

const ageJonas = now - 1991;

const ageSarah = now - 2018;
 // check operator precendence table 
  

console.log(now - 1991 > now - 2018);

  

let x, y;

x = y = 25 - 10 - 5; // x = y = 10, x = 10

console.log(x, y);

  

const averageAge = (ageJonas + ageSarah) / 2;

console.log(ageJonas, ageSarah, averageAge);

*/

```

### String 
```txt
==>need to use brackets like this (number) when using any number in the stirn ''
 "str str str (nbr+nbr-nbr)"
==>instead of using 'df' + 'dfs'
we use `` and use ${variable in it} `df dfs`
==>need new line use : \n\ in case of''
for `` just press enter where we need new line 
```

```js
// --- strings
const fname = 'rahul';
const job = 'artist'
const birthYear = 2002;
const year = 2025;

//need (int) like this in string
const rahul = "I'm " + fname + ', a ' + (year - birthYear) + ' years old ' + job + '!';

//dif btw thesse '' and ``
console.log(rahul);
console.log(`I am ${fname}`);
// conctenate
console.log('rahul' + 'kumar');
```

```js


```

```js


  


  

//input

// const fav= prompt('fav');

// if(fav==19)console.log(19);

  

// switch

const day='Mon';

switch(day){

case 'Mon':console.log('MON');

console.log('fsd');

break;

}

  

//THEORY : stamenet and expression

// EXP

// 3+4

// 1919

// true && fasle && !false

// STAMENT : it made from some expreseions does not produce a value

if(23>90){

console.log("sdfas");

}

  

console.log(`I am ${20}`); //so here ${expression only}

// console.log(`iam ${if(true)}`) no ${if else} cuz its a stement

  
  

// Ternary operator:

89>9?console.log(89):console.log("VVV");

const drink = age>=18?'wine': 'water'

console.log(drink);

  

//using ternary we can use condition inside template literal

console.log(`i like to drink ${age>=18?'wine':water}`);
```

### Type conversion and Coersion
`operators and functions automatically convert the values given to them to the right type`

#### Type conversion in Str and Number 
```txt
Str to Num
Use Number(Str) 

Num to Str
Use String(Num)

if any String fails to  be converted into num : 
--- we get NaN ie a invalid number whose typeof is Number type
NaN means a not a numer of number data type which shows that is a invalid number 
```

#### Type coercion in str and number
```txt
stringvar + numLiteral becomes string
but js has TYPE COERSION SO 
it dynamically change the type of number if used with the string . str operator num ==> str if + or num if - . 
if ->
+ is used then all nummber will chnage to string 
- is used then all stringnumber will chage to number 
```


```js
// string to num
let s = '1991';
console.log(Number(s));
// Type coersion in str and number 
console.log(s + 2); // result is string ie string +num==string ==> 19912 ie TYEP COERSION 
console.log(s-2); // result is number ie string - num == num ==> 1991-2 ie TYPE COERSION 
//num to string
console.log(String(2002));
```


#### Type Coercion in boolean
Js will try to coerse any value that is not boolean when being use in  logical context 
Falsy : value that are not actualy false values but they are  the values that become false when we try to convert them into boolean .
5 Falsy Values : 0 , '' , undefined , null , NaN
Other than these rest are : Truthy values . 
```js
// --- truthy falsy by MANUAL CONVERSION
console.log(Boolean(0)); // false 
console.log(Boolean(undefined)); // flase
console.log(Boolean('')); // fasle
console.log(Boolean({})); // true 
```

We dont explicitly convert these , they are always type coercion means 
when use truthy or falsy values js auto convert them for us 
when js convert : 
scenario : when use logical opertors btw these values 
scenarion 2 : our code has  if else  that has these values 

##### scenario 2 
```js
// TYPE COERSION in Boolean 
cost money =0  // its number type 
// here in logical context money convert into boolean by js and become T or F depending its a falsy or truthy value 
// same as we have done in Boolean(0) but now js will do type coercion cuz variable is being used in logical context
// eg
//type cohersion of falsy
const money = 0;
if (money) { // type cohersion happen then it 0 bcome false and wont exe
console.log("BYE");
} else {
console.log("RUN RUN RUN");
}

let height;
if (height) console.log("BYE"); // agian is undefined so bcme flasy
else console.log("RUNRUN RUN RUN RUN ");
```

---
### Equal vs Strictly Equal 
```js
// equal vs equal

const ag = 18;
// It will not do any Type coercion and return T only when ag is exactly same as 18 ie both should be exatly same data type and same value 
if (ag === 18) console.log('stricty 18 nummber cuz of === ');

// it does Type coersion and string converted into  numer an then checks the value 
if('18'==18)console.log('18 == cuz of type cohersion');

```

#### Prompt FN 
A fn that prompt you and you can give input by this on browser 
AUTO TYPE of input is string 
```js
promt("WHAT YOUR NAME") 
Numer(prompt("AGE"));
```

---

### Boolean Logical Operators
- AND OR NOT
```js
const hasDriverLicense = true;
const hasGoodVision = true;
console.log(hasDriverLicense && hasGoodVision);
console.log(hasDriverLicense || hasGoodVision);
console.log(!hasDriverLicense);
```

---

### SYNTAX of Switch 
```js
const day = MONDAY
// it will use strict comparioson ie 
// monday === MONDAY 
Switch (day){
	case 'monday':
		console.log();
		break;
	default:
	console.log()
}
```

---
### Statement And Expressions
**EXP**: code that produces a VALUE 
eg of EXP 
```cpp
3+4 // produces 7 
1919 // produces 1919
true && fasle && !false// produces false
operator // produces value eg condition ? exp : exp 
```
**STATMENT** : IT is made up of several expresion but it itself not produces any value . PROGRAM is a sequence of actions or statements . EG
```cpp
if()console.log("ACTION"); // statment  
```

EG : in tempelate literal we can only give expression  in that , not statments into.
```js
console.log(`I am ${2025-2000} years old`)
```

---
#### TERNARY 
condition ? expression : expression
Ii also can be used in templater literal 
```js
const age = 
```

---
## JS VERSION 
To standarize the language ECMA release ECMAScript 1 (**ES1**) 
Ecma is std where js is lang 

- major releases: ES5 then ES6/2015 (was the biggest upd to lang ever) . After that , they release new es every year 
new version is wrong word , call new releaase cuz **JS IS BACWARD COMPATIBLE** but its not **Fwd compatible**
- future release also called ESNext .


---
## BASICS 2
TO write more secure code . as it forbids us to do such things that lead to any bug in which vanila js would fail instantly 
```js
'use strict' 
```
PROS :
1. easy for dev to detect bugs
2. more secure code 
3.  it tells some mistakes that normak js wont 

##### scenario 
```js
//wrong spelling
if (passTest) hasDriverliscence = true;
if (hasDriverlisce) console.log('DRIVE'); // if i use wrong speelling then js will fail silently without letting us know that we did some mistake 
but strict mode give uncaught ref err  ie hasDrive is not define at lien xyz


// unintentional global variable
// x=10;
// console.log(x);

  

// using word which might get added later but arent reserved
// const private= 534; more eg : interface 
```

---

## Fn 

#### DEFINE : 
**a reusable peice of code , just like a variable that holds a reusable value but it has more chunks of code**

#invoke #parameters #arguments

Param: are variable that are specific to fn and only get define when we invoek the fn .  They also beign seen as input given to fn  . 
Arguments are the actual value given to the params when fn actually gets called 

### Types of Declaration of a FN  
#### 1. Naming Fn  
**Fn declaration** : we can call them before they are defined 
```js
//1. giving fn name direclty
function calcAge(birthYear) {code}

const save = calcAge(1991); // capture the value into save only when ifits return something
```

#### 2. Anonymous Fn ie A expression and give a value and this value capturing into calcAge2
**Fn expression** : we cannot call before initializing , bcuz of **HOISTING**  
```js
function (birthYear) {code}
```


```js
// 2. variable name acting as a fn name ie the whole expression of fun(){}

// has been assigned to calcAge2 varibale thus fn is assigned so it become a fn type 

const calcAge2 = function (birthYear) {code}
// calcAge2  is a fn now 
```

#### Fn are also just values adn thus we can store into variable 

---
#### 3. Arrow : 
```js
// 3. Arrow
// parameter => value; is a form of expression and means can be assign so can use by calling calcAge3 . no return keyword req , pros is so fast to type 

const calcAge3 = birthYear => 2037-birthYear;
// if need more paras use (p2,p1.) or more complex logic we use {} and return 
cost calcAge4 = (birthYear,firstName) => {code ... return value}; // here  return keyword is req before writing value 
```

---



### Array

**Init and add elm**
```js
  

// --- Arrays
const friends= ['R','K','A'];
console.log(friends);


// another way to create 
const year = new Array(1000,111,111,1232);

year[0]=33932
// but it was const so how we are mutating 
// only primitive const variable cannot be mutated but 
arra is non primitive 

// we cannot do this with const arr 
year =[3243,3423,423,423] ; give typeerr 


// give NaN when we do 3-year ie 3 - array so give NaN 
calc= fun(year){ 2020 - year}
calc(year)

 
//size:
console.log(friends.length);

  

// any data type to store:
const rahul = ['Rahul',2002,'Artist',friends];
console.log(rahul);

  

// Basic operations:

friends.push('I');  // add elm at end and return new len of arr

friends.unshift('Z'); // add elm to  the beginof arr , rtrn new len of arr
 
friends.shift(); //  remove elm from the begin 

friends.includes("elm") // return true if elm present in arr else false

```


**Remove**
```js
// Remove elements

friends.pop(); // Last elm will rmv and return that elm

const popped = friends.pop();

console.log(popped);

console.log(friends);

  

friends.shift(); // First elm to rmv and return that elm 

console.log(friends);
```


**Index**
give the referece of elm from arr
```js
console.log(friends.indexOf('Steven')); // return idx of elm 
console.log(friends.indexOf('Bob')); // return -1 if not in arr
```


---

### Objects

**Array** \[. . .]
```js

const jonasArray = [
'Jonas',
'Schmedtmann',
2037 - 1991,
'teacher',
['Michael', 'Peter', 'Steven']
];
```
**Obj** : each elm has a accociated key with it  { key : val }
```js

const jonas = {
firstName: 'Jonas',
lastName: 'Schmedtmann',
age: 2037 - 1991,
job: 'teacher',
friends: ['Michael', 'Peter', 'Steven']
};
```

**Order of elm in obj when we retrive them unlike arr where order matter as we going to access acc to order**
**access elm by their unique key in the object**

Key also callled property name  of that elm or value

Access
```cpp
  
// Dot vs. Bracket Notation 
console.log(jonas.lastName);  
console.log(jonas['lastName']); // can use any exprreession inside [ ] and can use that value to access the elm ,like below

const nameKey = 'Name';
console.log(jonas['first' + nameKey]); // jonas[firstName]
console.log(jonas['last' + nameKey]);// jonas[lastName] 
// console.log(jonas.'last' + nameKey) // ERROR
cuz in DOT we need to use real property name , not a computed property name 
as above lastName was real prop ,unlike this wehre 'last'+ 'Name' is a computer property 

// when to use when 
DOT :  if i know knwo the property name , can direclty use 
Bracket : if need to compute the property name to access 


// what if using wrong property name or undefined property 
jonas[sdfsafasdf] // rturn undefined  

```

**add more properties**
```js
 jonas.newPorp=value;
 jonas[location]='Portugal'
```

---
Object fn 
as fn are also the values that meeans we cal also create key adn value in objs where value is a fn 

```js
jonas ={
calcAge = function (para) {code} // no const let var needed when calcAge WHy?
// passing the property as args
calcAge: function (birthYeah) {
return 2037 - birthYeah;
}

  
// using this keyword to access that objects property rather pasing as agrs 
calcAge: function () {
console.log(this);
return 2037 - this.birthYeah;
}

  
// making a property in method so no need to call it to calc age , once it gets called age become a new property of that obj 
and can use age instead of calling the same fn agian 
calcAge: function () {
this.age = 2037 - this.birthYeah;
return this.age;
},
};
```

**this is methos , as any fn that is  attached to any object is called METHOD**
```js
jonas.calcAge(2929);
jonas['calcAge'](2343)];
```
**return is mandatory object method** 

---
#### this keyword inside method . this refer to the object that callling the mehtod
```js
calcAge: function () {
	console.log(this); 
	return this.birthYear;
}
```

---


#### FOR syntax
```cpp
// for loop keeps running while condition is TRUE

for (let rep = 1; rep <= 30; rep++) {
console.log(`Lifting weights repetition ${rep} 🏋️‍♀️`);
continue;
break;
}
```

#### While loop 
```cpp
let i=10;
while (i>=0){i--}
```




---
**Dom** 

Doc Obj Model : a strct repr of html docs , allowes js to access html elm and styles in order to manipulate then ,ie  change txt , attributs , and even css styles 
all this from our js  code

is auto created by the browser as soon html page loads , and is stored in a tree strcture liek this ![[DOM MANIPULATION.canvas]]
EACH ELM IS ONE OBJ IN THIS TREE
IT A DOM TREE STRUCTURE OF THIS CODE
```go
html
	head
		title
	head
	
	body
		section 
			p dfsdfsa p
			p dfsaddf p
		section
		
		section 
			img
		section
	body
html
```

---
DOm starts with doucmnet obj : serves as an entry point into the dom. is a special obj that we have access to in js 
the queSel methods is available on document obj ie why we say its entyr point to dom cuz we need it to start sleecting elms
```js
document.querySelector()
```

Next have html and then have two child that are sibling head and body 
and much more deeper in body till the 
**Basically its a complete repr of a html doucment and so that we can manupulate in complex wasy** 

---
Dom ! = js 
dom methods and props for dom manuoulation are not part of js . js is just a dialecte of ecma script specification and dom was not it there 
SO how they work in our code if not js part 
they are part of web api (libraries **(also written in js)**  that brosers implement) that we can access it from our js code . 
means they automaticaly available for us to use and dom manipllation works the same in all browser as there is and official dom specification that all  browser implement 

---
**Random** Fn 
```js
const n= Math.randon();  / Math is a object that js give adn random is one of math's methods
 gives us a number btw 0 and 1 ;
 
 / but to get a number for 0 to n 
 multi by n 
 const n=Math.random()*20;
/ it will give ranodm btw to 0 to 20.00000000... with decimal precision

to remove decimal point s
const n = Math.trunc(Math.random()*20);
but now it will give ranodm btw 0 to 19 as we removed decimal , it wont reach 20 as we cuutted .9999999 from 19.999999999 and only 19 left 
to mak e it raodon byw 1 and 20 ;

/add + 1 in result 
const n = Math.trunc(Math.random()*20) + 1;
```


**css manipulation using dom** 
- use camel case notation when writng css properties in js 
- alwasy use string when writing values for that properties( as we need to specify units wehn giving number , using # when giving colors to elms)
```js
let body =document.querySelector('body');

body.style.backgroundColor='#60b347';

  

document.querySelector('.number').style.width='30rem';
```
- even though changing css but its not affecting the css but its applying inline style means dom changeing the style using inline styling 

---
**Project 1**
[[guess number]]
[[code of guess]]

---
**Project 2**
[[modal]]

```html

```

**keyboard events** [[modal]]

---
**Project 3**
[[Pig Game]]



---
## Behind the scene of JS
### How JS works BTS
JS:
```txt
JAVASCRIPT IS A HIGH-LEVEL, PROTOTYPE-BASED OBJECT-ORIENTED,
MULTI-PARADIGM, INTERPRETED OR JUST-IN-TIME COMPILED,
DYNAMIC, SINGLE-THREADED, GARBAGE-COLLECTED PROGRAMMING
LANGUAGE WITH FIRST-CLASS FUNCTIONS AND A NON-BLOCKING
EVENT LOOP CONCURRENCY MODEL.
```

**HIGH LEVEL**
Any computer needs resources like **Ram , cpu etc**

LOW LEVL=`WE need to manully manage the resources`
HIGH= `We dont need to worry about any allocation or deallocation of res , everything happens auto`
PROS : easy to learn and easy to use 
CONS : programme running on HL will never be as fast as low 
BUt how they manage on its own.
HOW .
we have abstractions which take all the work away from us but how they .see
one power tool here that take memory managem(ie indeed a res) from devs is 
Garbage collector. 

---
**Garbage collection** ie a Algo which automaticaly removes old unused objs from memory in order not to cloag it up with these unnecessary stuff  , mainly this cloaging problem called memory leak . 
##### ie cleaning guy who cleans our memory time to time so we dont have to 

---
**Interpreted or just in time compiled**
COmputer processor only understand 0s and 1s . every prog need to written in this machine code . ie not practical .
so just
we write human readable code which is abstraction over these machine code.
This code eventually needs to be converted to machine code ie done by compiler or interpreter 
in js this transaltion inside the js engine .

---
js is fam for this.
**Multi paradigm lang**
#### Paradigm : An appraoch and mindset of structuring code , which will direct your coding style and technique.
3 types;
- Procedural programming 
- oop 
- functinal programming 
As many prg lang are either just oop or procedural but js is all of them 

---
Almost every thing in js is an object (except the primitive values ie num , string , etc) but arrays are just objects.
ques : when we create array how we are using or accessing the push method on this obj just  to add the elm?
```js
const arr= [1,2,3]; ==> this built from prototype .
arr.push(4); ==> our array inherits this "push" method from protype
```

Becz of prototype inheritence , 
we create array from array blueprint (ie prototype) which is like a template . This prototype contains all arrray's methods and the **array** that we create **in** **our code inherits the mehtod from prototype (blueprint)** so that we can use that mehtod on our array. 

---
**First Class Funtions**
Here fn  are simply treated as variables we can pass them into other functins, and can even  return them from functions
#### passing a fn into another fn as an argument is FIRST CLASS FN
```js
btn.addEventListener('click',fn);
```

---
**DYnamic** : Here it means dynamically typed : 
we dont assign data types to varibales instead they only become known when js engine exe our code  also the type of variable can easily be changed as we reassign the variable to diff typed value .
```js
let x=23==>here no data type definition given,types become knwon at runtime
x='rahul'==>data type of variable is automatically changed
```


Alternative : **TypeScript**

---
**Single Threaded**
?

---
**Non blocking event loop**
what is concurrency model : it is HOW js engine handles multiple tasks happening at the same time 
why we need :
Bcuz js runs in one **single thread**, so it can only do one thing at a time 
so we need a way to handle multiple things.
**Thread** is a set of instructions that is executed in a cpu . is where our program gets executed .

But what about a task which runs for a long period of time ie **long running tasks**
would it block the single thread. but **we need a non blocking behaviour**
but **how to achieve it** 
By using an event loop : it takes a long running tasks , executes them in the "background" and puts them back in the main thread once they are finished

---
### How js engine works
#### JS engine:
**A program that executed js code**
every browser has its own engine 
chrome uses  V8 engine and also used by node js which is js runtime , it is that we can use to build server side applications withjs ie outside of any browser .

But how it works and what are its components
every js engine contains: stack heap
stack : where our code is executed using execution context 
![[Call stack.canvas]]
Heap : unstructured memory pool which stores all obj our app needs

![[Heap.canvas]]
**How** code get compile to machine code so can be get exec

**Compilations** : Entire code is converted into machine code at once, and written to a binary file that can be exxecuted by any computer any number of time without converting into mahcine code again 
`src code =(compilation)=>machinecode=(execution)=>program running`
						 portable file
#### here execution can happen way after compilation
eg any app compiled way before ,now u are just executing it 
**Interpretation**: interpreter run through the source code and executes it line by line `src code=(execution line by line)+=> program running `
		**here code still needs to be converted to machine code**
#### Js use the mix of both
**JIT (just in time ) compiltion**
Entire code is converted into machine code at once, then executed immediately 
`src code =(compilation)=>machinecode=(execution)=>program run`
						 portable file
**but** 
#### here execution happens immediately

---
![[Screenshot 2026-03-02 at 11.58.34 AM.png]]
Below is explaination
How jit works
Modern jit compilationof js
**JS code**
```js
const x=23;
```

As soon as any piece of code enters then engine the first step is
**parsing** ie parse the code ie read the code . Parse into data structure called AST, by splitting each word into pieces that are meaning full to the lang like const or fn keyword and saving all these peices into the tree in a structured way
this is the place where our code gets checked **is there any syntax errors**

The resultant tree is later be used to generate machine code
**AST** of given **JS CODE**
```ast
{
  "type": "Program",
  "start": 0,
  "end": 13,
  "body": [
    {
      "type": "VariableDeclaration",
      "start": 0,
      "end": 13,
      "kind": "const",
      "declarations": [
        {
          "type": "VariableDeclarator",
          "start": 6,
          "end": 12,
          "id": {
            "type": "Identifier",
            "start": 6,
            "end": 7,
            "name": "x"
          },
          "init": {
            "type": "Literal",
            "start": 10,
            "end": 12,
            "value": 23,
            "raw": "23"
          }
        }
      ]
    }
  ],
  "sourceType": "script"
}
```

above is jsut repr of our code inside engine

2nd step is COmpilation of ast into machine code 
Then this machine code gets exec right away  becz js uses jit and we know this exec hapapen in call stack 
BUt 
js use a clever optimization strategy ie 
they create a very unoptimized version of the machine code in the beginning just so it can start exec as fast as possible then 
in background this code is beign recompiled during the already running program execution and this can be done multiple times ,after each optimization the unoptimised code will get swept with the new more optimized code without ever stopping execution . cuz of this process v8 is so fast
**parsing - compilation - optimisation all this happens in some special threads inside the engine ie completely separate from our main thread that was runing into call stack executing our own code**

---
#### What is js runtime
![[Screenshot 2026-03-02 at 12.17.26 PM.png]]

eg : browser (most common js runtime)
**Js runtime**: is a big container that has all the thigns that we need to use js (use js in the brwoser- for this case)
**1. JS engine is the heart of js runtime** , but engine alone is not enough . we also need
**2. web apis**: functionalities provided into the engine , *but they are not the part of the language*
, js only access this through global window object . *but they are part of js runtime* .
we also need 
**3. callback queue** data structure that contains all the callback fn that are ready to be executed
for eg: CLICk ; ie a event handler fn attached to any dom elem(for eg button) to react to certain events (click for eg)
so any event happen (click) , then the callback fn will be called , then this callback fn will be put into callback queue then it will wait for the call stack to get empty and when stack is empty then this call back fn is passed from queue to the stack so that it can be exec
All this happen by something called 
**4. event loop**: it takes callback fn from callback queue and put them into call stack so can be exe. and is essential for non blocking concurrency model


#### But Js  can also exist outside of browser , for eg can exist in node.js
#### Node.js. Javascript Runtime
its has similar componets but since we are not dealing with browsers so we dont have web apis component . **instead we have multiple c++ bindings and thread pool**


----
### How js executed the code 
As we already knwo that exec happens in call stack ie present in engine 
but here is more about it 

#### Execution context
- After making machine code now  its ready to be executed and 
- A global **1. execution context** is created for the **top level code**(code ie not inside in any fn)
	- so only code ie outside will be exec( cuz code of fn should only be exe when get called)
	- **execution context** environment is which a piece of js is executed. a box that  stores all the necessary info for some cod to be executed (exec coxt: is an abstraction concept) 
		- eg : stores all local variable  or arguments passed into a fn 

**pizza eg**

- now after creating the environment where top level code can be executed , it finally is executed . so **2. execution of top level code inside global EC**
- now after it finishes  **fn finally start to execute as well**
	- for each fn call a new EC will be created that containing all the info ie necessary to run that fn and 
**SUmmary** ONE global EC ie default context created for top level code and exec that code 
and when executing a fn call , one EC per fn will be created and executes that fn 

All this execution context together make up the **Call Stack** . 
ONce all the fn are done executing , engine will keep waiting for callback fn to arrive so can exec those callback fn (eg a fn (callback fn ) associated with a click event) and these all new callback fn will be provide by **event loop** 

---
##### what is inside execution context 
1. **Variable Environment**:  All these things 👇 are stored here 
```txt
let-const-var declarations
fn
argument objects : contains all the args that passed into the fn that the current execution context belongs to
```

2. **Scope Chain**: consist of references of variables that are outside of the current function and to keep track of its scope chains it is stored in each execution context 
3. **this**: each context gets this keyword 
These above are all generated in **creation phase** which happens right before execution . 
**EC belong to the arrow fn do not  get their own arguments keyword nor this keyword**
instead they can use the argument obj and the this keyword form their closest regular fn parent.

![[Screenshot 2026-03-02 at 5.45.56 PM.png]]

---
**Scoping**: How our program’s variables are organized and accessed.he asks
=> “Where do variables live?” or “Where can we access a certain variable, and where not?”;
-  **Lexical scoping:** Scoping is controlled by placement of functions and blocks in the code;
	eg: ` a fn ie written inside another fn has access to tha variables of parent fn `
-  **Scope**: Space or environment in which a certain variable is declared (variable
environment in case of functions). There is global scope, function scope, and block scope; 
eg: `variables enviroment which stored in the fn execution context`
**Diff btw scope vs variable environment**: for a fn scope , both are same .
global scope and block scope 
- **Scope of a variable: Region of our code where a certain variable can be accessed.**
TYpes of scope 
1. global scoope
- Outside of any function or block
- Variables declared in global scope are accessible everywhere
1. FUNCTION SCOPE
```js
function cal(year){
	cosnt now=9;
}
console.log(now) // ERROR: reference err
```
-  Variables declared here  are accessible only inside function, NOT outside
-  Also called local scope
3. BLOCK SCOPE (ES6)
Example: if block, for loop block, etc.
👉 Variables are accessible only
inside block (block scoped)
⚠ HOWEVER, this only applies to 'let' and const variables! ie why we say **let and const are block scoped** but var variables still be accssible outside  even its inside a block 
👉 Functions are also block scoped
(only in strict mode)
var when in a block and that block is in a fn then the var would still be accesible in the fn scope or if no fn present then acesible toglobal scope 
ie **var is fn scopes**
![[Screenshot 2026-03-02 at 6.02.08 PM.png]]
 ES5 and before we had only fn and global scope 
ie why code declared with var only care about fn and not about block s but es6 , all fn are block scoped with strict mode
means  if any block has a fn then that fn can only acccesed inside that block only 

**Global is blue and first is green and 
it have all the blue part and then in first , we have second and if ie yellow and purple respectively and purple hass all green part and yellow has also the all green part ie why**
`a child scope has access to all the varibale of its parent scope but vice verca is not possible`

How scope chain works 
**Variable lookup Process:**`if one scope need to access a variable but cannot find it in the current scope then it will look up in the scope chain and try to find in one of parent scope`
if it find out in any of the parent scope the ok `then it wont copy the variable ,it will just use it .`
if cannot find, it will give Reference err


**Scope chain vs call stack**: 
```js
const a ='Rahul'
first();
function first (){
	second();
	...
	function second () {...}
}
function thrid(){...}
```
![[Screenshot 2026-03-04 at 1.18.57 PM.png]]

**call stack** , where name EC with the variable enviorment in bracket
third EC (variable of third )
second EC (variables of second)
first EC `second=<function>`
global EC `a=rahul , first = <function> , third=<function>.`
(fn are **ordered** in which they were called )
**For now no scopes are involved rn creating one EC for each fn call and fiilling with the vars of that fn.**

now build **the scope chain** , start with the global scope 
Name scope with variabel available in that scope in the bracket
**Global scope:** (has same variables that was in the variable enviorment of the global EC)
**In global as we called the first fn then this fn also get respective scope**
First scope : ( has same variables that was in VE of the firtst EC  and also it has all the variables form it parent scope ie **Global scope** due to **Scope chain**) ie **first VE + Globacl VE**
(fn are **ordered** in which fn are written in the code, no matter the order in which fn are called) 
Second scope : **Second Ve and first VE + global VE**
thirst scope : **third VE and Global Ve**
(it cannot access the variable of global Ve and as first is also in global ve then it can acces the variable of first ve but when i go from here to first fn and do a varibale loolkup and i wont find any from first and its parent cuz it in the child and i cannot access variable of my child  )
Even if second call the thirst that doesnt mean third can access its variables thrid
has
```
d= hey (third ve)
-----
a= Rahul  (global ve)
first = <function> (global ve)
third= <funtion>  (global ve)
```
**Summary**
Scoping ?
its Types ?
**fact:** variables with var also be accessible up to the closest fn scope 
lexical scoping ? rule of accessing any variable depends on where the code fn and blocks are written 
**fact:** every scope always has access  to all the variables from its outer scopes . This is the scope chain.  scope chian is a one way streeet means a scope will neve ever have acces to the varibale of an inner scope 
**variable lookup**: when a variable is not in the current scope the engine looks up in the scope chain until it find the variable it looking for 
**fact:** to define a scope chain we need to add all the VE of the all its parent scope 
**fact** The order of fn call doesnt not affect the scope chain at all ( refer third fn call above)
fact :in global scope ,  u cant access variable that is in any other scope cuz from here only current scope wil get checked for variable and no parent scope present here to lookup to.

---
**Scoping in Practice** WATCH


---
**Variable environment** and Hoisting
**Hoisting** : Makes some types of variables accessible in the code before they are actualy declared . on the surface level it looks like ''variables lifted to the top of their scope''
but in bts
**WORKING ?** before the execution, the code is scanned for variable declaration before its executed, it happens during the creation phase of the EC. then for each variable ie found in the code a propp is created in vareable enviroment object 
Hoisting doest not wark the same for all the variable types 
`variable types and hoisting working`
**fn dec**: they are hoisted , means we can use fn dec before they are actually declared in code
**var**: even they are hoisted , when we tyr to access var varible we dont get the actual declared value , we get undefined **Note : we dont get error we get undefined. Major Reason of Bugs**
**let and const**: they are not hoisted but technically are hoisted , but the value of these variable are uninitialezed or **TDZ** at time of accesssing before its declared, which makes it like we cannnot access them btw the beginning of the scope and declaration line . so if we are in TDZ we get error 


eg 
```js
let a='Rahul'
{
	console.log(a) // refernce Err . but WHY . why not used scope chaing 
	.TDZ start from.begining of the scope until the line whehe varbl is define. 'a' is in tdz
	.T
	.D
	.Z 
	.is the region of the code where variable is defined but cannot be used in any way. like it didnt exits btu give ref err: cannot accs 'a' before initializaion.
	---------------------------------------------------------------
	let a= 'Kara';
	.safe 
	.to
	.use , now a is stu
	-----------------
}
```
cuz 
If a variable name exists in current scope, even in TDZ,  
it shadows outer variables completely.
```css
GLOBAL SCOPE
-------------
a : 5

BLOCK SCOPE
-------------
a : <uninitialized>   ← TDZ
```
WHAT HAPPEND : global scope created and has vars like a in his scope then 
this block scope created and has a in its scope 
when i try to print a , it will try to find that variable in current scope and say Yes its prsent in current so i have this variable to acces  so no scope chain required for this 'a' variable but now hoisting comes in 
due to let and const are hoisted in a diff way ,i can access this but due the value that im accessing is uninitialized or the place where im access is TDZ for that variable so  , will give Ref err : cannot acc 'a' before initialisation saying i know variable present  here in your VE but rn is uninitialised 

---
**fn expression and arrows**: depends upon which type of variable they are beign stored in (cuz they give value we can store them into variables)
so if var varibale stored a fn , then var hoisting will work other wise let and const hoisting will work

---
```js
{
console.log(a) // as a is in VE so stop looking for scope chain but this is TDZ so give ref err: cannot accs a before init 
let a='ra';
console.log(x); // as x in not in VE so give ref err:  x is not define 
}
```

Why this happens, why need a tdz to stop the hoisting's main aim(to acc before dec)
TO stop the accessing of variable before dec . this avoid err and bugs
tdz exist so even if we try to do acc before declar  we get err
- make const varible actually work the way they are supposed to .(suppose we try to acc the const variable when is uninitiased and reassign some value and then when we reach declaration it will try to reassign the const variable cuz we decalre there but then it throw err just cuz some one access the variable before declaration and assign , now the declaration stament of const is throwing err saying u again try to reassing a const vraible )
so simple , not to allow access of let nd const before they decalred

now if its stoping the work of hoisting , why introduced hoisting in the first place just  remove it and then no deal with hoisting , so no deal with tdz , so no deal with all this. but
Hoisting were introduce to help people so they can access the **fn** before declartion. and it eventually help the hoisting of var variables but to make sure good pracitses we also introduce let and const with diff hoisting work around using tdz concept 

---
**Hoisting Pracice**


IMPORTANT TO WATCH(fn stored in var , let , const variable part is imp)


---

### THis Keyword:
Special varibale ie created for every execution context (every fn ). take the value of ( points to ) the owner of the fn in which the this keyword is used.
**Points to the owner of the fn**

*this* is not static , it depends on how the fn is called 
diff ways fn can be called
1. **method** : fn attached to an object is method , 
	1. here *this* points to  `the object ie calling the method`
```js
const jonas = { // created a jonas obj with some method and attributes
	name : 'Jonas'
	showNmae: function(){
		log(this.name); // this refer to the jonas object
		or 
		log(jonas.name); // same effect : but above is best practice
	}
}
jonas.showName(); // jonas is a object 
```

2. **simple fn call :** this points to `undefined` in strict mode, other wise *this* points to the global obj of browser ie *window* object.

	`arrow fn are not a way to call the fn , we use variables to store them and call them as simple fn but this dont work as same as simple fn `
3. Arrow fn : **They don't get their this keyword**  #imp 
4. here if use this keyword , this means`this keyword of surrounding fn or parent fn ` **'this' is also called lexical this keyword cuz its gets picked up from outer lexical scope of arrow fn**
5. Event listerner : this mean `dom elm on which the handler is attached`

what *this* keyword is not : 
*this* will never point to the fn in which we are using it
*this* will never point to the variable environemnt of the fn 

OTHER WAYS in which we can call a fn
6. Using *new keyword, call , apply, bind* methods.

---
**'THIS' Practice**
*G*
```js
console.log(this); -> window {} // in GLOBAL , 'this' = window obj
```


with a reg fn call like this means where we  call this fn without the fn beign attacted to any object ie without having any owner.
```js
const calcAge = function(bithYear){
	console.log(3432 -bithYear);
	console.log(this); -> undefined (in strict mode) -> window(in vanilla)
}
calcAge(1919);
```


```js
const calcAgeArrow = (birthYear)=>{
	console.log(2027-birthYear);
	console.log(this); -> window fn (even in strict mode)
}
calcAge(1980);
```
cuz Arrow fn doest not get its own THIS keyword
so instead it simply uses the lexical this keyword ie it uses *this* keyword of its parent fn or its parent scope , which is GLOBAL in this case. so *this* keyword of GLOBAL points to window that is why , its giving window.
`'this' is not the 'this' keyword of this fn here , this is the 'this' keyword of its parent`


*this* inside a method (fn attached to an object)
```js
const jonas={
	k:val,k2:val,
	calcAge:function (){
		console.log(this); -> {k:val,k2:val}
	}
}
jonas.calcAge();
```
*this* point to the exactly this object (ie the one that is calling the method) ie `jonas` in this case. another way to say,this point to `jonas` ie is the owner of the method.

PROS: we dont have to pass any repeative value as argumen in this mehod call 
it can access its val from key without passing birthyear as argument.`log(this.birthYear)`

---
- Tell me something that is which is not in your resume.: strength , area of improvement 
- Imagine you have been assigned two mentors for project , one is happy and other person criticise you , which feedback would you take to work on. 
- what would you do to contribute the success of the project. 
- who did you partner with and how did you partner.
- if you have a project that failed , what happened what did you learn how has this shaped your apporach today.





----
## Data Structures  
#### Destructuring Arryas 
```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],

  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  },
};
```
is a ESX feature : a way of unpacking values from an arrao or obj into sep variables (complex ds into smaller ds ie variables)

1. way
```js
const arr= [1,2,3];
const a=arr[0];
const b=arr[1];
const c=arr[2];

```
better unpacking using destructuring assingment
```js
const [x , y , c] = arr; 
destructuring assignment  = (the data structuring where unpcking applies)
when used [] in right side 
```

2. dont need to take all the elm
`  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],`
```js
const [first, second] = restaurant.categories; 
```
it will just follow the order 
3. can skip the elm during unpacking `by leaving a hole there`
```js
const [first, ,third] = restaurant.categories; 
```
4. How to switch these variables ,
`first elm should be Pizzeria and second shoudld be Italian`
```js
const [first, second] = restaurant.categories; 

// mehthod 1  using temp
const temp = main;
main=secondary;
secondary = temp;


// method 2 using Stucturing 
[main , secondary]= [secondary , main]; --> Pizzeria Italian
create the array with inverted variables and destruct them and reassign 

else 
[secondary , main]= [main, secondary]; --> undefined Pizzeria
```
- will not affect the order of  res.categories 
**NOTE: make main, second as let variable else error**

5. Return multiple values using destrucuring : fn that reuturn a arryy(multiple return values) and then immediately unpack them
```js
order: function (starterIndex, mainIndex) {
	return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
}

const [starterFood, mainFood] = restaurant.order(1, 0);
console.log(starterFood,mainFood); -> Bruschetta Pizza
```

6. Unpacking in Nested Array
```js
const nested = [2,4,[5,6]];
const [i,,j]=nested; -> 2 [ 5, 6 ]
```
individual value using unpacking inside unpacking
```js
const nested = [2,4,[5,6]];
const [i,j,[a,b]]=nested;
console.log(i,j,a,b); -> 2 4 5 6
```

7. set Default Values for variables when extracting them , when size array dont know
```js
const arr=[8,9];

// no default 
const [i,j,k]=arr; -> 8 9 undefined

// using default values
const [i=0,j=0,k=0]=arr;
console.log(i,j,k); --> 8 9 0
```

#### Destructuring Objects
just use {} instead of `[]` and provide the variable name that match exacty with the actual property name that want to extract from object
1. extract : name categoris and opening hours
```js
const { name, openingHours, categories } = restaurant;
// in restrau : name ,...,  catergoreis ,... ,openinghrs 
// still didnt followed the order 
console.log(
	name, -> Classico Italiano
	openhrs, -> [ 'Italian', 'Pizzeria', 'Vegetarian', 'Organic' ]
	categ --> {thu: { open: 12, close: 22 },fri: { open: 11, close: 23 }}
)
```
- as order doesnot matter in object , we dont need to skip the elemnets in btw unlike array 
- and also no need to follow the exact order 

USE CASE : Extract the data from API call , cuz usually API gives the data in Object form 

2. But we need to give name  our variable exact as property names , what if we want some other names for our variables , like this:
```js
const { name:n, openingHours:hrs, categories:c } = restaurant;
console.log(n , hrs, c);
```
3. if use diff property name : will give `undefine` in that variable. req `mainMenu`
```js
console.log(restaurant.menu ); --> unefinde
```

So USE DEFAULT VALUES when trying to acces the props that does nt exist on the object else we get `undefined`  `res.menu X , res.mainMenu /`. just like we do in arr `[i,j,k=0]`
```js
const {menu =[], starterMenu:starters=[]}=restaurant;
console.log(
  menu, ->[]
  starters -> [ 'Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad' ]
);
```
Cuz when using third party API we might not always know how exactly the data lookslike

4. mutating the variables while unpacking `similar to switching in array-unpakcing`
```js
let a = 111; <-- mutate this to obj.a
let b = 999; <-- mutate this to obj.b
const obj = { a: 23, b: 7, c: 14 };
{ a, b } = obj; -> error:SyntaxError: Unexpected token '='


So
({ a, b } = obj); -> 23 7
console.log(obj); --> { a: 23, b: 7, c: 14 }
```
- first we have some variable that exactly has name as property name of obj, we want the value of those variable let a, b to mutate to 23 and 7 instead of 111 , 999 , we cannot use const {a,b}=obj or let {a,b}=obj cuz a,b already declared(ERROR) so use nothing just like when do reassignment `\{a,b} = obj;` but IT GIVE ERROR : 
- Fix? to use parenthesis 
`({ a, b } = obj)` instead of above 

5. nested objectes
`Extract open and close from res.openingHrs` open -close values is insdie openHrs obj which is inside res obj 
```json
openingHours: {
  thu: {
    open: 12,
    close: 22,
  },
  fri: {
    open: 11,
    close: 23,
  },
  sat: {
    open: 0, // Open 24 hours
    close: 24,
  },
}
```
Get the day for which we want open and close value
```js
const { sat } = restaurant.openingHours;
console.log(sat); --> { open: 0, close: 24 }
```
as we want the value , we furture destruct this saturday obj 
```js
const { sat:{open:o, close:c} } = restaurant.openingHours;
console.log(o,c); --> 0 24
```

6. Application : suppose a fn which has a lot of parameters then during calling its so hard to know the order of those parameters , rather than passing mannually , fix? : just pass the object as an argument and fn will destructur that obj immediately
```js
// function with just a object para with no destructuring 
orderDelivery: function (obj) {
	console.log(obj);
},
// function with immediate destructuring 
orderDelivery: function ({starterIndex,mainIndex,time,address}) {...},
  

restaurant.orderDelivery({
  time: '22:30',
  address: 'Via del Sole, 21',
  mainIndex: 2,
  starterIndex: 2,
});
```
- DURING CALLING: order of parameter doesnt matter - calling
- during destructing in fn : order doesnt matter here too - fn 
- need to use 'this' keyword to access the data of those parameters (not illegal thou)
PROS: *the props in the index don't have to match the order in which we do destructuring in fn*

#### Spread Operator
take all the values out of the arr and write them individually as if we wrote those indi values here manually
`manually writing the individual values of arr`
```js
const arr = [ 1, 4 ,5 ];
const newArr = [ 10 ,40 ,50, arr[0],arr[1],arr[2]]; 
```

Using Spread Operator `...`
```js
const newArray = [10,40,50,...arr];
```

Use case : use spread operator whenever need to write multiple values separated by commas eg Expand the newArr using old Array (here)
eg when passing arguments into fn 
log individual elm of this arr : cuz `console.log()` is a fn where we can pass individual elm using commas and print each one with spaces ie the exact use case where we need to write indi values of arr using commas 
```js
console.log(arr); -> [ 1, 4, 5 ]
console.log(...arr); -> 1 4 5  // method 2 BETTER 
console.log( 1, 4, 5) -> 1 4 5  // method 1 manully
```

*Note:* we are not manupulating the old arr when expanding the new arr 
`const newArray = [10,40,50,...arr];`
eg. Join two arrays
```js
const menu = [...restaurant.mainMenu, ...restaurant.starterMenu];
console.log(...menu);
```

SUMMARRY
- take all the elm from arr and it doesnt create new variable 
- only use it in places where we would otherwise write values separated with commas 
**COPY**
eg creating  Shallow Copy ,same as ?OBJECT.ASSIGN
```js
const mainMenuCopy = [...restaurant.mainMenu];
```

the spread operators works on all iterables , 
Most of the build in DS in js are iterables except *objects*
**NOTE** `...iter` is not a expression, so we cannot use it in tempelate literal ie `${}` means 
`${...iter} syntaxERROR:unexpected Token`

eg a custom fn 
```js
const ingrediendts = ['mushroom', 'spargus', 'cheese'];
restaurant.orderPasta(ingrediendts[0], ingrediendts[1], ingrediendts[2]);❌
restaurant.orderPasta(...ingrediendts);✅



WHAT FN EXPECTS:
  orderPasta: function (ingredient1, ingredient2, ingredient3) {
    console.log('making it using', ingredient1, ingredient2, ingredient3);
  },
```

*Q1* when spread op get added in js 

eg with Objects
copy the existing Object using spread operator 
```js
const newRestaurant={...restaurant , Boss:R,Y:2025 };
```
shallow copy objects , changing one wont affect another 
```js
const newRes ={...res};
```

#### Rest Pattern and Rest parameter
exactly like spread op , same syntax `...` but it does the opposite of spread op
Spread op: to build newArr, or to pass Multiple values into fn , where spread op just `expand the arr into individual elm``

Rest : same syntax `...` but used to collect multiple elm and  condense them into an array.
SO spread used to `unpack the arr into elm` and rest used to `pack elms to arr`


Spread:  used at right side of assignment operator `nAr=[...arr]
Rest: used at left side of assignment operator `[a,b,...others]=[arr]`

so it give first ,second and rest of the elms of the arr ie `a=1 b=2 others=[ 3, 4, 5, 6]`
```js
const [a,b,...other]=arr;
console.log(a,b,other); --> 1 2 [ 3, 4, 5, 6]
```
it collects the rest of the elms and put it into a new arr called `other`
eg: using both in a single statement 
```js
const [pizza,,risoto ,...otherFood] =
[...restaurant.mainMenu, ...restaurant.starterMenu];
console.log(pizza,risoto,otherFood);
```

NOTE 
`const [pizza,,risoto ,...otherFood , bread] = [...restaurant.mainMenu]`
Give SyntaxError : Rest elm must be last elm 

eg with objects 
```js
q1. take the thu and fri and pack it up in single obj
openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  }


const { sat, ...weekdays } = restaurant.openingHours;
console.log(weekdays); 
--> { thu: { open: 12, close: 22 }, fri: { open: 11, close: 23 } }
```


eg in fnc: 
spread: we expanded all the elms of this ingrediends arr , so to pass these elm as individial arguments to fn 
`we want to achieve this add fn to add any arbitrary number of values`
```js
const add = function(){
  
}
add(2,3);
add(2,3,4);
add(2,3,4,5);
```
`Q1: How many parameters do we make , for each type would we need a new add fn with more parameters`

Soln: make a rest variable that takes the multiple values (arbrtrary number of values) and then pack them all into one arry called `numbers`
```js
const add = function(...numbers){
  console.log(numbers);
}
add(2,3);
add(2,3,4);
add(2,3,4,5);
```
`USING RSEST ARGUMENTS`
Spread: we expand the input 
Rest: we Compress the input 

eg. Using both spread (pass in arguments) and rest(args compressed in parameters)
```js
const x=[1,2,4,5,8];
add(...x) --> here unpacking x into 1,2,3,4,5,8 
and in Fn(...x) --> here we packing those 1,2,3,4,5,8 into x 
```

Edge Cases 
```js
  orderPizza(mainIngredient, ...otherIngredients) {
    console.log(mainIngredient);
    console.log(otherIngredients);
  },
  
restaurant.orderPizza('mushroom', 'onion', 'olives', 'spinach');
```


in case 1:
mushrroom passed as mainIngredient and all the remaining packed into otherIngredients arr using rest 
in case 2 
no remaining elms passed , so otherIngrediend is a empty arr. cuz nothing to collect or pack
Rest parameter serves to collect the unused parameter that not used in this parameter`mainIng`


---
Summary
Spread and rest both look same but work in opp way depe on where they are used ,
Spread used where  we would otherwise write values separated by comma.
Rest is used where we would otherwise write variable name separated by commas .
```js
sep -> need to write [arr[0],arr[1],arr[2]] so we do [...arr]
rest -> need to write [a , b , c,d,e,f] = arr so we do [a, ...other]=arr
```
---
#### ShortCircuiting And OR 
Using Logical Operators only to comine boolean values .
```js
used two values != boolean and it returned a value ie not a boolean
log(4 || 'Rahul') -> 
```
Result doesnt always have to be boolean
OR 
- they can use data 
- return any data type 
- they do shortcircut evaluation 
Shortcircuit : If first value is a truthy value it immediately return that truthy value 
if operator found and truthy operand then the other operans  wont even be evalueated
Dont even look at them .

if falsy then evaluation continues then either found a truthy value and reutrn that or return the last operand

USE CASE: if DATA exist then assign to the variable else assign the default value in this variable 
```js
const X = data ? data : -1;
```
USING OR 
```js
const X = data || -1;
```
But what if data exist but value is 0 ie indeed a valid value for data but BOTH this method will assign -1 instead of 0 
Fix? : use nullish operator

And 
It short circuit when the operand found to be falsy , then imm return that flasy value without even evaluating the rest of the operand , but if truthy then evaluation continues then either found a falsy and return that or return the last operand
```js
log(0 && 'Rahul') -> 0
```
so if some one is false then entire result be False so no need to evn look any of the operand now , return that falsy .
eg if we dont know is this fn exist or not then 
```js
if(method){
	method();
}
```
USING AND 
```js
method && method();
```
if doesnt not exist so undefien it will short circuit the evaluation and nothing witll hapen if does exixt then the mehotd() will get evaluated and then it will get called .

---
sol- nullish coalescing operator inc=tro in es2020 
```js
const guest = restuarnat.num ? restuarant.num : 10;
const guest = restaurant.num ?? 10;
```
works with the idea / concept of nullish values instead of falsy value. 
and only null and undefined are considered as nullish values , so only nullish values will get shortcircuit the evaluation here 

---
Logical Assignement operator : intodueced in ES21
`OR Assignment Operator`
```js
res1.num = res1.num || 10;
res1.num ||= 10;

but still fail on res1.num = 0 
CUZ it work on falsy values 
```
sol : use nullish assigment operator 
`res1.num ??= 10`
`And assignment operator ` we want to anonimise the names of restra owner , ie when there is a valid value in owner we want it to become a "" only , ie make it annonimise
```js
res2.owner = res2.owner && '<ANNOYMOUS>'
fail on if owner was undefined already 

so soln:
'use AND assigment operator'
res2.owner &&= <ANONIMISE>


```
---
*CHALLANGE 1*
We're building a football betting app (soccer for my American friends 😅)!

Suppose we get data from a web service about a certain game (below). In this challenge we're gonna work with the data. So here are your tasks:

1. The first player in any player array is the goalkeeper and the others are field players. For Bayern Munich (team 1) create one variable ('gk') with the goalkeeper's name, and one array ('fieldPlayers') with all the remaining 10 field players
2. Create an array 'allPlayers' containing all players of both teams (22 players)
3. During the game, Bayern Munich (team 1) used 3 substitute players. So create a new array ('players1Final') containing all the original team1 players plus 'Thiago', 'Coutinho' and 'Perisic'
4. Based on the game.odds object, create one variable for each odd (called 'team1', 'draw' and 'team2')
5. Write a function ('printGoals') that receives an arbitrary number of player names (NOT an array) and prints each of them to the console, along with the number of goals that were scored in total (number of player names passed in)
6. The team with the lower odd is more likely to win. Print to the console which team is more likely to win, WITHOUT using an if/else statement or the ternary operator.

TEST DATA FOR 6: Use players 'Davies', 'Muller', 'Lewandowski' and 'Kimmich'. Then, call the function again with players from game.scored

GOOD LUCK 😀
dATA :
```js
	const game = {
	  team1: 'Bayern Munich',
	  team2: 'Borrussia Dortmund',
	  players: [
	    [
	      'Neuer',
	      'Pavard',
	      'Martinez',
	      'Alaba',
	      'Davies',
	      'Kimmich',
	      'Goretzka',
	      'Coman',
	      'Muller',
	      'Gnarby',
	      'Lewandowski',
	    ],
	    [
	      'Burki',
	      'Schulz',
	      'Hummels',
	      'Akanji',
	      'Hakimi',
	      'Weigl',
	      'Witsel',
	      'Hazard',
	      'Brandt',
	      'Sancho',
	      'Gotze',
	    ],
	  ],
	  score: '4:0',
	  scored: ['Lewandowski', 'Gnarby', 'Lewandowski', 'Hummels'],
	  date: 'Nov 9th, 2037',
	  odds: {
	    team1: 1.33,
	    x: 3.25,
	    team2: 6.5,
	  },
	};
```

1. Create player 1 and player2 arrays 
```js
// sol 1
let player1 = [];
let player2 = [];
[player1, player2] = [game.players[0], game.players[1]];
console.log(player1, player2);

// ANS
const [p1,p2]=game.players;
```
2. First player of team will be the Goalkeeper and rest be other members
```js
// sol2
let gk, others;
let gk2, others2;
[gk, ...others] = [player1];
[gk2, ...others2] = [player2];

// ANS
const [gk, ...fieldPlayers]=player1;
```

3. make a array that has all the players from both team 
```js
// sol 3
let allPlayers;
[...allPlayers] = [...player1, ...player2];
console.log(allPlayers);

// ANS
const allplayers=[...player1,...player2];
```
4. make a new player1 array that has all old elm + some 3 extra elm 
```js
//sol
let players1Final = [...player1, 'Thiago', 'Coutinho', 'Perisic'];
// ANS
cosnt pf=[...p1,"","",""];
```




----
For of SYNTAX #syntax
```js
for (const i of arr)log(i);
for(const [i,elm] of )
```

---
Enhanced objects literals (intro in ES)
Exs6 introduced 3 ways to write obj literals like this. `the below that manully written`
```js
const restaurant = {
  name: 'Classico Italiano',
  location: 'Via Angelo Tavanti 23, Firenze, Italy',
  categories: ['Italian', 'Pizzeria', 'Vegetarian', 'Organic'],
  starterMenu: ['Focaccia', 'Bruschetta', 'Garlic Bread', 'Caprese Salad'],
  mainMenu: ['Pizza', 'Pasta', 'Risotto'],
  order: function (starterIndex, mainIndex) {
    return [this.starterMenu[starterIndex], this.mainMenu[mainIndex]];
  },

  openingHours: {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  },
  orderDelivery: function ({ starterIndex, mainIndex, time, address }) {
    console.log(obj);
  },
  orderPasta: function (ingredient1, ingredient2, ingredient3) {
    console.log('making it using', ingredient1, ingredient2, ingredient3);
  },

  orderPizza(mainIngredient, ...otherIngredients) {
    console.log(mainIngredient);
    console.log(otherIngredients);
  },
};
```
1. suppose we have a object `opeingHrs` defined outside of this object 
```js
  const openingHours= {
    thu: {
      open: 12,
      close: 22,
    },
    fri: {
      open: 11,
      close: 23,
    },
    sat: {
      open: 0, // Open 24 hours
      close: 24,
    },
  };
```
we want this opening hrs in our object so we do
`openingHrs: openingHrs` in restaurant obj
But this prop name is exactly the same as the variable name from which we are getting the new object 
so ES6 Enhanced obj literals We dont need to write this 
just do 
`oreing`
take this opeinging hrs obj, and put into the restraunt obj and create a property name with exactly that variable name 

2.  Allow to write shorthand methods 
```js
UNLIKE THIS--> order: function(){...}

DO THIS-> order(){...}
```

3. compute the property rather than typing them manually 
```js
const weekdays=['','','',''];

rather doing -> thu : ...

do ->[weekdays[4]]: ... property become thu
or ->[`day-${2+2}`]:...  property beome day-6
```
`means u can compute propert name as u want`

---
Optional chaining
when accessing a property  of a obj that doesnt exist 
Suppose we dont know is this prop exist or not, eg if the data came from a real web service ,API , there could be multiple restaurants and not all of the open on mon , so there may not be a property mon in obj
```js
log(res.openHrs.mon) --> undefined
```
still no problem 
but if go even furture in chaining 
when try to check timing on monday , WE GET ERROR
```js
log(res.openHrs.mon.open) -->TypeError: Cannot read properties of undefined (reading 'open')
```
fix?
```js
if(res.openHrs.mon){
	console.log(restaurant.openingHours.mon.open); 
}
```
`BUT`
 