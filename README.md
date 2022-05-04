# Join Us

This assignment is designed for the job post of the **Senior Software Developer**. ( Dot Net )

## Assignment Info

Create a chat app that will have public rooms.

Step 1: Create a sign up api and page ( `/signup` ) ( Signup user with following details )

* First Name ( Required )
* Last Name ( Required )
* Email ( Required ) ( Unique ) ( Use AWS Cognito to register the user )
* Phone number ( Required )
* Profile pic ( Required ) ( Store this on AWS S3 bucket )
* Password ( Required ) ( Must have 8 characters with alpahnumeric and special characters )

After successfully signup redirect user to homepage ( `/signin` )

Step 2: Confirmation api and page ( `/confirmation?email=abc@mail.com` ) 

Step 3: Create a sign in api and page ( `/signin` )

* On sign in api and page user should be able to login with email and password.
* Show error if email and password doesnt match.
* Show error for invalid email address.
* If email is not confirmed, don't allow to signin.
* Redirect user to homepage ( `/` ) after successfully login.
* Show a forgot password link in login form where user can reset his password.

Step 4: Show available chat rooms on home page and create api for that ( `/` ).
Also show a button to create a public room.

Step 5: Create public chat room api and page ( `/create-room` ) ( With Following details )
* Name
* Description

Step 6: Join that room by click on room from home page ( `/room/{room_id}` ) 

Step 7: Send messages and all other people from that room will recieve the message ( `/room/{room_id}` )

### Bonus Points:

-	Use Google / Facebook / Apple / Github OAuth to register and login user in the application.
-	Implementing the API Rate limiting.
-	Leave a room would be a great feature to build.
-	Pagination on API side would be a great feature to build.
-	Filtering based on Filled and Non Filled rooms would be a great feature to build.

### Stack:
To develop the application, use the below-given stack:

FrontEnd: 
* HTML, CSS, JavaScript
* React, Vue and Angular are optional.

Backend:
* Language & Framework: C# & Dot Net.
* Database: Postgres
* CloudService: AWS

### Important Notes:

1. UI can be responsive but not a super important part.
2. Application should be build using the above stack.
3. For registration, use JWT or a session-based mechanism
4. Proper error handling is required.
5. Write neat, suitable, bug-free, and readable code as per the coding standards.
6. Create a data model as you need
7. Data model should be normalized and query must be acid complaint.
8. Use Websocket to create connection between users.

**Note: The goal of the task is majorly based on backend development and thus UI won't be an important factor while evaluation.**

**The timeline to complete this app is a maximum of three days. Plagiarism is
prohibited and if an applicant submits a plagiarised work then his application
will be rejected.**
