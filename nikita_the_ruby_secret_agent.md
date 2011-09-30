## Nikita the Ruby Secret Agent

* "Ruby has the best tools"--no one ever
* Ruby is a beautiful language
* People are leaving Ruby for: node.js, clojure, scala, etc
* Polyglot is the new liberal
* MRI != Ruby
* Devs are not paid to be happy...we're paid to make customers happy
* Twitter's migration from ruby to JVM. Critical issues:
  * GC
  * Concurrency
  * Performance
  * Tools
* Smalltalk _was_ an awesome language: it become irrelavant in about 18 months
* If tools are the answer, what are the questions?
  * How do I understand this code?
  * Fear of the unknown
* Solutions & Problems
  * Optional Typing
    * Ruby is about _behavior_
    * Classes organize code and support encapsulation
    * Three pillars of OO: Encapsulation, Polymorphism, Inheritance
  * Hidden Typing
    * Not in ruby, undefined or not documented
    * Hidden checks in MRI for types (i.e. to_f)
    * Types tell you what you _cannot_ do (not what you _can_ do!)
    * Like all walls, people try to defeat them
  * Refinements
    * One of the leading proposals for 2.0
    * Brian things they are a terrible idea, will "ruin" ruby
    * does not help program comprehension
    * "What if?" programming
    * horizontal vs. vertical integration
  * -w
    * `-wtf`
    * hidden in the parser
    * no ruby objects
    * not programmerable or configurable
    * no real semantic analysis
* Rubinius Foundations
  * Generational GC
  * Concurrency
  * JIT compiler
  * Tools
* Rubinius GC
  * Precise
  * Generational
  * Copying compaction
* Concurrency
  * Fully concurrent ruby threads
  * concurrent vs parallel--concurrent could be time slicing w/o true
    parallel
  * hipster Actors
  * JIT Fast--order of magnitude
* Rubinius implements ruby differently
* Rubinius uses ruby to create a consistent system
* homoiconic: same symbol--to_ast, to_sexp
* Everything is a `CompiledMethod`
* Nikita
  * Brian's idea of a tool
  * Client/Server, available as a gem
  * CompiledMethod database
  * Coverage/profiling
  * Bytecode instrumentation
  * AST transformation
  * Debugging
  * Documentation
  * Analysis
