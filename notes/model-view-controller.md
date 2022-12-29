---
tags: computer-science software-architectural-pattern
---

# Model view controller (MVC)

**Model-view-controller (MVC)** is a software architectural pattern that splits program logic into three separate but connected elements - the _model_, _view_, and _controller_.

- commonly used for building [[user-interface|user interfaces]], web applications, and other types of programs.

## Components

### Model

The **model** is the central component. Often it is a dynamic data structure, independent of any UI. It directly manages data, logic, and rules for an application.

An example of a model in a web application would be an application's database, or a table within a database.

### View

The **view** is any representation of information visible for the user. In most cases, these are elements in a user interface that usually allow for user input.

In web applications, these are often [[hypertext-markup-language|HTML]] pages or templates that involve [[web-rendering|web rendering]] for users to see the data.

### Controller

The **controller** accepts input and converts them into specific commands or actions for the model or view.

In web applications, these could be functions that accept requests and return web responses, and even affect the view by using HTML templates. Oftentimes, the controller contains [[algorithm|algorithms]] for business logic.

## Interactions

MVC defines these interactions:

- the model is responsbile for managing the data of the application. It receives user input from the controller
- The view renders presentation of the model in a particular format.
- The controller responds to the user input and performs interactions on the data model objects.
  - The controller receives the input, optionally validates it and then passes the input to the model.

## Sources

- <https://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller>
