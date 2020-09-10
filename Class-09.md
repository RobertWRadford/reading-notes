# Forms and JS Events

## HTML/CSS Chapter 7 "Forms" pg 144-175

Form internal process is as follows:

1. The user fills in a form a submits
2. The name of each form and the entered value with it
3. The entered values are processed through script/code
4. Updates to the page or a new page are pushed based on the information received

```HTML
<form action="http://www.google.com" method = "get">
  <p> Form controls will appear here
    <input type="text" name="username" size="24" maxlength="24" />
  </p>
  <p> more can appear in one form tag
    <input type="password" name="password" size="24" maxlength="24" />
  </p>
  <p> How do you feel about this? </p>
    <textarea name="feedback" cols="20" rows="4">express it in the text box made here</textarea>
  <p>Rate your experience from 1 to 5 please
    <input type="radio" name="rating" value="1" checked="checked" /> 1
    <input type="radio" name="rating" value="2" checked="checked" /> 2
    <input type="radio" name="rating" value="3" checked="checked" /> 3
    <input type="radio" name="rating" value="4" checked="checked" /> 4
    <input type="radio" name="rating" value="5" checked="checked" /> 5
  </p>
  
</form>
```
there are more form options as well, such as checkbox which allows multiple simultaneous selections, dropdown lists, and more.

You can use <label></label> to categorize input element

You can also use <fieldset> </fieldset> to encapsulate a collection of form controls


## HTML/CSS Chapter 14 "Lists, Tables & Forms" pg 330-357

list-style-position is a property for lists that can take inside or outside as values, and dictates whether or not the list item symbol is a part of- in otherwords whether or not it is "inside"- the word block so the next line would wrap underneath it.

:focus can be used to effect something while it is in use; and :hover can do the same thing when the user hovers over them

## JS Chapter 6 "Events" pg. 243-292

event types include:

*load - web page finishes loading
*unload - webpage is unloading; f.e. when a new page is requested
*error - browser encounters a JavaScript error or an asset doesn't exist
*resize - Window has been resized
*scroll - user scrolled the page vertically
*keydown - user presses a key; repeats while key is depressed
*keyup - User releases a key
*keypress - character is being inserted; repeats while key is depressed
*cick - user clicks and releases over the same element
*dbclick - user clicks and releases over the same element twice in succession
*mousedown - user clicks while over an element
*mouseup - user releases click while over an element
*mousemove - user moves the mouse; won't work with touchscreen
*mouseover - user moves the mouse over a specific element; not touchscreen
*mouseout - user moves mouse off an element; not on a touch screen

an event can be bound to an element, through HTML handlers such as a tag for body including onresize="" and some procedure, a DOM event handler, or an eventListener() DOM parameter

since you cannot directly pass parameters with event listeneres, a work around is typically used, f.e.

```JavaScript
var fishPicture = document.getElementById('fishPic');
var fishDimensions = fishPicture.getBoundingClientRect();

function setCenter(width, eleID){
    var windowSize = [window.innerWidth, window.innerHeight];
    var pushAmount = (windowSize[0] / 2) - (width/2);
    var elementToPush = document.getElementById(eleID);
    elementToPush.style.left = pushAmount+"px";
}

fishPicture.addEventListener('resize', function() {
  setCenter(fishDimensions.width, 'fishPic');
}, false);
```

ie 8 and older versions do not support event listener format or the getBoundingClientRect() method used in the previous example so common practice if the page must be compatible with old IE versions as well is to make fallback event handlers like so

```JavaScript
var fishPicture = document.getElementById('fishPic');
var fishDimensions = fishPicture.getBoundingClientRect();
var fishDimensionsOld = fishPicture.offsetWidth;

function setCenter(width, eleID){
    var windowSize = [window.innerWidth, window.innerHeight];
    var pushAmount = (windowSize[0] / 2) - (width/2);
    var elementToPush = document.getElementById(eleID);
    elementToPush.style.left = pushAmount+"px";
}

if (fishPicture.addEventListener) {
    fishPicture.addEventListener('resize', function() {
    setCenter(fishDimensions.width, 'fishPic');
    }, false);
} else {
    fishPicture.attachEvent('onresize', function() {
    setCenter(fishDimensionsOld, 'fishPic');
    });
}
```


