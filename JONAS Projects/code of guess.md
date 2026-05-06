[[guess number]]

```js
'use strict';

  

let secret_number = document.querySelector('.number');

const rdm = Math.trunc(Math.random()*20) + 1;

const scoreelm=document.querySelector('.score');

let mainscore=scoreelm.textContent;

  
  

secret_number.textContent = rdm;

let inp=document.querySelector('.guess');

const fn = function () {

let currscore=scoreelm.textContent;
console.log(typeof currscore);

const guesses_num= Number(inp.value);
console.log(guesses_num);

let msg = document.querySelector('.message');
msg.textContent="Number is required , pls give";

if(!guesses_num){
console.log(msg);
}

// if inp is number , compare it with the secret_number

else if(guesses_num===rdm){
console.log("win");
msg.textContent="WINNNNNNERRRRR";
}

else if(guesses_num>rdm){
msg.textContent='try lower number';
currscore--;
}

else {
msg.textContent='try higher numebr';
currscore--;
}

if(currscore>=0)scoreelm.textContent=currscore;

else {
msg.textContent='You lost';
scoreelm.textContent=mainscore;
}

}

let chkbtn=document.querySelector('.check');

chkbtn.addEventListener('click',fn);
```

---


**Game reset fnlity using Again btn**
```js
const resetfn = function () {
// restore the color 
    body.style.backgroundColor = '#222';
// restore the width
    document.querySelector('.number').style.width = '15rem';
// set to ? again 
    secret_number.textContent = "?";
// set the inp to empty 
    inp.value="";
// set the score to back to main score
    scoreelm.textContent = mainscore;
// set the msg from winner to start guessing ...
	msg.textContent="Start guessing";
}

//event
let againelm = document.querySelector('.again');
againelm.addEventListener('click', resetfn);
```


---

**update high score logic**
```js
// whn player wins
else if (guesses_num === rdm) {
	msg.textContent = "WINNNNNNERRRRR";
	
	let high = Number(highscrelm.textContent);
	if (high < currscore) {
		highscrelm.textContent = currscore;
	}

}
```

