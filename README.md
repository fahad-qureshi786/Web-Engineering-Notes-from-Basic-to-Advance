# WELCOME TO WEB DEVELOPMENT 
👤 By Fahad Qureshi
_________________________________________________
## jQuery
### What is jQuery?
		jQuery is a lightweight, "write less, do more", JavaScript library.
		The purpose of jQuery is to make it much easier to use JavaScript on your website.
### Features of jQuery?
		The jQuery library contains the following features:
		HTML/DOM manipulation
		CSS manipulation
		HTML event methods
		Effects and animations
		AJAX
		Utilities
### Syntax of jQuery:
		The jQuery syntax is tailor-made for selecting HTML elements and performing some action on the element(s).
		Basic syntax is: $(selector).action()
		A $ sign to define/access jQuery
		A (selector) to "query (or find)" HTML elements
		A jQuery action() to be performed on the element(s)
		Examples:
			$(this).hide() - hides the current element.
			$("p").hide() - hides all <p> elements.
			$(".test").hide() - hides all elements with class="test".
			$("#test").hide() - hides the element with id="test".
### jQuery Selectors:
		jQuery selectors allow you to select and manipulate HTML element(s).
		jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing CSS Selectors, and in addition, it has some own custom selectors.
		All selectors in jQuery start with the dollar sign and parentheses: $().
		Some HTML Selectors are these:
			$("p")
			$(".className")
		Example:
			$(document).ready(function(){
			  $("button").click(function(){
				$("p").hide();
			  });
			});
		The .class Selector
			The jQuery .class selector finds elements with a specific class.
			$(document).ready(function(){
			  $("button").click(function(){
				$(".test").hide();
			  });
			});
### jQuery Effects
		Hide, Show, Toggle, Slide, Fade, and Animate. WOW!
			$("#hide").click(function(){
			  $("p").hide();
			});

			$("#show").click(function(){
			  $("p").show();
			});
### The following example demonstrates the speed parameter with hide():
			$("button").click(function(){
			  $("p").hide(1000);
			});
			$("button").click(function(){
			  $("p").toggle();
			});
### Fade:
			$("button").click(function(){
			  $("#div1").fadeIn();
			  $("#div2").fadeIn("slow");
			  $("#div3").fadeIn(3000);
			});
### Slide:
			The jQuery slide methods slide elements up and down.
			slideDown()
			slideUp()
			slideToggle()
### Animate:
			With jQuery, you can create custom animations.
			$("button").click(function(){
			  $("div").animate({left: '250px'});
			}); 
			Stop:
				The jQuery stop() method is used to stop animations or effects before it is finished.
				$("#stop").click(function(){
				  $("#panel").stop();
				});
### Callbacks:
		jQuery Callback Functions
		JavaScript statements are executed line by line. However, with effects, the next line of code can be run even though 
		the effect is not finished. This can create errors.
		To prevent this, you can create a callback function.
		A callback function is executed after the current effect is finished.
		Typical syntax: $(selector).hide(speed,callback);
### Chaining:
		jQuery Method Chaining
		Until now we have been writing jQuery statements one at a time (one after the other).
		However, there is a technique called chaining, that allows us to run multiple jQuery commands, one after the other, on the same element(s).
			$(document).ready(function(){
			  $("button").click(function(){
				$("#p1").css("color", "red").slideUp(2000).slideDown(2000);
			  });
			});
### Traversing:
		jQuery traversing, which means "move through", are used to "find" (or select) HTML elements based on their relation 
		to other elements. 
		Start with one selection and move through that selection until you reach the elements you desire.
		UP:
			parent()
				return imidiate parent to the selected element
			parents()
				return all parent till root element html
			parentsUntil(e)
				return parent elements untill e where e is excluded
### Descendents:
			children()
				The children() method returns all direct children of the selected element.
			find()
				The find() method returns descendant elements of the selected element, all the way down to the last descendant.
				$(document).ready(function(){
				  $("div").find("span");
				});
