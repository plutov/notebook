## CI / CD

### Good Practices

- Fail a build when a project rule is violated – such as architectural breaches, slow tests, and coding standard violations.
- Send automated feedback from CI system to all cross- functional team members.
- Write build scripts that are decoupled from IDEs. These build scripts are executed by a CI system so that software is built at every change.
- Provide large visible displays that aggregate information from your delivery system to provide high quality feedback to the Cross-Functional Team in real time.
- Automate the verification and validation of software to include unit, component, capacity, functional, and deployment tests.
- Run multiple tests in parallel across hardware instances to decrease the time in running tests.
- A deployment pipeline is an automated implementation of your application’s build, test, deploy, and release process.
- Fail the build as soon as possible. Design scripts so that processes that usually fail run first. These processes should be run as part of the commit stage.
- Build your binaries once, while deploying the binaries to multiple target environments, as necessary.
- Provide an automated single command rollback of changes after an unsuccessful deployment.