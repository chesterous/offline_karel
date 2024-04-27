# One File Karel IDE

Provides an IDE for editing and running Karel code, but is completely contained in a single HTML file.

## Description

Students in Stanford Code in Place, prior to learning Python, learn a Python-like variant of Karel programming using online resources. This project tries to replicate most of the functionality of those resources, but does not require an internet connection and can be run locally.

## TODO
* Features needing implementation
    * if/else
    * for
    * function calls with recursion
    

## Version History
* 0.4
    * support for while and if and most conditionals
    * conditionals not tested, may contain obvious bugs
    * supported conditions:
        * (front/left/right)_is_(clear/blocked)
        * (no_)beepers_present
        * (not_)facing_(north/south/east/west)
    * unsupported:
        * (no_)beepers_in_bag()
    * code still kind of messy
* 0.3
    * hideous code to support... writing code
    * frankenstein of different programming methodologies
    * commented out sections
    * now can write the few built-in function calls and run them
    * still buggy, still doesn't support loops or conditionals
* 0.2
    * Minor Updates
    * Click to add/remove beepers from map
    * Displays history
    * Keyboard shortcuts
        * u: undo
        * r: redo
        * w: pick beeper
        * s: put beeper
        * d: move
        * a: turn_left
* 0.1
    * Initial Release
    * Supports move, turn_left, put_beeper, pick_beeper
    * Code not clean or well debugged
    * Only shows errors in console
    * Does not gray out buttons that can't be used

## Acknowledgements

* [Code in Place](https://codeinplace.stanford.edu/)
* [Intro to the Karel variant](https://compedu.stanford.edu/karel-reader/docs/python/en/intro.html)

