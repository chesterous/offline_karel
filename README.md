# One File Karel IDE

Provides an IDE for editing and running Karel code, but is completely contained in a single HTML file.

Originally started with the idea of it being used (unofficially by interested students and SLs) in code in place 2024, but might not complete it in time.

## Description

Students in Stanford Code in Place, prior to learning Python, learn a Python-like variant of Karel programming using online resources. This project tries to replicate most of the functionality of those resources, but does not require an internet connection and can be run locally.

This is getting somewhat unweildly? Weildy? Wieldy? The one file is approaching 1,000 lines of code. Attempted to encapsulate with objects like a "state" object, etc. But those efforts may have actually made it more complex. Might restructure everything at some future date.

![offline_karel_tutorial](https://github.com/chesterous/offline_karel/assets/164004822/15cb6636-28a5-48ca-b8d4-46d4d0931cad)

## TODO
* Bug fixes
    * bug on line 320, will try to fix later
    * seems to get into a state where correctness markers for code get into line strings
    * maybe when pausing in debugger or something... might fix to make this state impossible
    * if code gets into a broken state, it starts behaving weirdly
    * maybe handle broken code better (just don't run error code?)
* Features needing implementation
    * user ability to resize grid
    * maybe load in the problems from code in place (like karel helper)
* Architecture changes
    * break into multiple files and just merge for a release
    * better encapsulation, for example, playing code forward/back/etc in an encapsulated unit
* Possible future of development
    * stackless version that doesn't support for but supports function calls without recursion by inlining all functions

## Version History
* 1.0
    * function calls sort of maybe work
    * but this code is ugly and probably bug-ridden
* 0.5
    * added support for else statements and for
    * switched to generalized stack implementation
    * stack used for  function calls as well as if/while/for
    * can change styles and speed of playback
    * have separate playground mode for just calling core functions
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

