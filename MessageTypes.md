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

 | Type 		   | Response | Payload 		| Description 					     |
 |-------------------------|----------|-------------------------|----------------------------------------------------|
 | Add_User_Permission 	   | No       | UserPermission-Model    | Used to assign Payloads to an user		     |
 | Get_User_Permission 	   | Yes      | User-Model 		| Used to get all the permissions of a specific user |
 | Remove_User_Permission  | No       | UserPermission-Model    | Used to remove a permission from an nser 	     |
 | Add_Group_Permission    | No       | GroupPermission-Model   | Used to assign Payloads to a group 		     |
 | Get_Group_Permission    | Yes      | Group-Model 		| Used to get all the permissions of a specific group|
 | Remove_Group_Permission | No       | GroupPermission-Model   | Used to remove a permission from an group 	     |
 | Add_Permission 	   | No       | Permission-Model 	| Used to create new permissions 		     |

### UserPermission-Model
{
	"userId" : "The id of the user",
	"permissionId" : "The id of the permission"
}

### User-Model
{
	"userId" : "The id of the user"
}

### GroupPermission-Model
{
	"groupId" : "The id of the group",
	"permissionId" : "The id of the permission"
}

### Group-Model
{
	"groupId" : "The id of the group"
}

### Permission-Model
{
	"permissionText" : "Text what the permission does"
}


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
	"recipient": "module to be notified with the loaded icon",
	"type": "the type of message the recipient expects"
}
```
