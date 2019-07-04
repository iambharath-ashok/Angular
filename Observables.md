## Observables

-	do(), map(), catch(),subscribe() methods are operators on the Observable class used for asynchronous operation
-	map() operator is used to transform object of one type to another 

	-	subscribe:
	
			subscribe(
				(response : Response) => {
				
				},
				(error: Response) => {
				
				
			});
		
	-	catch:
		
			catch((error:Response) => {
		
		
			})
			
	-	map:
		
			map((response: Response) => {
				
			
			});
		
	-	Promise:
	
			new Promise((resolve, reject) => {
				setTimeout(() => {
								
					if(control.value === 'bharath'){
						resolve({isUnique: true});
					}
					else {
						resolve(null);
					}
				
				
				},3000);
				
			});


##	Observables vs Promises


-	With Observable nothing happens until we subscribe to that ie API call is not going to happen 
-	Observables are lazy and promises are eager
-	We can convert and Observable to promise but not recommended using toPromise() operator on Observable instance

		
		this._http.get()
		.map((response:Response) => this.data = response.json())
		.toPromise()
		.catch();

-	promises dont have subscribe() method
-	promises have only two methods 

	-	then(): for handling success response
	- 	catch(): for handling error response
-	promises are eager, we dont need to call then() method to make an API call
-	Observablesa are lazy nothing happens until we subscribe to them


##	Why Observables are lazy

-	Observables are lazy because of its operators 
-	Observable operators are very powerful to perform specific operations
-	Observable operators allows to implement certain features with only one of code 
-	retry(3) 

	-	if call to API fails observable retry(3) method is going to make API 3 times 
	-	traditionally retry() requires lot of code but with observable retry method its just a one line of code
	-	This is called Reactive Programming
		-	performing complex operations with one line of code
		-	rxjs is library for using Reactive Programming allowing us to write code in reactive style
		-	Reactive Programming allows some feature that is far more complex to implement the traditional way
		
		
-	Since observable is going to work only when we subscribe to it, we can chain multiple operators together like map(), catch(), do(), retry(3) etc


#	RxJs


-	RxJs is a third party library that angular uses heavily for asynchronous operations
-	RxJs is Reactive Programming library which is all about observables