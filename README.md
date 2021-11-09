# Note-App

A clean architecure note app with one single feature having presentation, use case, domain and data layer. 
Built with jetpack compose with notes tagged with different colors. 
Features clean architecture, MVVM, dependency injection, CRUD with Room and Custom View

- You can create a new note with a tagged color
- Edit and update a note
- Delete a note and Undo the action
- Order notes by various conditions (ascending, descending by date, title, color e.t.c)
- Also included are Unit, Integration and End-2-End tests



https://user-images.githubusercontent.com/40584796/139787832-28f27985-a0c3-40ef-a16e-b4afe550b2c0.mp4

// System Design Approach
- Understand the problem + requirements
  - Breakdown into functional (user should be able to publish a tweet, follow) and non functional 
    (speed, reliability, performance, scalability, high availability, low latency
    ) and be clear
  - Define boundaries for the features
    
- Handle the data
  - Client - Server communication
  - Define required endpoints  
  - Understand the data and its characteristics (model)
  - How will the data be consumed (Caching, going from domain to presentation)
  - Read or Write heavy
  - Realtime or not or push or pull
  - Define and walkthrough the appflow
    
- Discuss the components di,data,domain,use cases (boxes and arrows, Write an API for each component), 
  end up with an end to end diagram(Load balancing, Database(sharding), Caching, UI layer)
 
- Discuss the trade-offs
    - You can expand on modularity, using FCM, error handling

- Dont forget concurrency, threading, testing, bad network (workmanager), accessibility issues, phone screen issues, 
  low battery, breaking, edge cases, low ram
- Internationality (As the app grows internationally)

- Think into the future

- Principles to remember( Robustness (edge network cases, Scalability, Performance, Extensibility 
  (Adding new features), Resiliency(breaks can it recover))
    
- Put on your product manager hat

- Initially, start monolithic with clean architecture and di

Two modules
app - contains the presentation layer and framework maybe
core - contains the data, domain(could house the use cases or be a seperate package)

Importance of Clean Architecture
Code gets decoupled, easier to reuse and test
Easily onboard teammates, understand improvement

Maximizes S(Single Responsibility) O(Open-closed) L(Liskov Substitution) I(Interface Segregation) D(Dependency Inversion)

Presentation: Layer that interacts with the UI(ViewModel and View) MVVM
Use Cases: Defines actions that user can trigger
Domain: Business logic (Contains all models used, interface definition and business rules)
Data: Abstract definition of data sources(remote or database) with model classes synonymous to the api and interface implementation
Framework: Implements interaction with the Android SDK

Error Handling using a Resource class
Event Handling maybe
Testing (Unit, Integration and E2E)

Designing for accessibility


Feature based



