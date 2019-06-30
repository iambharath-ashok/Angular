#	Typescript

-	Create Class, interface, enum
-	Interface can have method declaration and class implementing interface will provide implementation


## ng Bootstrap

-	ng Bootstrap provides components and directives based on css and bootstrap markup
-	ngb-alret, ngbButton , ngbButtonLabel, ngb-datepicker, ngbDropdown 


## How to add Bootstrap 4 to angular

-	install via npm 

		npm install --save @ng-bootstrap/ng-bootstrap

-	Once installed we need to import our main module:
	
	
			@NgModule({
			  ...
			  imports: [NgbPaginationModule, NgbAlertModule, .., NgbModule, ...],
			  ...
			})
			export class AppModule {
			}
			
			
- 	add in .angular-cli.json
	
		"styles": [
		  "node_modules/bootstrap/dist/css/bootstrap.min.css"
		]
			
			
			
			
