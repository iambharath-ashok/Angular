#	Typescript

-	Superscript of javascript
-	Typescript has feature that current javascript doesn't have them

## Features of TS

-	Strong Typing
-	Object Oriented Features
-	Compile Time errors
	-	Transpile TS to Js
-	Great Code Editors


##	Installing TS

-	npm install -g typescript

-	Create new ts file

		main.ts
	
-	Compile ts file
	
		tsc main.ts
		
-	run js file

	node main.js 
	
	


## Declaring variables


-	two ways

	- 	let number = 10
	-	var number = 10

-	From ES2016, js also has let keyword support 


##	Types

-	string
-	number
- 	map
-	dictionary
-	boolean
- 	any
-	array
	-	number[]
	-	string[]
	-	any[]
	
	
## Const
		const colorRed = 0;
		const colorGreen = 1;
		const colorBlue = 2;


## Enum
		
		
		enum Color { RED=0, GREEN=1, BLUE=3 };
		let backgroundColor = Color.RED;
	
## Type Assertions 

-	Type Assertions is a way to tell the compiler about the type of variable so that we can access the IntelliSense
-	TS supports Type Assertions in 2 ways


		let name;
		name = 'bharath';
		let containsString = (<string>name).endsWith('th');
		let alternative = (name as string).endsWith('th');
		
		
## Arrow Fucntions

-	Like declarative programing
-	lambda expressions 


		let fun1 = function (message) {
			console.log(message);
		}
		
		
		let fun2 = (message) => console.log(message);
		
		

## Interface

- 	Interface contains the methods declaration that implementor of interface will provide implementation
-	Interface can also be used to define the Object Structure with fields
-	EX:

			export interface ICar {
			
				name: string,
				model: string,
				capacity: number
			}
			
			
			let benz: ICar = {
			
				name: 'Benz extreem',
				model: '2022',
				capacity: 2
			
			}


## Class 

-	Class is a encapsulation of properties and functions that highly related 


## Objects

-	Objects are concrete implementation of class or interface


## Constructors

-	Constructor is a special method that is called at object creation time


		
		
			export class  Car {
			
			
				constructor (public name: string, public model: string, public capacity: number) {
					// no need of assignment in TS
				}
			
			}

## Constructor with optional parameters


		class Point {
		
			constructor(x?: number, y?: number) {
			
			}
		
		}


## Access Modifiers

-	public
-	private
-	protected




##  export or Module

-	export should be used before class, directives, interfaces, const to use outside the scope of that module
-	export is used to add visibility outside its defined module 


	































































