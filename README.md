# MEAN STACK
*Building a media watch list application*  
## ANGULAR

- Parts that you use to write applications in Angular:
![ANGULAR components](/images/angular1.png)  
- Angular is built upon ***components***. 
- The starting point of an Angular app is the bootstrapping(like the HTML DOM tree) - Angular runs on a component tree model. 
- After Angular loads the first component with the bootstrap call, it then looks within that component's HTML view and sees if it has any nested components. 
- If so, Angular finds matches and runs the appropriate component code on those. This repeats for each component down the tree. 
![ANGULAR components img 2](/images/angular2.png)  
- *A component in Angular is used to render a portion of HTML and provide functionality to that portion*.  
-  It does this through a ***Component class*** in which you can define application logic for the component. 
- For example, you can have a MediaItemComponent that can have a property named mediaItem that represents the data for a mediaItem.   
  And that component can also have a method called onDeleteClick that can handle raising the delete mediaItem event.  
  With each component in Angular, you can ***specify an HTML template***, the markup that will get rendered. And through the use of the Component class and how Angular renders the component, you can display the data for the mediaItem property in your template.  
  And Angular provides an easy syntax, known as the ***template syntax***, to wire up to DOM events within your template. So you can wire up the click event on a button to the onDeleteClick method.  
![ANGULAR components img 2](/images/angular3.png)  

- You can even use ***components within components***. This is where the component tree comes into play. You can build out your Angular apps by having components rendering components within their templates.  
- Each component gets configured with a ***selector***, which tells Angular what markup element tag to associate the Component class logic with. *When you build a component in Angular, you are creating support for a new custom element for the DOM*.  
### Directives and Pipes
#### Component
Components are actually directives with a template. *Directives provide functionality and can transform the DOM.*
- Structural Directives - modify layout by altering elements in the DOM. 
- Attribute directives - change the behavior or appearance of an existing DOM element.  
You can applying directives to an existing element, or a template element, to change that element in some way.  
![ANGULAR components img 2](/images/angular5.png)  
Like a component, a directive gets configured with a selector that Angular will use to find a match and apply the directive.  
You apply a directive in different ways. You can write an attribute on an element that matches your selector,  
or you can use the template syntax to add a directive and an assignment statement.  
![ANGULAR components img 2](/images/angular6.png)   
In addition to creating your own directives Angular comes with a number of directives out of the box to handle common web app constructs by conditionally rendering elements based on some expression1(```ngIf```), looping out items to render(```ngFor```), or even for things like router links (```routerLink```).  
#### Pipe
Another tool in the Angular toolbox to display content is the pipe. A ***pipe*** takes in data, like a string or an array, and runs some logic to transform it to a new output.  
Angular comes with some common pipes like date, and uppercase and lowercase.  
You can also write your own pipes.  
*Pipes are a great way to change data in a reusable way without having to imbed the transformed logic within component classes. And without having to modify the data just for display purposes*.  
### Data Binding
- You can bind data to views and work with data in those views via ***interpolation***, - ```<h1>{{ movie.title}}</h1>```.  
- You can also use directives to help display data. Use the ***template syntax*** in Angular to work with data in views.  
You can wire up click events to DOM elements that modify data that you've displayed elsewhere and Angular will handle the update of that data visually.  

There are many elements to the template syntax. 
- interpolation and built-in directives
- constructs and patterns
  - Template expressions and statements
  - Value binding - binding syntax for property, attribute, class, and style bindings
  - Event binding
  - Template expression operators.  

You can also create and use local template variables created in markup using the hash to get a reference to the element and then use that from any sibling or child element in the view.  

This allows you to wire up simple interactions or display related data from within your markup without needing to write any script code.  
![ANGULAR components img 2](/images/angular7.png)  
- Now when it comes to collecting data from the user, Angular has a form module loaded with directives and services for helping you build HTML forms.  
  It provides:
  - data binding for both setting and getting data
  - change tracking
  - validation
  - error handling  

### Dependency injection
- Angular brings dependency injection to JavaScript. 
- ***Dependency injection (DI)***is the concept of *inversion of control (IoC)*, where you architect code in a way that you provide modules with other modules it needs to get some work done.
- DI allows you to write decoupled code that is easier to unit test and to work with. 
![ANGULAR components img 2](/images/angular8.png)  
- You can write modular components, and services and tell Angular what/where you want to use them. 
![ANGULAR components img 2](/images/angular9.png)  
- The most common place you use DI is in your class constructors.  
  - components
  - directives
  - pipes
  - services
- You can declare types on your constructor parameters with TypeScript.
- You can also leverage DI through 
  - component metadata,
  - properties, for directives and providers. 
- You can even do some DI at the bootstrap phase of an Angular app, setting up your dependency graph when your app starts up, and getting that delivered through all aspects of your app. 
- You can replace a dependency at any phase of application code.  

### Services and other business logic
- *Services in Angular are more of an implied pattern*. A JavaScript class or function that is encapsulated is refered to as a service in Angular. 
- Put application business logic in services.  
***Example:***  
You can write a JavaScript class that handles finding the record data and returning it as an object. This would be a service. And then, using Angular's DI framework, you can specify that a component is going to use this service. And from within the component logic, you can request the a data record from your service and make it available to your view template.  
- These services that you write can also leverage DI, so you can create constructors and specify parameter types, with the help of some TypeScript, and Angular will provide your service instance with the appropriate dependencies.  

