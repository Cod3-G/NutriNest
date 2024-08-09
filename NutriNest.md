Healthy Food Website - "NutriNest"
Overveiw: This site is built in angular and firebase.
Version of Angular Used : 16

Angular: Angular is a popular open-source web application framework maintained by Google. It is used for building single-page applications (SPAs) and dynamic web applications. Here are some key aspects of Angular:

1. Architecture
Component-Based: Angular applications are built using a component-based architecture. Components are the basic building blocks of an Angular application, encapsulating HTML, CSS, and TypeScript code.
Modules: Angular applications are divided into modules, which are containers for a cohesive block of code dedicated to an application domain, a workflow, or a set of related capabilities.
2. Development Language
TypeScript: Angular is primarily written in TypeScript, a superset of JavaScript that adds static types. TypeScript helps catch errors at compile time, making the development process more robust and maintainable.
3. Key Features
Two-Way Data Binding: Angular provides a mechanism for synchronizing the model and the view, making it easier to manage the flow of data within the application.
Dependency Injection: Angular has a built-in dependency injection framework that helps manage and inject dependencies in a clean and efficient way.
Directives: Directives are special markers in the DOM that extend the functionality of HTML elements. Angular provides built-in directives like ngIf, ngFor, and custom directives.
Services: Services are used to share data and functionality across components. They are typically used for business logic and data management.

Component Structure:
.html file contains html code
.css file contains the css part or styling  code
.ts file contain typeScript related code or logic code
spec.ts usually not used

Structure Of Healthy Food Website
Modules of this project:
There are 4  modules used in this site
1.	Defualt module app module: needs to run the application, contains all the imports
2.	Admin Module contains admin related components, routing and other data
3.	Client Module contains Client related component, routing and data
4.	Shared Module: this module contains component and others that can be used both for Admin, Employee  ,Client and Authentication Realted data.
Defualt Module: it contains defualt routing and one defualt component,
Admin Module: it contains five components,	
such as 
	DashboardComponent: it contains all the code and data related to the data that is displayed on the Admin dashboard, it contains all the order management data.
	MainComponent: it contains all the code and data related to the data that is displayed on the on the Product Management page, admin can view all the products, add new product , edit and delete products
	ProductComponent: it contains all the code that are used for the update and add new product, this componenet opens in the modal.
UserComponent: This component contains code and login related to the user management where admin can manage the his employees either Activate the employee Account and Deactivate or Delete the employee account.

Client Module: it contains five components,	
such as 
	MainComponent: it contains all the code and data related to the data that is displayed on the Client dashboard
	MenuComponent: it contains all the code and data related to the data that is displayed on the Menu, user can item to the cart.

	TrackComponent: it contains all the code for the tracking the order, user view al the order history.

CartComponent: This component contains logic related to cart item it contains all the info that is required for the cart item, user can remove item from the cart, increase the quantity of the item and proceed to the checkout.

AboutComponent: it contains the info related to the site.

Shared Module: it contains eight  components,	
such as 
	NavbarComponent: it contains all the code and data related to the data that is displayed on the Header of the site, this used for Client, Employee and Admin
	FooterComponent: it contains all the code and data related to the data that is displayed on the Footer of the site, this used for Client, Employee and Admin

	ProfileComponent: it contains all the code and data related to the data that is displayed on the  Profile Page, this used for for Client, Employee.

LoginComponent: This component contains logic for the Login system this is used for Client, Employee and Admin

RegisterComponent: it contains all the code and data related to the data that is displayed on the Register Page 
PaymentComponent: it contains all the code and logic related to the payment, it contains stripe logic
EmployeeComponent: it contains all the code and logic related for employee or delivery boy where order can be managed.

Backend Code:

node-server: contains the backend related work
server.js: this is the main file it contains all the logic for the stripe payment.
Services: It contains all the login or the code  that is used to fetch or post data to the Firebase(Database)
Guard : Guard are used to resctrict the user on the routes,
There are 2 guards used
Auth Guard: This is Guard checks if the user is logged in or not, if logged in then it continues the user to navigate otherwise it redircts to the Login page.
Employe Guard: This is Guard checks if the Logged in user is the employee or not
