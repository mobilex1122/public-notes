icon:: ✅
tags:: API, Open-Source
status:: [[In Development]]

- **Sub pages:**
	- [JSON Models]([[API Docs/Quizer/JSON Models]])
- **INFO**
  collapsed:: true
	- This is an API for new app / ecosystem called Quizer.
	- **Apps + Source**
		- [Quizer Editor](https://apps.projnull.eu/quizer/) - NO SOURCE YET
- **Types**
  collapsed:: true
	- `:code`: `AAAA-AAAA` - Small Invite code
	- `:id`: `<Numeric ID>` - Incremental ID usualy used inside the JSON
	- `:uuid`: `<UUID>` - Used for user IDs
	-
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