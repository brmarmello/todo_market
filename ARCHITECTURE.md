# Architecture

App ToDo Market

# Goal

The main purpose of this document is to organize the software development process.

# Initial Rules, Threshold and Analysis

Points to consider before introducing a new feature:

- Every project will need to respect the Lint rules written in the flutterando-analysis package.
- This project must have a minimum test coverage of at least 70%.
- Global layers must have a specific place in the application, therefore, they must be in the Shared folder.
- Each feature must have its own folder where it will contain all the layers necessary for the execution of the use cases of the feature.
- All design patterns used in the project must be listed in the “Design Patterns” section of this document, otherwise it will be considered an erroneous implementation.
- New packages and plugins can only be used in projects after evaluation and approval by the entire team responsible for the project.
- Updates to the Domain Model can only be accepted if first added to this document and approved by everyone involved in the project.
- It is not allowed to have a concrete class as a dependency of a layer. Cohesion will only be accepted with abstract classes or interfaces. With the exception of the Store.
- Each layer should have only one responsibility.

# Design Patterns

- Repository Pattern: For external API access.
- Service Pattern: To isolate code snippets with other responsibilities.
- Dependency Injection: Resolve class dependencies.
- Store: Save and change states.
- State pattern: Pattern that helps in state management.
- Adapter: Convert one object into another.
- Result: Work with multiple returns.

# External packages (Common)

- uno: HTTP client.
- result: Multiple return in Failure and Success format.
- Mocktail: For unit testing.

# External packages (App)

- flutter_modular: Route modularization and dependency injection.
- realm: Local database.

# External packages (Backend)

- shelf_modular: Modularization of routes and injection of dependencies.
- Shelf: Web server creation.
- Postgres: Data persistence.
- Redis: In-memory data persistence.
