icon:: ✅
type:: API
tags:: API, Open-Source
status:: Concept

- # Info
  collapsed:: true
	- This is an API for new app / ecosystem called Quizer.
	- **Apps + Source**
		- [Quizer Editor](https://apps.projnull.eu/quizer/) - NO SOURCE YET
- # Types
  collapsed:: true
	- `:code`: `AAAA-AAAA` - Small Invite code
	- `:id`: `<Numeric ID>` - Incremental ID usualy used inside the JSON
	- `:uuid`: `<UUID>` - Used for user IDs
	-
- # JSON Models
  collapsed:: true
	- Quiz JSON
	  id:: 69abf1e8-a7e1-421d-99a4-c102596c1d03
	  heading:: true
		- ```json
		  {  
		  	"name": "Quiz Name",  
		  	"elements": [  
		  		{  
		  			"id":":id",  
		  			"required":true, // can be true/false (undefined == false)  
		  			"question": "My Question",  
		  			"type":"single",  
		  			"correct": ":id",  
		  			"answers": [  
		  				{id:":id",text:"My Answer"}  
		  			]  
		  		},  
		  		{  
		  			"id":":id",  
		  			"type":"html",  
		  			// `correct` does not need to be set  
		  			"data": "HTML **CODE**"  
		  		},  
		  		{
		  			"id":":id",  
		  			"question": "My Question",  
		  			"type":"open",  
		  			"correct": "Correct Answer"  
		  		}  
		  	]  
		  }
		  ```
- # Endpoints
	- ## Auth API `/auth/`
		- ### POST `/login`
			- Login DUH
		- ### POST `/register`
			- Register (defaults to `student`)
			- Teacher accounts need to be made manualy (db edit idk)
		- ### GET `/profile`
			- Returns user profile.  
			  With account type (`student`,`teacher`)  
			  
			  ```json  
			  {  
			  "name":"My Name"  
			  "type":"teacher"  
			  }  
			  ```
	- ## Student API `/student/`
		- ### GET `/quiz/:code`
			- Returns the [Quiz JSON](((69abf1e8-a7e1-421d-99a4-c102596c1d03))) without answers. (AKA `correct` is removed from each)
		- ### POST `/quiz/:code`
			- Send the answers
	- ## Teacher API `/teacher/`