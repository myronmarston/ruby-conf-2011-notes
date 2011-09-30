## Practical Metaprogramming

* Ruby as a message passing programming programming language
* Ruby Rogues, Ep 12: Metaprogramming
* Proposed definition: "Code that writes code", "things that treat code as data"
* Virtually all core libraries make use of Metaprogramming
* Goal: dispel FUD around metaprogramming...demonstrate that metaprogramming is "just programming"
* Let the ancestor chain guide us
* "Metaprogramming is writing code that re-directs passed messages at
  runtime OR that provides or alters structures that do said processing"
* The order you include modules determines ancestor chains
* Metaprogramming idioms
  * Tier 1:
    * Open Class:
      * Kernel Method -- adding methods to kernel to add new keywords
      * Monkey Patch
    * attr_* methods
    * Singeton methods
  * Tier 2:
    * Taking the control out of ruby's hands for handling messages
  * Tier 3:
    * Dynamic generation and inclusion of modules
    * No-holds-barred manipulation of classes and instances

