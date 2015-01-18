# Flexbox

It is the latest W3C standard attempting to unfuck what CSS fucked up - layout elements. It aims at distributing and aligning space among items in a container when their sizes are unknown/dynamic.

Checkout http://css-tricks.com/snippets/css/a-guide-to-flexbox/ for an excellent, visual and concise description of Flexbox.

## Flexbox Options

### Options on Container

1. _display: flex_: Defines the flex container
2. _flex-direction_: Defines the direction in which items inside the container will be laid out. Establishes the "main axis".
3. _flex-wrap_: Can the items be wrapped to next row or should they be shrunk to fit it on row
4. _justify-content_: How should the items in each line be distributed?
5. _align-items_: This is like justify_content but for the cross-hair axis. How should the items be distributed along the cross-hair axis?
6. _align-content_: How should the different lines of items be distributed along the cross-hair axis?

### Options on Items

1. _order_: Order in which items must be laid out. Items inside a flex container need not be displayed in code order. This property controls the ordering
2. _flex-grow_: Defines the ability of an item to grow within the container. Items inside flex container grow proportional to the value specified.
3. _flex-shrink_: Same as flex-grow but for shrinking
4. _flex-basis_: Base height/width of the container before growing or shrinking. 
5. _flex_: Combines flex-grow, flex-shrink and flex-basis
6. _align-self_: Override parent's align-items value for this specific element
6. 