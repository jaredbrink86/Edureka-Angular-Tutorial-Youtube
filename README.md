## Edureka-Angular-Tutorial-Youtube

### Angular Basics 

-----

Understand use of all the files.
Component tree structure 
How to add components 
Understand how to manipulate typescript and html 

### Understand Data Binding 

1. Interpolation - Component to DOM binding. Example: Send the variable name defined in TypeScript to HTML using {{}} braces. 


2. Property Binding - SImilar to interpolation i.e. component to DOM binding. Send the string or value to particular property. 
Define property as 
<img [src] = imagePath alt="">
where src is the property enclosed in []. 
Now imagePath is defined in the typescript file and can be used to extract the value. 


3. Event Binding - DOM to component. Example Button. 
<button type = "button" name = "button" (click) = "changeValue()">Value Badal</button>
Example here onclick of button an changeValue() function is called defined inside TYpeScript file. 
() used to defined event. 


4. twoWayBindings - The change is simultaneous in both directions. It can be considered as a combination ofproperty binding and event binding. 
The two way binding is defined as follows - 
<input type="text" [(ngModel)] = "twoWayData" [value]="twoWayData" name="" value="">
  {{twoWayData}}

-----

### Directives - 

-----

Directives allow you to manipulate your DOM. 

Types of directives - 
1. Component - Directive with a template. 
2. Structural Directive - Add or delete DOM elements and changing DOM layout. 
3. Attributes Directive - Change the attributes(Apperance or behaviour example background colour, font etc) of a particular element.

#### 1. Built in Structural Directives

-----

1. NgFor - Iterates over collection of data. 
We define it in div as *ngFor where star defines that it is structural directive. 
*ngFor="let item of items">
{{item}}


2. NgIf - Uses If to add or remove an element. 
Can be used to display DOM based on some decision. For exapmple toggling a DOM based on button click. This can be considered important when the DOM contains a component which has expensive computations otherwise the hidden property can also be used. 


3. NgSwitch - Displays 1 DOM out of many using switch.   
NgSwitch can be used whenever we have switch case scenario. 


#### 2. Built in Attribute Directives

1. NgStyle - Sets inline styles dynamically based on the state of the component. 
 
Using button changed the style object defined in the typeScript file. Now the same style file was used with one of the DOM using the ngSTyle so the style of that particular file also got updated. 

2. NgClass - Allows you to add or remove CSS classes dynamically. 

The CSS classes can be defined in the particular components CSS file. Whenever we need to change the CSS of a particular DOM we can attach a NgClass to it as we can then dynamically change the class by changing the string defined in the TypeScript which has the name of the current CSS class. 

3. NgModel - Displays a data property and updates it as per the user interaction. 

Can be used to change the DOM properties using the twowaybinding. 
Importanat thing is using NgModel as an input, now as the input gets defined the style can be used for any DOM. 

4. CREATING CUSTOM DIRECTIVES

ng g directive appBold

Directive files are created which are quite similar to the COmponent files. Here we can import ElementRef and HostListener to update the properties of any DOM based on some event. For example mouse hover etc.
