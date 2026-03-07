- JSON Models for [Quizer]([[API Docs/Quizer]])
- # Quiz JSON
  id:: 69abf1e8-a7e1-421d-99a4-c102596c1d03
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