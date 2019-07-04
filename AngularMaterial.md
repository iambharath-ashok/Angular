# Angular Material

## What is Angular Material

-	Angular material is reusable high quality UI components 
-	A library of high quality UI components built with Angular and TypeScript
-	Clean and Simple API
-	Well tested
-	Customizable
-	FAST 
-	I18n
-	Great look and feel



## Various Components of Angular Material

-	FormControls:
	-	input 
	-	radio
	-	select
	-	slider
	-	form field
	-	check box
	-	date picker
	
-	Layout

-	Navigation

-	Button and indicators



##	 Angular Boootstrap 

-	Bootstrap is nothing to do with angular
-	We need to create custom directive or components and do some magic in order to use those components
-	We need to use third libraries to develop complex functionalities
-	Bootstrap provides different look and feel 


##	Bootstrap vs Angular material


Angular Material | Bootstrap
----------------|------------
Still new(and immature) | more mature
same quality standards | we have to 3rd party libraries
common api | lot of dependencies
easy to use| 


##	Installing Angular material

-	create the app
-	npm install --save @angular/material @angular/cdk @angular/animations
-	yarn add @angular/material @angular/cdk @angular/animations
-	import material modules into AppModule


###	Step 2: Configure animations

				import {BrowserAnimationsModule} from '@angular/platform-browser/animations';

				@NgModule({
				  ...
				  imports: [BrowserAnimationsModule],
				  ...
				})
				export class PizzaPartyAppModule { }
	

###	Step 3: Import the component modules

			import {MatButtonModule, MatCheckboxModule} from '@angular/material';

				@NgModule({
				  ...
				  imports: [MatButtonModule, MatCheckboxModule],
				  ...
				})
				export class PizzaPartyAppModule { }
		
				
			import {MatButtonModule, MatCheckboxModule} from '@angular/material';


-	Or create a shared modules

			@NgModule({
			  imports: [MatButtonModule, MatCheckboxModule],
			  exports: [MatButtonModule, MatCheckboxModule],
			})
			export class MyOwnCustomMaterialModule { }			

###	 Include a theme

		
			@import "~@angular/material/prebuilt-themes/indigo-pink.css";


###	Gesture Support


-	Some components (mat-slide-toggle, mat-slider, matTooltip) rely on HammerJS for gestures
-	 In order to get the full feature-set of these components, HammerJS must be loaded into the application.
	
			npm install --save hammerjs





##	CheckBox


		<md-checkbox [value]="" [checked]="isChecked" (change)="onChange($event)">Subscribe to news letter </md-checkbox>
		
	


















