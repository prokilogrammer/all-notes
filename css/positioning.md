# Positioning

## Floats
- *Use*: Floats are useful to make an element position automatically respecting the sizes of surrounding elements. Floats should be the _go-to_ method for positioning an element.
- *Problem*: Things go wrong when a parent element has too many floats inside it. In this case, inner floats don't respect parent's boundaries and flow outside. The parent element also shrinks to a height=0. This problem can be solved in one of two ways:

  - Overflow Technique:  Set overflow property of parent element to 'auto'. This will set proper height for the parent element. However, this can add scrollbars on some browsers. Also, it will cut off any styles that spans outside of the parent, like a box shadow.
  - Clearfix Technique: If the overflow technique doesn't work, try the clearfix approach. Here we add an imaginary table to the :before and :after pseudo-elements to keep the top and bottom borders of the parent element from collapsing. Example code:

    .box-set:before,
    .box-set:after {
          content: "";
            display: table;
    }
    .box-set:after {
          clear: both;
    }

## Position Property
- *Use*: Explicitly control an element's position. 
- *Options*: Position property accepts five different options.
    - _static_: Default value for position property. These elements don't honor any offset properties specified in them.
    - 
