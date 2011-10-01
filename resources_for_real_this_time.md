# Resources, for Real this Time

* 5 months ago, Sean said Rack/WSGI is broken
  * Response: "It ain't broke if people make it work"
* History of Ruby & HTTP:
  * CGI, SCGI, FCGI
    * shell/fork, setenv, exec
    * used stdin/stdout
  * WEBrick
    * a standalone server
    * "servlet" interface
  * Rails!
    * MVC!
  * Rails 1.2ZOMGREST!
    * Two voices in the wilderness:
      * Scott Raymond: doing REST Right--RailsConf '07
      * Ben Scofield: All I really need to know I learned by writing my
        own web framework (RubyConf '08)
  * Sinatra
    * Rails is too heavy, let's go raw
    * Built on rack
* Inside Rack
  * Servers/handlers
  * Middleware
  * Applications
* What Rack promises:
  * Composability
  * Simple interface
  * Separation of Concerns
* Why Rack is Broken
  * Blind up, blind down:
    * Only tools are `env` going down, return tuple going up
  * `env` is a dumpster
  * Communicate by convention (not contract)
  * Middleware order matters
  * High coupling
* HTTP is hard
  * Is the request method allowed?
  * What media-type to return?
  * Is the response cacheable?
  * Did the resource move?
  * Where should the logic live to answer these questions? App?  Middleware?
* HTTP doesn't change, only your resources.
* Encapsulate those hard decisions and reuse them.
* Let's shape our applications like HTTP, with resources.
* A resource is:
  * Data or Service
  * Identified by URI
  * Representations
  * Other variances/properties
* Introducing WebMachine: Doing HTTP Better
  * A toolkit for easily creating well-behaved HTTP applications.
  * An executable model of HTTP
* Shaped like HTTP
  * Declare resources, don't perform actions
  * Negotiate hard decisions transparently
  * Respond with the right status code
  * Sensible default behaviors
* Not a framework!
  * No ORM
  * No template system
  * No "plugins"
  * No "asset pipeline"
* Resource-focused
  * Resources are the core building block
  * Classes define "resource families"
  * Well-defined interface to HTTP logic
  * URIs map to resource families
  * 36 resource "callbacks"
* Simple dispatching
  * Break path into segments
  * Bind segments to symbols
  * Trailing "wildcard" to match varaible segments
  * Route-specific "static" bindings