### Siblings:
			siblings() return all siblings to the selected elements
			next()	return next sibling
			nextAll()	return all next siblings
			nextUntil(e)	return all next siblings till e but excluded e	
			prev()	return prev siblings
			prevAll()	return all previous siblings
			prevUntil(e)	return all previous siblings till e but e is excluded
### Events:
			jQuery is tailor-made to respond to events in an HTML page.
			click
			dblclick
				$("p").dblclick(function(){
				  $(this).hide();
				});
			mouseenter
				$("p").click(function(){
				  $(this).hide();
				});
			mouseleave
				$("#p1").mouseleave(function(){
				  alert("Bye! You now leave p1!");
				});
### Bubbling:
		Stop the click event from bubbling to parent elements:
		The event.stopPropagation() method stops the bubbling of an event to parent elements, preventing any parent event handlers from being executed.

		$("span").click(function(event){
		  event.stopPropagation();
		  alert("The span element was clicked.");
		});
		$("p").click(function(event){
		  alert("The p element was clicked.");
		});
		$("div").click(function(){
		  alert("The div element was clicked.");
		});
### preventDefault vs stopPropagation:
		preventDefault prevents the default action the browser makes on that event.
		stopPropagation prevents further propagation of the current event in the capturing and bubbling phases. 

_________________________________________________
## Web Working:
### Request and Response Cycle:
			Web Client (Javascript based application) request to some web server via Rest or Soap services and then it get back the response along with some 
			payload and some status code (Response)
			Request is of two different types:
				Rest:
					Rest is JSON Based communication from server to client
					Rest call is little bit unsecure as compared to SOAP Services
					Rest Calls are very easy to implement and mostly used in the markeet
				SOAP:
					SOAP is XML based http communication from server to client
					Soap services are highly efficient and secure as compared to the rest services
					SOAP Services are bit harder to implement for the developers and less used as some secure banking system use these type of communication 
					from server to server or server to client
### XHR,AJAX & JSON
			These are some standards to communicate from client to server, in client side XHR, ajax or json are methods to send data 
			from client to server
		XHR Example:
			let oReq = new XMLHttpRequest();
			oReq.addEventListener("load", reqListener);
			oReq.open("GET", "https://fakeuserapi/products/findAll");
			oReq.send();
### AJAX:
			$.ajax({
				url: "http://fakeuserapi/products/findAll",
				method: 'POST',
				data: data,
				success: function(res){
					console.log(res)
				},
				error: function(err){
					console.log("error", err.message)
				}
			})
### load:
			load() method allows HTML or text content to be loaded from a server and added into a DOM element. 
			Specify selector with url to specify a portion of the response document to be inserted into DOM element.
_________________________________________________
## ES-6
### Introduction to ES-6
	ECMAScript (ES) is a scripting language specification standardized by ECMAScript International.
	It is used by applications to enable client-side scripting.
### ES6 and Hoisting
		The JavaScript engine, by default, moves declarations to the top. This feature is termed as hoisting. 
		This feature applies to variables and functions. Hoisting allows JavaScript to use a component before it has been declared.
### Features:
		Default Valued Parameters
			We can assign or pass the value to any parameter in the function, so that we can be safe from the error 
			getting from the user if he will not give any arg value then its default value will be set to the variable
### Template Literals
			Template literals are also known as the template string. These allow us to write the embaded, multi line and 
			javascript based string expressions. Template literals are the string literals enclosed by the backtick 
			“(grave accent) and can contain placeholders indicated by dollar sign curly braces.
			let myName = 'John';
			let myRole = 'Software Developer';
			console.log(`My name is ${myName} and I am a ${myRole}.`); // 
			My name is John and I am a Software Developer

### Tagged Literals
			These are the advance version of the template literal strings. Here we pass first arg in function as array, sec 
			and third args will be variables that we have to store in the array, then it will be stored in an array and function will return an array 
### Destructuring assignment
			The destructuring assignment allows reading values from an array or properties from an object, into distinct variables.
			let myName, myRole;
			let array = ['John', 'Software Developer'];
			[myName, myRole] = array; //positional assignment occurs here
			console.log(myName, my Role); //John Software Developer
