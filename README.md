# One File Karel IDE

Provides an IDE for editing and running Karel code, but is completely contained in a single HTML file.

Originally started with the idea of it being useful for people in Code in Place 2024.

## Description

Students in Stanford Code in Place, prior to learning Python, learn a Python-like variant of Karel programming using online resources. This project tries to replicate most of the functionality of those resources, but does not require an internet connection and can be run locally.

This is getting somewhat unweildly? Weildy? Wieldy? The one file is approaching 1,000 lines of code. Attempted to encapsulate with objects like a "state" object, etc. But those efforts may have actually made it more complex. Might restructure everything at some future date.

## Contact Me

People wanting to help out, or suggest things, or whatever, can create an account on coproductional. I'll eventually setup an account there. I didn't put any contact info here because I assumed there was some way to contact people on github. That appears to not be the case. Coproductional is supposed to have more people eventually. I don't know. But you can try anyway and post something on it, I guess. I'll get around to doing something on there related to programming, maybe? Or maybe check back here later. I may eventually create a website or put some other contact info here.

* [Coproductional social media](https://coproductional.com/)

## Introduction

Some features:

* Like the official editor, can play code forwards and backwards
   * controls are: "rewind", "play in reverse", "step back", "pause", "step forward", "play", "fast forward"
   * includes speed control for playing code forward and reverse
* Has a "playground" mode for just executing single commands
* Can click the field to add or remove beepers
* Has different styles to choose from
   * all suspiciously similar to a Super Nintendo game, however

![offline_karel_tutorial](https://github.com/chesterous/offline_karel/assets/164004822/15cb6636-28a5-48ca-b8d4-46d4d0931cad)

## TODO
* Bug fixes
    * seems to get into a state where correctness markers for code get into line strings
    * maybe when pausing in debugger or something... might fix to make this state impossible
    * if code gets into a broken state, it starts behaving weirdly
    * maybe handle broken code better (just don't run error code?)
* Features needing implementation
    * user ability to resize grid
    * forgot to add a count if there are multiple beepers on a square
    * maybe load in the problems from code in place (like karel helper)
    * probably make it more resilient by giving error messages or something
    * syntax highlighting might be nice...
       * but would have to change the textarea-style implementation
       * so, not sure if it's worth it
    * maybe implement the bag functions? (not sure if deprecated)
       * i.e. beepers_in_bag() and no_beepers_in_bag()
    * corner functions WON'T be implemented, since they seem deprecated
       *  i.e. paint_corner(COLOR_NAME) and corner_color_is(COLOR_NAME)
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

(corner color functions seem to be deprecated)

