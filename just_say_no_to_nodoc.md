## Just Say No to :nodoc:

* Goals:
  * Why Documentation Matters
  * The elements of good and bad docs are
  * How Tools Make it Easier
  * Use Docs to improve your APIs
* Protocols
  * How machines communicate with each other
  * Codified contracts for machines
  * Docs are a codified contract
* "Contract" sounds rigid and harsh...but we love them
* Specs are geared for your system, not for end users
* Documentation Smells
  * Complicated return values
  * :nodoc:
    * It's not all bad
    * It's just heavily abused
      * Used to forcibly hide public methods
      * Hiding documentation
* You should decide what to hide when you generate docs, not when you write it.
  * Like separation of HTML and CSS
* Ambiguitiy sucks
  * Not important
  * "I don't care enough to tell you"
  * or not yet documented?
* Elements of good docs
  * Describe the behavior
    * Avoid 1st person pronouns (no "we" or "I"; "you" is OK)
    * First sentence should summarize the method or class
    * Leave out implementation details unless they affect usage
  * Examples! (@example)
  * Mention any usage caveats (through @note)
  * References (classes, methods, URL, @see)
  * List acceptable parameters and return types
    * multiple types and ducktypes are fine
* Types
  * Param names don't tell full story
  * A "type" is not only a class.  duck-types are types
* Tools
  * can remove duplication
  * rspec and cucumber plugins
  * can audit code
* Next level API design
* Document Driven Development
* README Driven Development--different from DDD. It's a subset of DDD.
* RDD is about planning ahead
* DDD: "Write, Validate"
* Codifying the API
  * Tells us when our API sucks
  * Let's us improve our API
* A lot of APIs can be improved by examining how easy it is to explain them.
