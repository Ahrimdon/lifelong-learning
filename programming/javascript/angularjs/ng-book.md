# ng-book. Reference repo: `angulearn`

AngularJS features: Separation of app logic/data models/views, Ajax services, dependency injection, browser history, testing.

JQuery, extend the custom JS objects and manipulate DOM from outside. Angular adds shit to HTML to give it native MVC capabilities. So you can encapsulate a portion of the web page as one application rather than forcing the entire page to be an entire app.

As opposed to Rails, Angular create live templates -- `ng-app declares that everything inside of it belongs to a specific Angular app. Controller doesn't have to worry about rendering the view.

We bind `name` attribute to the input field using the `ng-model` directive on the containing model object (`$scope`).

This is just bi-directional binding in the view. For back-front end, we have to use Controllers. Declaring `ng-controller` attribute on a DOM element means that all the elements inside it belong to this controller.

The controller function takes one parameter, the `$scope` of the DOM element. This `$scope` object is available on the element and the controller and is the bridge by which we'll communicate from the controller to the view.

## Modules

Module - where you put the application code. An app can contain several module, each one containing code for a specific function.

Why?

- Cleaner global namespace
- Tests are easier to write
- Easier to share code between applications
- Allow app to load different parts of the code in any order

Defining a module (setter):

    angular.module('myApp', []);

Fetching an app (getter):

    angular.module('myApp')

Properties: `name` and `requires`

## Scopes

Scope = execution context for the expressions. This is where we define the biz functionality of the app, methods in the controllers, and properties in the views.

Just before out app renders the view to the user, the view template links to the scope, and the app sets up the DOM to notify Angular for property changes.

Scope = source of truth for the application state. Live binding means `$scope` can be updated immmediately when the view modifies it.

