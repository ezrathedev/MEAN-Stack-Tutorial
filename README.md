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