### Arrow Function Expression:
			New Syntax to write an ordinary function based expressions in javascript
			below function called an arrow function that can be written in only one line with the help 
			of string interpulation and the arrow function features ir ES-6

			const getFullName = (firstName, lastName) => `${firstName} ${lastName}`
				can also be written as below:
			const getFullName = (firstName, lastName) => {
				return `${firstName} ${lastName}`
			}

### let and const:
			let helps to declare a block scope based variable unlike var whose scope it till complete function of js
			let vs. var vs. const

### Spread and Rest Syntaxes (...)
			Rest and spread use three dots notation:
			Spread syntax spread an array into saperate elements
				let addNumbers = (x, y, z) => x+y+z
				const numebrs = [1,2,3]
				log(addNumbers(...numbers))
			Rest syntax condence an array element into a single element
				let addNumbers = (...numbers) => {
				let result =0;
					numbers.forEach(num=> result +=num);
					return result
				}
				console.log(addNumbers(1,2,3));//prints 6

### Classes:
			Classes are a template for creating objects. They like functions can be defined as class declarations and class expressions and can be declared using the keyword class followed by the name of the class (say, Person).
			
			Class Person{
			 constructor(name, age){
				this.name = name;
				this.age = age;
				}
			}
	🔚
=========================   From Akram Notes ================================================
## 	ES6 --- Notes 
		.....
		Outline 
		....
		ES6 Features
		..........
		o Template Literal
		o Arrow Function
		o Classes
		o Modules
		o Enhanced Object Literals
		o Destructuring
		§ Object
		§ Array
		o Default + Rest + Spread
		o Iterators & For…Of
		o Generators
		o Promises
		........
		ES (ECMA Script):
		ECMAScript (ES) is a scripting language specification standardized by ECMAScript International.
		It is used by applications to enable client-side scripting.

		ES6 and Hoisting
		The JavaScript engine, by default, moves declarations to the top. This feature is termed as hoisting. 
		This feature applies to variables and functions. Hoisting allows JavaScript to use a component before it has been declared.

		Arrow ftn :
		let subtract=function (a,b){
			return a-b;
		}
		console.log(subtract(20,10))
		......
		use of arrow fuction sort
		.....
		let arr=[1,2,3,4];// sort arr in descending order
		arr.sort(function (a,b){
					return b-a});
		console.log(arr);
		output:[4, 3, 2, 1]

		let arr2=[4,3,2,1];// sort arr2 in ascending order
		arr2.sort(function (a,b){
					return a-b});
		console.log(arr2);
		output [1, 2, 3, 4]
		...
		ES-6 Classes 
		..
		ES-6 Module
		..
		Default exports
		...
		A module can have one and only one default export. 
		The default export is easier to import. The default for a module can be a variable, a function, or a class.



		// sort.js
		export default function(arr) {
		  // sorting here
		}
		export function heapSort(arr) {
		  // heapsort
		}
		Named export
		.....
		With named exports, one can have multiple named exports per file
		// imports
		// ex. importing a single named export
		import { MyComponent } from "./MyComponent";
		// ex. importing multiple named exports
		import { MyComponent, MyComponent2 } from "./MyComponent";
		// ex. giving a named import a different name by using "as":
		import { MyComponent2 as MyNewComponent } from "./MyComponent";
		// exports from ./MyComponent.js file
		export const MyComponent = () => {}
		export const MyComponent2 = () => {}
		....
		Import all named export into an Object
		...
		import * as MainComponents from "./MyComponent";
		// use MainComponents.MyComponent and MainComponents.MyComponent2
		here
		...
		ES-6 Object Enhance Literal
		...
		Object literal enhancement is used to group variables from the global scope and 
		form them into javascript objects.
		It is the process of restructuring or putting back together
		Example :
		var name = "Duke";
		var color = "Brown";
		var age = 5;
		  
		// Using Object Literal Enhancement
		// Combines all variables into a dog object
		var dog = {name, color, age};
		console.log(dog);
		Output:{name: 'Duke', color: 'Brown', age: 5}

		...
		ES-6 Object destructuring
		...
			When we fetch an object from API, we need to extract element for our work purpose. 
			In older javascript style we extract each element from an object with a line.
			If there is 100 element of an object we to had to write 100 lines for extraction but ES6 is a big relief.
			It helps us to extract multiple elements from an object with a single line.
		....
		Code Example
		...
		const student = {
			firstname: 'Akram',
			lastname: 'Bugti',
			city: 'Sui',
			ielts_scores: {
			  speaking: 8,
			  listening: 7.5,
			  writing: 8.5,
			  reading: 7.0
			}
		};

		//Old Style 
		const firstname = student.firstname;
		const lastname = student.lastname;
		const country = student.city;
		const ielts_scores = student.ielts_scores;
		console.log(`Old method: ${firstname}, ${lastname}, ${city}`) //"Old method: Akram, Bugti, Sui"


		//ES6 Style
		const { firstname, lastname, city, ielts_scores }=student;
		console.log(`New method: ${firstname} ${lastname} ${firstname}`) 

		.....
		Output: New method: Akram Bugti Akram
		....
		.....
		ES-6 Array Destructuring 
		.....
		Destructuring means to break down a complex structure into simpler parts. 
		With the syntax of destructuring, you can extract smaller fragments from objects and arrays. 
		It can be used for assignments and declaration of a variable.
			Array Destructurng:
				When destructuring an array, we use their positions (or index) in an assignment.
			Code Example:
				var colors = ["Violet", "Indigo", "Blue", "Green", "Yellow", "Orange", "Red"];  
		  
		// destructuring assignment  
		var[color1, color2, color3] = colors;  
		  
		console.log(color1); // Violet  
		console.log(color2); // Indigo  
		console.log(color3); // Blue  

		output: Voilet Indigo Blue
		..........
		Getting Random Values:
		..........
		If you want to choose random elements from the given array then in array destructuring you can perform it as follows:

		var colors = ["Violet", "Indigo", "Blue", "Green", "Yellow", "Orange", "Red"];  
		  
		// destructuring assignment  
		var[color1,,color3,,color5] = colors; //Leave space for unpick elements  
		console.log(color1); // Violet  
		console.log(color3); // Blue  
		console.log(color5); // Yellow  

		Output : Violet Blue Yellow
		........
		Array destructuring and Rest operator '(…)'
		......
		var colors = ["Violet", "Indigo", "Blue", "Green", "Yellow", "Orange", "Red"];  
		  
		// destructuring assignment  
		var [a,b,...args] = colors;  
		console.log(a);   
		console.log(b);   
		console.log(args);  

		Output: Violet Indigo [ 'Blue', 'Green', 'Yellow', 'Orange', 'Red' ]

		.......
		Parsing returned array from functions
		.............
		A function can return an array of values.
		It is always possible to return an array from a function,
		but array destructuring makes it more concise to parse the returned array from functions.
		 Code Example 
		 function array() {  
			return [100, 200, 300];  
		}  
		   
		var [x, y, z] = array();  
		   
		console.log(x); // 100  
		console.log(y); // 200  
		console.log(z); // 300  

		Output: 100 200 300
		........
		Rest parameter vs default vs  Spread Operator
		......
		Rest parameter: collects all remaining elements into an array. (condence)
		Spread operator: allows iterables ( arrays / objects / strings) to be expanded into single arguments/elements.
		Default parameter:
		Code Example : function(name = 'no name') {
		}
		If value is undifined 
			function myFunction(x, y) {
				if (y === undefined) {
					y = 2;
				}
			}
			// in function parameter
			function myFunction (x, y = 2) {
		  // function code
		}



		.......
		ES-6 Iterators
		.......
		Introduction to Iterator :
			Iterator is an object which allows us to access a collection of objects one at a time.
		..>Arrays and TypedArrays
		..>Strings — iterate over each character or Unicode code-points.
		..>Maps — iterates over its key-value pairs
		..>Sets — iterates over their elements
		..>arguments — An array-like special variable in functions
		(for in vs for of )
		The for–in loop is for looping over object properties.
		The for–of loop is for looping over data—like the values in an array.)

		Code Example 
		let list = [4, 5, 6];

		for (let i in list) {
		   console.log(i); // "0", "1", "2", return index or keys
		}

		for (let i of list) {
		   console.log(i); // "4", "5", "6" return values 
		}
		.......
		ES-6 Generators 
		.....
		ES6 introduced a new way of working with functions and iterators in the form of Generators (or generator functions).
		A generator is a function that can stop midway and then continue from where it stopped.
		In short, a generator appears to be a function but it behaves like an iterator.
		generator is a user defined function running behaviour or controlled by the user for running a state ment witht next functions

		Code Example:
		function* generate() {
			console.log('invoked 1st time');
			yield 1;
			console.log('invoked 2nd time');
			yield 2;
		}



		.......
		ES-6 Promises
		.........
		Promises used in JavaScript for asynchronous programming. For asynchronous programming, 
		JavaScript used callbacks but there is a problem using the callback which is callback hell or Pyramid of DOM.
		Using the ES6 Promise will simply avoid all the problems associated with the callback.

		Call Back Hell:

		f1(function(x){
			f2(x, function(y){
				f3(y, function(z){ 
					...
				});
			});
		}); 

		A Promise is always in one of the following states:

		fulfilled: Action related to the promise succeeded.
		rejected: Action related to the promise failed.
		pending: Promise is still pending i.e not fulfilled or rejected yet.
		settled: Promise has fulfilled or rejected

		Code Example:

		const myPromise = new Promise((resolve, reject) => {
			if (Math.random() > 0) {
				resolve('Hello, I am positive number!');
			}
			reject(new Error('I failed some times'));
		})
