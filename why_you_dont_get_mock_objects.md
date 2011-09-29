## Why You Don't Get Mock Objects

* Growing Object-Oriented Software, Guided by Tests--best book on mock
  Objects.
* Why the mock object hatred?
  * Duplicate Implementation
  * Lead to brittle tests that do a poor job
* Mock objects + procedural programming is a very bad idea
* Mocks aren't stubs
  * Mocks assert on messages
  * Stubs return values
  * Asserting on state vs asserting on messaging
* Mocking + OOP = good idea
* Objects tell objects to do things
* Messages are _more_ important than object internals.
* In OOP, behavior is found in the messages.
* Mocking && messaging allows you to change composition of the objects
  in your system.
* Key Mocking Rules:
  * Mock roles, not objects--wanting to mock concrete objects is a
    design smell. Well designed objects don't know who they are talking
    to. They should only know the role the collaborator is playing.
    When mocking roles, TDD becomes a design process.
  * Only mock types you own. If you don't own the API, there is no
    design feedback. Instead of mocking a role, your mocking an
    implementation. Duplicating your production code in your test is a
    test smell. This means don't mock boundary objects.
  * Only mock peers, not internals. Not everything belongs to a peer.
    Key question: "Is this my role?"
* Tests should respect the encapsulation of your code.
