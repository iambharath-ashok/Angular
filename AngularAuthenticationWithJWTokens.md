#	JSON Web token

-	User authenticate with username and password in server /api/authenticate
-	Server is going to validate these credentials and if they are valid we are going to return json web token
-	JSON Web token is basically a json object that includes certain attributes about login user
-	And we use this Json object to identify on client and also on the server 

	-	Json object contains details like :
	
		-	userId
		-	role
		-	name
		-	email

-	We need to store the JWT token in browser so that we can use that across session restarts
-	If user closes the browser and opens it again it should be there 
-	All modern web browser provides some mechanism  to store Json web token in local storage

	-	On client we identify the user and based on that
		
		-	we can display current user name
		-	show/hide part of a page
		-	prevent access from certain routes
		
		
-	When user wants to access certain secured api's like /api/orders
-	Then client should include the JWT token with request 
-	Server will extract the token and validates it and returns response
-	If token is invalid then unauthorized response will be sent back to client



##	JWT Token implementation at Client side

-	User will authenticate with his username and password
-	We will make a api call to /api/authenticate resource with post request
-	Server will validate the credentials and return JWT token if its valid otherwise it will return null as response
-	At client side we can subscribe to response and use the map operator to validate the token 

	-	If token is valid, we will store it on the localStorage  and true
	-	JavaScript has a localStorage instance available, we can use that for storing the token
	-	else return false showing invalid credentials
	
		
		
			login (credentials) {
			
				this._http.post('/api/authenticate', JSON.strify(credentials))
				.map((response:Response) => {
					let result = response.json();
					if(result && result.token) {
						localStorage.setItem('token', result.token);
						return true;
					} else {
						return false;
					}
				});
			
			
			}
			
			
			logout () {
				
				localStorage.removeItem('token');
			}

## Showing and Hiding elements

-	Install angular2-jwt package

			npm i -g --save angular2-jwt
	
	
			isLoggenIn(): boolean {
			
				let jwtHelper = new jwtHelper();
				let token = localStorage.getItem('token');
				let isTokenExpired = jwtHelper.getTokenExpirationDate(token);
				let isExpired = jwtHelper.isExpired(token);
				
				return !isExpired;
			}



































