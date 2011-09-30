## Continuous Release and Deployment

* The tranditional deployment model
  * Fixed quarterly or longer schedule
  * You get feedback from clients very late
* The iteration deployment model
  * Weekly or monthly schedule
* Continuous Delivery model
  * Release every few minutes!
  * Is our code correct?
  * Is deployment safe?
  * Is our work valuable?
* What do rubyists do well? What could we do better?
* CI & Testing _really_ important
* The job of the CI system is to disprove the production-readiness of a release candidate.
* Pipeline: there should be an output from your CI build...a deliverable to the next step.
* Try to parallelize your CI pipeline.
* CI can be used for communication with customers.
* Don't have a separate deployment team.
* Use your CI to build a deployable artifact; then deploying is quicker.
* Automate until human intervention = decision
* Suggestion: don't need gcc, git, rvm in production
* Configuration management makes deployment safe
* Deploy the same thing the same way to every environment
* Deployinator from Etsy
* Deploy the right stuff
  * Small features
  * Big features with small tasks
  * Add the UI last (hard with BDD)
  * Branch by abstraction (big changes)
* With feature toggles, you can decouple deployment from release