_________________________________________________
## React.JS Notes
### Introduction:
		React Introduction. ReactJS is a declarative, efficient, and flexible JavaScript library for building reusable 
		UI components. It is an open-source, component-based front end library responsible only for the view layer of 
		the application. ReactJS uses virtual DOM based mechanism to fill data in HTML DOM.
### Core Features of React js:
		Virtual DOM. This characteristic of React helps to speed up the app development process and offers flexibility. ...
		JavaScript XML or JSX. ...
		React Native. ...
		One-Way Data Binding. ...
		Declarative UI. ...
		Component Based Architecture. ...
		Short Learning Curve. ...
		Enables Building Rich UI.
### React JS Thinking:
		Step 1: Break The UI Into A Component Hierarchy. ...
		Step 2: Build A Static Version in React. ...
		Step 3: Identify The Minimal (but complete) Representation Of UI State. ...
		Step 4: Identify Where Your State Should Live. ...
		Step 5: Add Inverse Data Flow.
### ReactDOM:
		ReactDOM is a package that provides DOM specific methods that can be used at the top level of a web app to enable an 
		efficient way of managing DOM elements of the web page
### JS vs JSX:
		JS is simply a scripting language, adding functionality into your website. JSX is an addition to the JavaScript syntax 
		which is a mixture of both HTML and JavaScript. Both JS and JSX are interchangeable but JSX makes the code easier to 
		understand for users.
