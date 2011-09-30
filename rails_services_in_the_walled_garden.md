## Rails Services in a Walled Garden

* They've migrated a monolithic rails app to 9+ services
* Walled Garden: services that are only used internally--gives them far
  more control.
* Why SOA?
  * map to biz verticals
  * independent evolution and deployment
  * scale out only what is in demand
  * easier to maintain
  * smaller, independent codebases
  * small teams
  * disadvantages:
    * chattiness
    * decreases performance!
    * ACID transactions are difficult
    * API versioning
    * continuous integration across multiple services is difficult
* Why rails?
  * easy to create APIs
  * powerful routing
  * mime-type negotiation
* Walled garden?
  * inside the garden is easy(er)
  * full HATEOAS is expensive
* rails does RMM 2(.5)
* areas of interest
  * authentication
    * transparent service orchestration
    * must be stateless--can't use cookies
    * easiest: firewall
    * central auth service--OAuth 2
  * authorization
    * user roles--many gems
    * roles over HTTP are difficult
    * centralized roles and federated rules
  * chattiness
    * performance build--SLA for your services
    * caching: HTTP 304 is your friend
  * pagination
    * model collections as collection resources
  * observer pattern
    * callback URIs--many problems
    * message queue--a centralized bus w/ registered listeners
  * API versioning
    * easier in a walled garden--communication is key
  * atomic transactions
    * two phase commit
  * engineering
    * standardization
    * treat comon code like any other library
    * api vs html
    * configuration management--let Chef/Puppet manage it
