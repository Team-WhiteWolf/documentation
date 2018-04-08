# Message Type Overview

## Basic Message Structure
```
{
	"trackingID": "",
	"sender": "",
	"reciever": "",
	"type": "",
	"payload": ""
}
```


## Permission-Service

 | Type | Response | Payload | Description |
 |------|----------|---------|-------------|
 | | | | |


## Icon-Service

 | Type     | Response | Payload       | Description                            |
 |----------|----------|---------------|----------------------------------------|
 | Add_Icon | No       | Icon-Model    | Used to add an icon to the database.   |
 | Get_Icon | Yes      | Data Response | Used to get an icon from the database. |

### Icon Model
```
{
	"name": "File Name",
	"data": "base64 encoded icon/picture file"
}
```

### Data Response
```
{
	"id": "The id of the icon to get",
	"subscriber": [
		{
			"recipient": "module to be notified with the loaded icon",
			"type": "the type of message the recipient expects"
		}
	]
}
```