### Conditional Rendering in Javascript Applications:
		Rendering based on the parameters passed into the components is known as conditional rendering. For example in below we
		have to components namely UserGreeting and GuestGreeting passed isLoggedIn parameter
		
		function Greeting(props) {
		  const isLoggedIn = props.isLoggedIn;
		  if (isLoggedIn) {
			return <UserGreeting />;
		  }
		  return <GuestGreeting />;
		}

		const UserGreeting = () => {
			return (
				<>
					<h1> Hello User <h1/>
				</>
			)
		}
		const GuestGreeting = () => {
			return (
				<h1>
					Hello Guest
				</h1>
			)
		}
		
	
		ReactDOM.render(
		  <Greeting isLoggedIn={false} />,
		  document.getElementById('root')
		);
### Webpack:
		Webpack is an open-source JavaScript module bundler. It is made primarily for JavaScript.
		But it can transform front-end assets such as HTML, CSS, and images if the corresponding loaders are included. 
		Webpack takes modules with dependencies and generates static assets representing those modules.
### Props:
		Usage of props
			Props are the only one way to pass the data from one component to another component in javascript
		PropTypes and DefaultProps
			PropTypes are a mechanism to ensure that components use the correct data type and pass the right data, and that components use the right type of props, and that receiving components receive the right type of props.
			If child component will not pass the data of prop then by default DefaultProps will be set with parameters
			import React, { Component } from 'react';
		Example of defaultProps
			class App extends Component {
			render() {
				return (
				<div >
					<Person name="kapil" eyeColor="blue" age="23"></Person>
					<Person name="Sachin" eyeColor="blue" ></Person>
					<Person name="Nikhil" age="23"></Person>
					<Person eyeColor="green" age="23"></Person>
				</div>
				);
			}
			}

			class Person extends Component {
			render() {
				return (
				<div>
					<p> Name: {this.props.name} </p>
					<p>EyeColor: {this.props.eyeColor}</p>
					<p>Age : {this.props.age} </p>
				</div>
				)
			}
			}

			Person.defaultProps = {
			name: "Rahul",
			eyeColor: "deepblue",
			age: "45"
			}

			export default App;
