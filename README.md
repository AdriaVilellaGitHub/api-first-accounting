# api-first-accounting
The first API Accounting System

## Objectives

Provide an API First Accounting System for any kind of legal entity incorporated into virtually any country of incorporation.
For now, I'm doing it just for fun!

## Development and deployment considerations

- I'm developing this project using Agile methodologies and disciplines as SCRUM and Test-Driven Development.
- The architecture of the project will be based on a clean hexagonal architecture.It helps me define decoupled code structure, isolated with external components and easy-to-run tests.
- Cloud-native solution available to deploy in any public, private or hybrid cloud as well as on-premises.
- Container based deployment, allowing it to run in a wide range of hosts/OS.
- 100% test coverage of the base code.
- Fully documented for both technical and business stakeholders.
- Infrastructure as a Code for automated deployment.
- Framework and database agnostic.


## Business requirements

- Easy to use
- Adaptable to the specifications of each sector
- Modular: Financial, Analytical and budget accounting, treasury, and so on.
- High performance at the minium possible cost in terms of resources.
- High availability and disaster resilient.

## Development stack

- Programming language: Python or Go
- Unit Test: Pytest or testing package
- E2E testing: Postman / curl
- CI/CD: GitHub actions
- IaaC: Terraform
- API framework: FastAPI or Echo
- Cloud provider: AWS first, Google and Azure later.

# Hexagonal Architecture

In an hexagonal architecture, everything is surrounding the core of the application. It is a technology agnostic component that contains all the **Independent Business Logic**. The existence of other things in the outside should be completely ignored. In other words, the core is not aware of how the application is served or where the data is actually hold.

## Project structure

- **core** folder: It contains all the core components (services, domain and ports). 
  - **domain** folder: It contains the model's definition of each entity that is part of the domain problem and can be used across the application. The independent business logic.
  - **ports** folder: It contains the interfaces definition used to communicate with actors.
  - **services** folder: The services are our entry points to the core and each one of them implements the corresponding port. They are the use cases that our application considers.

- **handlers** folder: Here goes the implementation of the driver adapters so the application can interact with the actors. Our service is going to be served via http (API REST). Therefore, this driver adapter must be capable of transform an http request into a service call.

- **repositories** folder: The models are going to be saved somewhere: in an “in memory” key value store, in a database, in text files, etc. This driven adapter must satisfy the *ports.XYZ* interface.

# Business definitions

- **Accounting entry**
- **Line entry**
- **Chart of accounts**
- **General Ledger**
- **Assets and Liabilities**
- **Profit and Loss**
- **Trial Balance**
- **Balance Sheet**
- **Balance Accounts**
- **Operating Accounts**
- **Accounting account**
- **Journal or Accounting Journal**
- **Ledger**