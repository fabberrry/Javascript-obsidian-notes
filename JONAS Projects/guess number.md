Just like we use class and id to select elm in css 
in js we also do this for dom manupulationn 

**QuerySelector**
```js
let elm = document.querySelector('.id'); // select elm using class or id 
where 
queryselector a mehtod ie availabele on document obj

log(elm);
```

---
 Now we have elm we can aslo get the text that it has as its COntent**use .textContent**** to extract
**textContent**
```js
let content = elm.textContent; 

// dot operator works form left to right , first querySelector then content 
```

---
Dom 



---
change text or number 
```js
content='some other content'
let num =  document.querySelector('.number').textContent;
num= 13;
```


change the input box in html
**Value property on inp elements**
```js
let ip = document.querySelector('.inp').value;
log(ip); /give noting as inp as nothing
ip =23;  /u see 23 in inp auto , not by user by typing 23


document.querySelector('.inp'); /throws error ❌ , req 1 argument or parament ie vlaue or smthig 

```


---




what we did , we changed the inp to 23 and log 23 by writing and runnningbut 
we want this to happen when some one clicks **check button**

### EventListner : 
mouse moving , mouse clcking , key press and many more event , and with event listner method we can wait for a certain evnt to happen and react to it 
iits a method req args 
(**type of 'event'** that u want to listen to ,**event handler**: a function value: that shoulb be exec when ever this event occur )
we are **not calling the fn inside this para** cuz havnt use ( ) and jsut passing it to event handler fn

**Real Development code** [[code of guess]]

1. check buttn : when some one press something should happen (we log whats is inp so need to select the inp and log its content by getting its value )
```js
const fn = function () {
const guesses_num= Number(inp.value);
console.log(guesses_num);
}
let chkbtn=document.querySelector('.check');
chkbtn.addEventListener('click',fn);
```
notes : if inp is vacant then  string inp gives empty string when log and number inp gives 0 when log
```js
const guesses_num= Number(inp.value);
console.log(guesses_num);
```

---
[[code of guess]]