### State:
		State is the plain javascript object used by react to represent an information about the component's current situation.
		Its manage inside the component.
### Passing state from Parent to child component:
		We can pass state from parent to child component via params
		See example at https://www.pluralsight.com/guides/passing-state-of-parent-to-child-component-as-props
### Passing state from Child to parent component:
		https://stackoverflow.com/questions/38394015/how-to-pass-data-from-child-component-to-its-parent-in-reactjs
### Component Architecture
		In react we split components into smaller and more managable components. This helps the maintainability, reuseability
		and saperation of conern When multiple components share the same piece of state we can lift this state into a higher 
		component so that we aren't repeating it.
### Declarative vs Imperative
		Declarative programming is a programming paradigm … that expresses the logic of a computation without describing its 
		control flow. Imperative programming is a programming paradigm that uses statements that change a program's state. 
		Declarative Programming is like asking your friend to fix your car.
### Virtual DOM:
		The virtual DOM (VDOM) is a programming concept where an ideal, or “virtual”, representation of a UI is kept in 
		memory and  synced with the “real” DOM by a library such as ReactDOM. ... Since “virtual DOM” is more of a pattern 
		than a specific technology, people sometimes say it to mean different things.
### Event In React:
		https://www.javatpoint.com/react-events
### Fetching Data From an API in React.js 
		In class component we fetch data as below
			https://www.pluralsight.com/guides/fetching-data-updating-state-react-class
		In functional component we can use React Hooks to fetch data as below	
			
			import {useEffect, useState} from "react";
			import axios from "axios";
			export const UserGreeting = () => {
				const [loading, setLoading] = useState(true)
				const [data, setData] = useState([])
				
				const fetchApi = async () => {
					await axios.get("https://jsonplaceholder.typicode.com/users").then(res => {
						setLoading(false)
						return setData(res.data)
					}).catch(err => {
						setLoading(true)
						return err
					})
				};
				useEffect(async () => {
					await fetchApi();
				}, []);
				return (
					<>
						<h1>Greeting to User</h1>
						<ul>
						{
							data.map(user=> {
								return <li key={user.id}>{user.name}</li>
							})
						}
						</ul>
					</>
				)
			}


