# Types
	- `:code`: `AAAA-AAAA`
	- `:id`: `<Incremental ID>`
	- `:uuid`: `<UUID>`
- # Endpoints
	- ## Auth API `/auth/`
		- ### POST `/login`
			- User Login
		- ### POST `/register`
			- Register (defaults to `student`)
			- Teacher accounts need to be made manualy (db edit idk)
		- ### GET `/profile`
		- Returns user profile.
		- With account type (`student`,`teacher`)
		- ```json
		  {  
		  "name":"My Name"  
		  "type":"teacher"  
		  }
		  ```
	- ## Student API `/student/`
		- ### GET `/quiz/:code`
			- Returns the QUIZ Json without answers. (AKA `correct` is removed from each)
		- ### POST `/quiz/:code`
			- Send the answsers
	- ## Teacher API `/teacher/`