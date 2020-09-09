# More CSS Layout

## HTML/CSS Chapter 15 "Layout" pg. 358-405

Block level elements in HTML start a new line where as inline elements flow between text.

When a block level element contains another block level element the figurative box around both elements is referred to as the containing or parent element.

CSS has the following positioning schemes to control the layout of the page: 

* Normal Flow
  *Every block level element appears on a new line, in order of when they were added
* Relative Positioning
  *Moves an element from the position it **would** be in, shifiting it in any direction.
* Absolute Positioning
  *Positions the element in relation to its containing element, and ignores individual block level elements. Moves as the user scrolls up and down the page
  
Additionally there are box offset properties to tell the browser how far to push the element

Fixed positioning is a form of absolute positioning that positions the element in relation to the browser window, as opposed to the cointaining element.

Floating elements lets you take an element out of normal flow and position it to the right or left of a containing box. The floated element becomes a block level element around which other content can flow.

the z-index property can be used to control whether elements sit on top of eachother or not, higher numbers being closer to the front.

you can set float and a width and margin value to designate more specific space.

960-1000 pixels wide is an industry common goal for webpages.

You can use @import to link to a single style sheet within HTML but access multiple