### Forms:
		Form components naturally contain some internal states in React 
		Here below we have form in which we will take two attributes values namely name and email and then user will submit this form then we will show the result:
		
		const {Component} = require("react");
		class NameForm extends Component {
			constructor(props) {
			super(props);
			//initialize the state with default values in class component for form
			this.state = {
				value: '',
				email: ''
			};
			//register or bind the methods in the class components
					this.handleChange = this.handleChange.bind(this);
					this.handleSubmit = this.handleSubmit.bind(this);
				}
				//below function is responsible to handle the internal state of the form in react
				handleChange(event) {
					switch (event.target.name) {
						case 'value':
							this.setState({value: event.target.value})
							break
						case 'email':
							this.setState({email: event.target.value})
							break
					}
				}
				//below function is responsible to save the state as default as we have the data in the existing state of the component
				handleSubmit(event) {
					alert(`Name: ${this.state.value} \nEmail ${this.state.email}`);
					event.preventDefault();
				}
				render() {
					return (
						<form onSubmit={this.handleSubmit}>
							<label>
								Name: <input type="text" name={"value"} value={this.state.value} onChange={this.handleChange}/>
								Email: <input type="email" name={"email"} value={this.state.email} onChange={this.handleChange}/>
							</label>
							<input type="submit" value="Submit"/>
						</form>
					);
				}
			}
		export default NameForm


### Component Life Cycle Methods:
		There are 3 basic major component life cycle methods in react.js
			1. componentDidMount() {}         //when any component will be render/register/ or rerender then this method will be called
			2. componentDidUpdate(prevProps, prevState, snapshot) {}  //when component is changing the state on some action then this method will be called
			3. componentWillUnmount() {} 		//when component will be finishing the state this method will be called
			for detailed explanation visit here https://www.w3schools.com/react/react_lifecycle.asp


### Hooks Introduction
			Hooks are new edition in React 16.8. Hooks are alternative way to communicate with the data as we communicate in class component with the help of component life cycle
			methods. Hooks provide the extra and out of the box functionality and hide the complexity. Hooks can only be used within the functional Components. There are various 
			type of Hooks are available to use in React Js as default for example:
				useState(state)
					allows us to access and update the certain values in the component over time.
						//const [variable, functionNameToChangeState] = useState(initialState)
					e.g const [products, setProducts] = useState([])
				useEffect(callbackMethod)
					useEffect let us perform the side effects in the functional components. Side effect is like when are are trying to react with the outside world like data fetching
					for an API of updating data on some actions. It takes the callback function inside the function like:
					useEffect(callBackFunction, dependencyArray)
						useEffect (() => {
							return (
								
							)
						}, [])
				useRef()
					useRef Hooks allows us to hold the reference of some variable or value
					const value = useRef('')
				useContext() //ham ny nahi parha 
				useReducer()//ham ny nahi parha
					useReducer is a useFull hook to implement a certralize state for all the components in the react instead of passing data with the help of props from 
					parent to child components with hierarchy. In react we create a ceteral store at one place and create some reducer that are responsible to update 
					the states, component that wanted to update something, will request to relative reducer and reducer will update and send the updated notification to
					all the component by dispatching an action that would update the state of all the components in the react
### React Router:
		To show or hide the data from the components to the UI based on some fixed or dynamic URL pattern we use react router.
		Steps to use React Routers:
			yarn add react-router-dom
			wrap all the components used within the App.js with <BrowserRouter>...Components...</BrowserRouter
			<BrowserRouter>
			  <Routes>
				<Route path="/" element={<Layout />}>
				  <Route index element={<Home />} />
				  <Route path="blogs" element={<Blogs />} />
				  <Route path="contact" element={<Contact />} />
				  <Route path="*" element={<NoPage />} /> //router is no any path is available will called this router
				</Route>
			  </Routes>
			</BrowserRouter>
### Single Page application:
		Application that don't refresh the complete dom but it only update some perticular section of the page with the help of reuseable componnets is said
		to be a single page application.
		There are various javascript libraries available in the markeet to achieve the single page application ceoncept like React.Js and Angular CLI or Angular.Js or Vue.js
_________________________________________________

## Introduction to Node.js
	Node.js is open source, asyncronous, single threaded javascript environment for building the backend Application Programming Interfaces to build an application.
	It uses V8 engine to fulfill the application need. Its single processor without creating the new thread for every new request.
	Sample code for Node.Js application.
	create following files:
	package.json containing following code:
		{
		  "name": "test-node-app",
		  "version": "1.0.0",
		  "description": "",
		  "main": "index.js",
		  "scripts": {
			"test": "echo \"Error: no test specified\" && exit 1"
		  },
		  "keywords": [],
		  "author": "",
		  "license": "ISC",
		  "dependencies": {
			"nodemon": "^2.0.15"
		  }
		}
