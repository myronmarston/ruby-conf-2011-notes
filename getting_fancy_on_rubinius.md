## Getting Fancy on Rubinius

* Motivation:
  * A language & implementation that is:
    * Easy to understand and extend
    * Consistent (no "magic")
    * Well documented
    * Noob friendly
    * Without ambiguities (syntax & semantics)
* Inspirations: Smalltalk, Ruby, IO, Erlang
* Smalltalk:
  * OO
  * Pure message passing semantics
  * Limited syntax and special keywords
  * Dynamic
  * Class based
  * Reflective
* Ruby:
  * More than one way to do it
  * File based
  * Embrace unix
  * Similar literal syntax
  * Naming conventions
  * It's a script! (Class / Method defs)--all contexts are executable
* IO/Erlang:
  * Lock-free concurrency using:
    * Async message sends
    * Futures
    * Actors
* Async & Actors
  * Any object can be an actor
* Ruby Integration
  * Explicit syntax for calling out to ruby methods
* Has FSpec like RSpec
* Has Dynamic scoping
* Most syntax gets compiled into dynamic message sends that are executed at runtime
