WHy playre 1 and player 0 , why not playre 1 and player 2

**select** the **elm** by **id** in js using **#** and **getElementById** method
```js
const score0El=document.querySelector('#score--0');
const score1El=document.getElementById('score--1');
```
**initialise the score**
we write 0 ie a number but js will convert them into string and store itno textcontent 
```js
score0El.textContent=0;
score1El.textContent=0;
```

make hidden class to be hidden in css

```css
.hidden {
	display:none;
}
```

and then add the hiddden class to dice to hide it  at the **beginnig of the game**

```js
const diceEl=document.querySelector('.dice');
diceEl.classList.add('hidden');
```

**Add event if click on roll btn a random dice numebr will show**
#### imp : how to change src of a image elm from JS
`error : use ${dice} instead of ❌{$dice}`
```js

// if click on roll , fn = roll the dice
btnRoll.addEventListener('click', function(){
/ generate a random number out of dice 
    const dice= Math.trunc(Math.random()*6)+1;

    
/ display that dice number
    //1. remove the hiddem class
    diceEl.classList.remove('hidden');


/ change the source property of diceEl as it a img elm 
    diceEl.src=`dice-${dice}.png`;
    // ie src = otherdice.png

/ check for rolled 1 if true weitch to next player , ow continue with same player
});
```

---

**if dice =1 then swithc other wise add the dice to active player rn its 0** and make a currScore global so it will ramain accessible for both players also if is in fn then will get reset when i press roll btn and fn trigger andmake currscore 0  so need to be in global 
```js
/ check for rolled 1 if true weitch to next player , ow continue with same player
	if(dice!=1){
        // add dice numebr to currscore
        currscore+=dice;
        current0El.textContent=currscore; 

    }
    else {// switch to next player

    }
```

but rather 0 or hard coding adding into 0 if active 0 or addidng into 1 if active 1 we canuse "\`\`"
and type exprression that give eirhter current--0 or current--1 elm 
```js
// intitally 0 
let active =0;
currscore+=dice;
let current_iEl=document.getElementById(`current--${active}`);
current_iEl.textContent=currscore;
```
**This was why we used 0 and 1 in clas names**


----
whoever **has player-active class** has some visully appealing colors so when we change the number active in js we also need to add or remove the active class when changing to diff  player 
means if player 0 active then 0 has active class so when change the active then alos  remove the active class from 0 and add the active class into the player1
but instead of hardcoding this logic usijng if else
**use toggle and : remove if it has or add if it has not** 

```js
const player0El=document.querySelector('.player--0');// the box of each player 
const player1El = document.querySelector('.player--1');// the box of each player

// also chnage css / ie if swicth then the color also switch
        player0El.classList.toggle('player--active');
        player1El.classList.toggle('player--active');
```


we need to toggle form both players so if 0 has thne remove from0 similarly chech same togle for 1 player too 

----

**Logic of player Holding the current score**
Either use a array of a numner of size two adn add into corrrect posistion dependitn whose active ie 0 so adding into 0s index else in 1s index . **pros**: no need to convert scoreelm texcontent into number before adding currscore so its method 2

```js
// part of mehtod 2
const scores=[0,0];

//if click on hold , fn = player can hold the currscor
btnHold.addEventListener('click',function(){
    // add current score to active player score
//MEHTOD 1
    let score_iEl= document.getElementById(`score--${active}`);
 ❌   score_iEl.textContent+=currscore; 
    // as txcont is the string so s+=num wont work here , reuslt will concatenate , not add so 
    // do 
 ✅   score_iEl.textContent=score_iEl.textContent+currscore; // due to string coersion it will add string + num into a valid numebr adn save as string into textcontent 
    


    
// METHOD 2 
    //or if ac=0 add into player0 ow 1s
    scores[active]+=currscore; //score[0] += currscore or score[1]+=currscore
});
```