### Create index.js and paste the following sample code
	
			const http = require('http')
			const hostname = '127.0.0.1' //or localhost
			const port = 3000	//on which apis will be accessible like 'http://127.0.0.1:3000/api/...
			const server = http.createServer((req, res) => {
			  res.statusCode = 200
			  res.setHeader('Content-Type', 'text/plain')
			  res.end('Hello World\n')
			})
			server.listen(port, hostname, () => {
			  console.log(`Server running at http://${hostname}:${port}/`)
			})
		run node server:
			node index.js
		install nodemon library for continous refresh and running application on update:
			npm install nodemon
		now run following command
			nodemon index.js
### Advantages of Node.js	
		Read the checklist of Node.js greatest features below before you put off on your successful journey with Node.
			Efficient performance.
			Easier development process.
			Reusable code.
			Ability to handle multiple requests.
			Ability to scale smoothly.
			Prompt code execution.
			Asynchronous and event-driven.
			Supported by leading companies.
### Traditional Web Server Model Working:
		Traditional hosting comes mainly in two forms, dedicated and shared. With shared hosting, which is more common among small and medium sized businesses, 
		the client pays for a set amount of space (storage) on a single server, and that server's resources are shared by a number of other websites.
### Node.js Modules:
		In node.js modules are helpful to import or export components or function from one file to another file
		Functions:
		
			function add(x, y) {
			   return x + y;
			}
			  
			function subtract(x, y) {
			   return x - y;
			}
			  
			// Adding the code below to allow importing
			// the functions in other files
			module.exports = { add }
### Buffer Module:
			The buffers module provides a way of handling streams of binary data. The Buffer object is a global object in Node. js, and it is not necessary 
			to import it using the require keyword.
			Sample Code:
				Resource: 	https://www.w3schools.com/nodejs/ref_buffer.asp#:~:text=The%20buffers%20module%20provides%20a,it%20using%20the%20require%20keyword.
				var buf = Buffer.alloc(15);
		Node.js Module and its types:
			Follow this resource:  https://www.tutorialsteacher.com/nodejs/nodejs-modules
		Node Package Manager:
			Node Package Manager (NPM) is a command line tool that installs, updates or uninstalls Node. js packages in your application. 
			It is also an online repository for open-source Node. js packages.
### Web Servers
		Web Servers are the used to host the applications that helps to communicate from business logic layer to different clients like web apps and mobile apps.
		There are various types of web servers available in the markeet like Apache Tomcat Web Server (JVM based applications), Nginx(Microsoft web server)
### Node js Events:
		Follow this resource: https://www.w3schools.com/nodejs/nodejs_events.asp
### Express.JS
		Express.js is fast, unopinioned web framework for building the node js applications by hiding the major complexity.
### Example CRUD Application, Database Connectivity and much more with the help of node js:
		Go to https://github.com/fahad-qureshi786/Node-JS---Learning-Work/tree/full-backend
		and Enjoy the ride.

## Server Side application development with Node Js
	https://expressjs.com/

## CRUD Rest APIs Development with Node js and MySQL PhpMyAdmin database server
	https://blog.logrocket.com/build-rest-api-node-express-mysql/
	In given tutorial you will have to change only one file named config.js, write below code there
		
		const config = {
		  db: {
			/* don't expose password or any sensitive info, done only for demo */
			host: "localhost",
			user: "root", //username of your database
			password: "", //password if you have
			database: "dbName",
		  },
		  listPerPage: 10,
		};
		module.exports = config;
## Follow link to check your skill assessment:
[Follow this Link](https://www.javatpoint.com/reactjs-mcq#:~:text=12)
_____________________________________________
🙏🏼🙏🏼🙏🏼🙏🏼 😊😊
### THANK YOU FOR VISITING PLEASE FOLLOW us ON GitHub https://github.com/fahad-qureshi786/
			
			
			
			
			
			
			
			
			
			
