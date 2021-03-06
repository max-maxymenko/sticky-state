#StickyState

StickyState ads state to position:sticky elements and also polyfills the missing native sticky feature.

todays browser do not all support the position:sticky feature (which by the way is beeing used (polyfilled) on pretty much every site you visit) - moreover the native supported feature itself comes without a readable state. something like a:hover => div:sticky to add different styles to the element in its sticky state - or to read the state if needed in javacript. 

unlike almost all polyfills you can find in the wild StickyState is high perfomant. the calculations are reduced to a minimum by persisting several attributes.

###Dependencies
none!

###Browser support
IE >= 9, *

###install
```
npm install sticky-state
```
### demo
https://rawgit.com/soenkekluth/sticky-state/master/examples/index.html

###css
your css should contain the following lines: 
(you can specify the classNames in js)
```css
.sticky {
  position: sticky;
}

.sticky.sticky-fixed.is-sticky {
  position: fixed;
  backface-visibility: hidden;
}

.sticky.sticky-fixed.is-absolute {
  position: absolute;
}
```

###js
```javascript
var StickyState = require('sticky-state');
new StickyState(yourElement);
// or for all elements with class .sticky
StickyState.apply(document.querySelectorAll('.sticky'));
// for example
```
###React Component
https://github.com/soenkekluth/react-sticky-state
