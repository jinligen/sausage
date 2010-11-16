Sausages
===========

A contextual pagination jQuery plugin for infinite scrolling pages. Early days--pretty rough at the moment. Check the demo!

The goal of this project is to contextualize the infinite scrolling experience. Rather than have the user scroll into a bottomless pit, provide instant feedback when pages are added and allow for navigation to previously viewed pages.

A Picture!
--------------

![Alt text](http://s3.amazonaws.com/forrst-production/posts/snaps/39102/original.png?1289710907)

Demos
--------------

- [Basic](http://christophercliff.github.com/lazypages/demos/basic.html "Basic")

Requirements
-------------

- jQuery 1.4.3
- jQuery UI 1.8.5

Usage
-------------

    $('.myPages')
        .sausages()
        ;

Presumably, you have some callbacks available for lazy loading additional data. If that's the case, you can do the following:

    ...
    startLoadingSomeData: function () {
    
        $('.myPages')
            .sausages('block')
            ;
    
    },
    gotTheDataAndUpdatedTheDOM: function () {
    
        $('.myPages')
            .sausages('draw')
            .sausages('unblock')
            ;
        
    }
    ...

Future development/TODOs
-------------

- Graceful degredation/cross-browser compatibility
- Customizable tooltips (e.g. page name, thumbnail, etc.)
- Blocking
- BUG: alignment gets progressively worse as pages are added, need to investigate...
- <strike>Highlight the current page</strike>
- Scale to 100+ pages (&#8734; pages!?!?)