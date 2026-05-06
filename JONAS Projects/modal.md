we can show the window when some one click the its respective button and also hide it using x btn and also if clicked out side the window 

```css
CSS
/* CLASSES TO MAKE MODAL WORK */
.hidden {
  display: none;
}
```

```html
HTML
<button class="show-modal">Show modal 1</button> ==>  btn 
<button class="show-modal">Show modal 2</button>
<button class="show-modal">Show modal 3</button>

<div class="modal hidden"> ==> the window
  <button class="close-modal">&times;</button>
  <h1>I'm a modal window 😍</h1>
  <p>
	...........
  </p>
</div>
<div class="overlay hidden"></div> ==> outside part of the window ie overlay
```

```js
???? JS

'use strict';
const modal = document.querySelector('.modal'); //=> the btn 
const overlay = document.querySelector('.overlay'); //=>outside part of window
const btnCloseModal=document.querySelector('.close-modal'); //=> X btn
const btnsOpenModal= document.querySelector('.show-modal'); //=> the first button  ie a button.show-modal1
console.log(btnsOpenModal);
```

But **queryselector** is only selecting a single button out of 3 showbtns so how to select all the three buttons
USe **queryselctorAll**
```js
const btnsOpenModal= document.querySelectorAll('.show-modal'); ie nodeList(3)
```

so its jsut a array now so we can traverse and work on all of them 

---

```js
%% eg %%
for(let i=0;i<btnsOpenModal.length;i++){
    console.log(btnsOpenModal[i].textContent);
}
```

----

now we will go to add event listerner to each button and say 
when click then 
go to the **modal class** in html 
```html
<div class="modal hidden"> ==> the window
  <button class="close-modal">&times;</button>
  <h1>I'm a modal window 😍</h1>
  <p>
	...........
  </p>
</div>
```

and remove **hidden class**
```html
<div class="modal"> ==> the window
```

result : the window will become visible

by using js , **IMP: dont use dot here to specify the class name unline used to do in queryselectr**
```js
modal.classList.remove('hidden'); // window will be visi
```
also need to make overlay also to be visiibel to remove the hidden class from that too
```js
overlay.classList.remove('hidden'); // overlay will be visi
```

just like it become visible when we click the show btn 
we need to make a X and ovelay implement too so can become invisible when we click X or click overlay. it is outside of the for loop cuz its not related to those 3 btns  
```js
// for closing the model  when click X
btnCloseModal.addEventListener('click',function(){
	modal.classList.add('hidden'); // window will get hidden
	overlay.classList.add('hidden'); // overlay will get hidden
});
```

but this is only work if u click x btn 
we need to implement also the overlay when if click on overlay same model overlay hidden class should get added 

```js
const closeModal = function () {
    modal.classList.add('hidden');
    overlay.classList.add('hidden');
};
// for closing the modal wehn click overlay 
overlay.addEventListener('click',closeModal);
```
---

**Keyboard Events** just like click event is 
Another type of events , but they are  global events means they dont happen on one specific a single element . so we uslly listen event on whole document 
so here the element on which the addevnetlister method to be called is the whole document object 
ie **document**.
```js
document.addEventListener('keydown',function(){
    console.log('some key was pressed');
})
```
3 types of keybaord event **key down**, key up, key press
keydown : when we press the key 
keyup: we lift off the key 
keypress: pressing continuosly

**how to knwo which btn presses** we need 
event object  : when ? 
```js
document.addEventListener('keydown',function(e){
    console.log('some key was pressed');
	console.log(e);
    console.log(e['key']); or e.key
});
```

---
so we can use it to imllemt that
when some press **ESC** key we closeModal but if press key but window is already hidden do nothing 

```js
if (e.key === 'Escape' && !modal.classList.contains('hidden')){
	closeModal();
}

document.addEventListener('keydown',function(e){
	if (e.key === 'Escape' && !modal.classList.contains('hidden')){
		closeModal();
	}	
});
```