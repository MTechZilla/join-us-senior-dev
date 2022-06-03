# Join Us

This assignment is designed for the job post of Senior Software Developer. ( Dot Net )

## Assignment Info

Create a chat api that will have public rooms.

### Database structure

1. User
```
id: ( guid, unqiue )
firstName: ( string, required )
lastName: ( string, required )
email: ( string, required, unique )
phoneNumber: ( number, required )
profilePic: ( string, required )
password: ( string, required )
roomsOwned: Room[]
roomsJoined: Room[]
createdAt: ( date, auto-added )
updatedAt: ( date, auto-added and updated )
```

2. Room
```
id: ( guid, unqiue )
name: ( string, required )
description: ( string, required )
ownerId: User
users: User[]
createdAt: ( date, auto-added )
updatedAt: ( date, auto-added and updated )
```

  **Note:** This is a reference structure. You can improvise it as per your requirement.

### APIs

1. Signup
```
  Request:
    URL: /sign-up
    Method: POST
    Body: {
     firstName: ( string, required ),
     lastName: ( string, required ),
     email: ( string, required, unique ),
     phoneNumber: ( number, required ),
     profilePic: ( url, required ),
     password: ( required, must have 8 characters with alpahnumeric and special characters )
    }
  Response:
    statusCode: 201,
    data: {
     accessToken: string,
     refreshToken: string
    }
```
  **Note:** Send a `confirmationToken` via mail to the end user.

2. Confirmation
```
  Request:
    URL: /confirm
    Method: PUT
    Body: {
      token: ( string, required )
    }
  Response:
    statusCode: 200,
    data: {
     message: "Account confirm success"
    }
```

3. SignIn
```
  Request:
    URL: /sign-in
    Method: POST
    Body: {
      email: ( string, required ),
      password: ( string, required ),
    }
  Response:
    statusCode: 200,
    data: {
     accessToken: string,
     refreshToken: string
    }
```

4. Logout
```
  Request:
    URL: /logout
    Method: PUT
  Response:
    statusCode: 200,
    data: {
     accessToken: string,
     refreshToken: string
    }
```

5. Get all rooms
```
  Request:
    URL: /rooms
    Method: GET
  Response:
    statusCode: 200,
    data: {
      rooms: []
    }
```

6. Get single room
```
  Request:
    URL: /rooms/:id
    Method: GET
  Response:
    statusCode: 200,
    data: {
      id: string,
      name: string,
      description: string,
      users: Array of users ( Use relationship )
    }
```

7. Create single room
```
  Request:
    URL: /rooms
    Method: POST
    Body: {
      name: ( string, required ),
      description: ( string, required ),
      ownerId: ( string, required )
    }
  Response:
    statusCode: 200,
    message: "Room created success"
```

8. Join single room
```
  Request:
    URL: /rooms/:id
    Method: PUT
    Body: {
      userId: ( string, required )
    }
  Response:
    statusCode: 200,
    message: "User joined successfully"
```

9. Post message in room ( Use websocket connection )
10. Get messages in room ( Use websocket connection )


### Stack:
Develop the application, use the below-given stack:

* Language & Framework: C# & Dot Net Core.
* Database: Any SQL Database.

### Bonus Points:
1. Implementing API Rate limiting.
2. Implementing Domain white listing.
3. Implementing api caching using redis.
4. Having properly protected and non-protected as per functionality described in above api structure.
5. Have application hosted over aws/azure/gcp.

### Important Notes:

1. Application should be built using the above stack.
2. For registration, use JWT or a session-based mechanism
3. Proper error handling is required.
4. Write neat, suitable, bug-free, and readable code as per the coding standards.
5. Create a data model as given in the data structure section.
6. Data model should be normalized and the query must be an acid complaint.
7. Use Websocket to create a connection where you think is required.
8. Have a swagger ui to document this api.

**Note:** The timeline to complete this app is a maximum of three days.
