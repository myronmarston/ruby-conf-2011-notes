## Laser

* Static analysis in ruby
  * Find errors and style issues
  * Find properties of a program w/o running it
  * Uses:
    * optimization
    * error discovery
    * statistical analysis
  * Loop inference, constant propagation, type inference, exception
    inference, dead code elimination, etc
  * Everything is undecidable!
  * ...but what can we do in ruby?
* Example: block use detection
  * required
  * ignored
  * optional
  * foolish
* No one writes `yield if halting_problem(M, x)`
* Two challenges:
  * metaprogramming
  * flow analysis
    * clearly needed in block usage example
* Analyzing Metaprogramming:
  * Easy: just run the top-level code
  * run until you hit I/O
  * capture global state changes--new classes/methods
  * Is this enough?
  * How many methods to you add after time t?
* Flow analysis
  * Flow-sensitive vs. Flow-insensitive (i.e. ruby -w)
  * Flow-sensitivity makes _all_ analysis better
  * Laser's major contribution
  * Builds a control-flow graph for ruby code
* Control-flow graphs
  * representation of program
  * graph of basic blocks--blocks of code that are uninterrupted
  * Small instruction set
* Statis single assignment
  * every variable assigned only once
  * key point: distinguishes variables w/ same name, assigned on
    different code paths
  * gives us flow sensitivity!
* Uses cartesian production algorithm
  * Conservative: doesn't miss anything, but may find extra types that
    aren't actually possible
* Detects:
  * unexpected return types
  * unused methods
  * unused variables
  * block usage
  * finds many guaranteed raises
* There are things that laser will be wrong about.
