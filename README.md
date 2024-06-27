# Flexbox

https://internetingishard.netlify.app/html-and-css/flexbox/index.html

https://flexbox.malven.co/

https://www.joshwcomeau.com/css/interactive-guide-to-flexbox/

Flexbox info

flex is shorthand for flex-grow, flex-shrink, and flex-basis.

flex: 1; === flex-grow: 1, flex-shrink: 1, flex-basis: 0 === flex: 1 1 0;

~*Flex-grow*~ expects a single number as its value and that number is used as the flex-item's growth factor. 

flex:1 tells every div to grow the same amount. (Every div always ends up the exact same size)

flex:2 added to one of the divs tells that div to grow 2x the size of the others.

etc.

~*Flex-shrink*~ is similar to flex-grow but instead of setting the growth factor, it sets the shrink factor. And it is only applied when ALL flex items are larger than their parent container.

flex-shrink:0 === item will -not- shrink.

flex-shrink:1 === all items shrink evenly.

flex-shrink:2 === items shrink 2x faster.

etc.

~*IMPORTANT*~ When you specify -flex-grow- or -flex-shrink-, flex items do not necessairly respect your given values for width. They will grow or shrink to fill their parent container.

~*Flex-basis*~ sets the baseline size of a flex item. Any flex-growing or flex-shrinking starts from the flex-basis initial size.

flex-basis: auto === default value BUT if you set flex: 1 on an item, it is interpreted as flex: 1 1 0. You can use flex: 1 1 auto === flex: auto.

If flex-basis is set to 0% all flex items will shrink evenly.

If flex-basis is set to auto all flex items check for a width declaration.

~*Flex: auto*~ 
flex:auto === flex-grow:1, flex-shrink:1, flex-basis:auto === flex: 1 1 auto.

~*~*~*~*~*~*~*~*~*~*~

Flexbox can work either horizontally or vertically. 

flex-direction: row === horizontal (default) main axis === horizontal
flex-direction: column === verticle main axis === verticle

using flex: 1 with flex-direction: column sets flex-basis to 0, which means that all flex-growing and flex-shrinking would beging from 0. Use flex: auto or flex:1 1 auto.

'using flex: 1 with flex-direction: column sets flex-basis to 0' === this happens because when flex-direction: column flex-basis refers to height instad of width.

~*~*~*~*~*~*~*~*~*~*~

~*justify-content*~ aligns items across the **main** axis 
~*align-items*~ aligns items across the **cross** axis

Because *justify-content* and *align-items* are based on the main and cross axis of the parent container, their behavior changes when you change the flex-direction.

flex-direction: row === justify-content aligns horizontally
                        align-items aligns vertically

flex-direction: column === justify-content now aligns vertically
                           align-items aligns horizontally