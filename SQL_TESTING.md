# SQL Testing

Our backend is currently WIP and you can see the completed code [here](https://github.com/CSPB3308-Team/productivity-backend/blob/main/app/models.py)
The rest can be found [here](https://github.com/CSPB3308-Team/productivity-backend/tree/main)

# User
The User table stores information about the user.

## UserID
Data Type: integer
Parameters: Primary Key, AutoIncrement

A numeric identifier generated when the user is created.

## first_name
Data Type: varchar(20)
Parameters: Required

User's first name.

## last_name
Data Type: varchar(20)
Parameters: N/A

The user's last name.

## username
Data Type: varchar(20)
Parameters: Required

The user's name that is visible to other users.

## email
Data Type: varchar(100)
Parameters: Required
Unique

The email address used to contact the user.

## password_hash
Data Type: varchar(255)
Parameters: Required

This will safely store the hashed password, via bcrypt


# User Tests

This describes the User table and how our routes interact with it. We have:  
- Signup  
- Login  
- Create  
- Update  
- Delete  

---

## Signup

**Use case name**: Signup Page, `signup()`:  (`/signup`, methods=["POST”])  
**Description**: Test that a User can create an account  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User provides an email, password, firstname and lastname.  
User provides a unique email  
- User has passed all required fields `["username", "first_name", "last_name", "email", "password"]`  
  => If they’re not passed, it will reject with `Missing Field: {field}` with an error 400 for a bad request  
- If User email already exists in the database, return a 409 conflict error  
- If user email is unique, and all required fields passed, status 201 (successfully created) and redirect  

**Test steps**:  
- Navigate to login page  
- Provide valid email  
- Provide valid password  
- Provide a username and name  
- Try to create a user, prompt success or failure  
- Use the status codes to signify pass or fail  

**Expected result**:  
User provides all valid info, user is navigated to dashboard with successful login, get a status 201  

**Actual result (when you are testing this, how can you tell it worked)**:  
User is navigated to dashboard with successful login, get a status 201  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with the database and successfully signed into their account.  
The account session details are logged in the database.  

---

## Update a User

**Use case name**: Update a user (`"/user"`, `update_user()`:,  methods=["PUT", "PATCH"])  
**Description**: Test that a user can be updated, if provided valid authentication (JWT)  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
The user provides a Bearer Token via JWT that can be retrieved and verified using server utils  
The user provides an email for a User account that exists in the database  
The user provides valid information for the associated fields they wish to change  

**Test steps**:  
Navigate to /user, Edit Account form  
Input the details they would like to change about their account:  
- Username  
- Email  
- Password  
- First Name  
- Last Name  
Press ‘Confirm’ button  

**Expected result**:  
User should be able to change the information they wish to change, and be provided with that info  

**Actual result (when you are testing this, how can you tell it worked)**:  
User successfully changes any field in the database, and is shown their new information when the test is successful.  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with database, user’s info is modified as provided, a status 200 is returned  

---

## Login a User

**Use case name**: Log in user (`"/login"`, `login()`:,  methods=["POST"])  
**Description**: Test that a user can log in and get returned a valid JWT in their local storage  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
The user  

**Test steps**:  
Navigate to /user, click Delete Account button  
Press ‘Confirm’ button  

**Expected result**:  
User account is deleted and the user is navigated to the home page (/)  

**Actual result (when you are testing this, how can you tell it worked)**:  
User account is deleted and the user is navigated to the home page (/)  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with database, user’s info matched against the JWT, and then the account is deleted, providing a status 200 (success) is returned  

---

## Delete a User

**Use case name**: Delete a user (`"/user"`, `delete_user()`,  methods=["DELETE"])  
**Description**: Test that a user can be deleted, if provided valid authentication (JWT)  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
The user provides a Bearer Token via JWT that can be retrieved and verified using server utils  
The user exists in the database, and matches the token  

**Test steps**:  
Navigate to /user, click Delete Account button  
Press ‘Confirm’ button  

**Expected result**:  
User account is deleted and the user is navigated to the home page (/). It should also delete the associated Taskagotchi  

**Actual result (when you are testing this, how can you tell it worked)**:  
User account is deleted and the user is navigated to the home page (/)  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: We can currently delete users, however there is no Avatar (Taskagotchi) table yet and so the logic to delete the associated Avatar does not exist.  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with database, user’s info matched against the JWT, and then the account is deleted, providing a status 200 (success) is returned  

# Task
The Task table stores all information relating to tasks

## TaskID
Data Type: integer
Parameters: Primary Key, AutoIncrement

A numeric identifier generated when the user creates a task.

## user_id
Data Type: integer
Parameters: Foreign Key, Required

The ID of the user that created and owns the task.

## task_name
Data Type: integer
Parameters: Foreign Key

The name the user gives the task.

## created_date
Data Type: datetime
Parameters: Required

The creation date and time of the task. This value is populated automatically when the task is created.

## due_date
Data Type: datetime
Parameters: Required

The date that the user declares the task should be completed by.

## task_complete
Data Type: boolean
Parameters: N/A

The date and time the task is completed or expired. The value is initially null, and is automatically updated to the datetime when the task is marked as completed.
If the user does not mark the task as completed by TaskDueDate, the value is set to the due date and TaskIsComplete remains False.

Whether or not the user marked the task as complete. If the user does not complete the task as complete before the due date, this value remains False.

If the due date for a task has passed, the user can spend currency to renew the task up to 24 hours after the task has expired. Renewing a task changes TaskDueDate to 24 hours and marks this field as True. A task cannot be renewed again if this field is True.


## task_renewed
Data Type: boolean
Parameters: N/A

Whether or not the task has been renewed.


## task_type
Data Type: enum => 'short-term', 'long-term', 'daily'
Parameters: N/A


# Tasks Tests

This describes the Tasks table and how our routes interact with it. We have:  
- Get tasks  
- Create tasks  
- Update tasks  
- Delete tasks  


## Get tasks

`/tasks`, method: GET, function: `get_tasks()`  

**Description**: Get a user’s tasks  

**Optional Parameters**:
  - `/tasks` => Returns all tasks, all users
  - `/tasks?user_id=1` => Returns tasks for user_id = 1
  - `/tasks?task_complete=true` => returns completed
  - `/tasks?task_type=short-term` => choose what type return
  - `/tasks?task_complete=true&user_id=1` => we can also add combinations

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
There are tasks in the database associated with the user  
The user is logged in  

**Test steps**:  
Navigate to tasks page (while logged in)  

**Expected result**:  
The user’s tasks are displayed on the tasks page  

**Actual result (when you are testing this, how can you tell it worked)**:  
The user’s tasks are displayed on the tasks page (it’s working)  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
Tasks were not inadvertently modified (this is a read-only operation)  

---

## Create task

Route: `/tasks`, method: POST, function: `create_task()`  

**Description**: A user creates a new task  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User is logged in  
User is on the tasks page  

**Test steps**:  
Navigate to tasks page (already logged in)  
Click add task  
Provide task info: task name, task type (long-term, short-term, or daily), and due date (must after today)  
Click create button  

**Expected result**:  
Task should be created in the database and displayed to the user  

**Actual result (when you are testing this, how can you tell it worked)**:  
Task is successfully created and displayed  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
Task exists in the database  
The user is not blocked from continuing to use the app (create another task, do any other action)  

---

## Update task

Route: `/tasks`, methods: PUT, PATCH, function: `update_task()`  

**Description**: The user needs to make some change to one of their tasks. The most common case would be marking it as completed.  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
The user is logged in  
The user has a task in the database  
The task has been retrieved from the database and is already displayed to the user (via GET)  
The user wants to make some change to the task  

**Test steps**:  
Navigate to the tasks page  
Mark the task as completed (or some other edit)  

**Expected result**:  
The task should be updated in the database  
The updated task should be displayed to the user  

**Actual result (when you are testing this, how can you tell it worked)**:  
Task is updated and displayed correctly  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: Currently, the main update to a task, marking it as completed or unmarking it as completed, is working, but we have not implemented other edits like changing the name or task type.  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
The task in the database has the new information  
The tasks page reflects the new state of the task  

---

## Delete task

Route: `/tasks`, method: DELETE, function: `delete_task()`  

**Description**: User should be able to delete a task completely (not just mark it as completed)  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User is logged in  
User has at least one task in the database  
The user is on the the tasks page  
The task is being displayed to the user (from the GET request)  

**Test steps**:  
Navigate to the tasks page  
Click the delete button next to a task  
Confirm deletion  

**Expected result**:  
The task should be deleted from the database and gone from the screen  

**Actual result (when you are testing this, how can you tell it worked)**:  
The task is deleted from the database and gone from the screen (it works)  

**Status (Pass/Fail, when this test was performed)**:  
Pass  

**Notes**: N/A  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
The task is no longer in the database  
The task is no longer on the screen  


# Avatar
## AvatarID
Data Type: integer
Parameters: Primary Key, AutoIncrement

A numeric identifier for the avatar that is generated when the avatar is created.

## UserID
Data Type: integer
Parameters: Foreign Key, Required

The ID of the user that created and owns the avatar.

## AvatarName
Data Type: varchar(20)
Parameters: Required

The name the user gives the avatar.

## AvatarEnergy
Data Type: int
Parameters: Required

The current avatar energy / stamina. This value depletes over time, and is increased when the user completes tasks.

## AvatarSkinColor
Data Type: int
Parameters: Required

The ID of the customization item used for the avatar's skin color.

This value is pulled from the CustomizationItems table, from the skin category (ItemCategory value of 0)

## AvatarShoes
Data Type: int
Parameters: Required

The ID of the customization item used for the avatar's shoes or feet.
This value is pulled from the CustomizationItems table, from the shoe category (ItemCategory value of 1)

## AvatarShirt
Data Type: int
Parameters: Required

The ID of the customization item used for the avatar's body.

This value is pulled from the CustomizationItems table, from the shoe category (ItemCategory value of 2)




## Avatar Tests

This describes the Avatar table and how our routes interact with it. We have:  
- Get  
- Create  
- Update  
- Delete  

There is a Collections table that serves only as a lookup with GET functions. It only has three columns: id, item_id, item_cost and is utilized in the Avatar tests through relationships; such as pulling values from this table in order to place items on the Avatar. It will be FIXED to pre-seeded items only with no interactions other than lookups. 

---

## Get

**Use case name**: Home Page, `get_avatar()`:  (`/`, method=[“Get”])  
**Description**: Test that when a user hits the homepage, if they have an account, it returns their Taskagotchi (avatar)  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User is logged in with a valid JWT, confirmed by the server  
The User attempting to visit (/) exists in the database  
The user has an Avatar associated with them in the database  

**Test steps**:  
Navigate to home page  
See if User is logged in, if not logged in redirect to /login  
If user is logged in, query database for their Avatar  
Render their avatar with associated settings if exists  
If the avatar does not exist, prompt for creation  

**Expected result**:  
User provides all valid info, logs in, and is presented with their taskagotchi  

**Actual result (when you are testing this, how can you tell it worked)**:  
The Taskagotchi is rendered on the page when the user is logged in and they visit the homepage.  

**Status (Pass/Fail, when this test was performed)**:  
Fail - this table is not built yet  

**Notes**: We have not implemented the User avatars yet, we are still building the models  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with the database and successfully signed into their account.  
The taskagotchi is displayed, as it is available.  

---

## Create

**Use case name**: Signup, `create_avatar()`:  (`/signup`, method=[“Post”])  
**Description**: Test that when a User creates an account, the default avatar associated with their account is created and displays when they visit the homepage. This will be executed after the User is created in the Database, an Avatar will be created and then associated with them  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User provides an email, password, firstname and lastname.  
User provides a unique email  
- User has passed all required fields `["username", "first_name", "last_name", "email", "password"]` => If they’re not passed, it will reject with Missing Field: {field} with an error 400 for a bad request  
- If User email already exists in the database, return a 409 conflict error  
- If user email is unique, and all required fields passed, status 201 (successfully created) and redirect  
- The Avatar’s user_id field has a proper association with Users table  

**Test steps**:  
Navigate to signup page  
Provide valid email  
Provide valid password  
Provide a username and name  
Try to create a user, prompt success or failure  
Try to create and associate an avatar, prompt success or fail  
Use the status codes to signify pass or fail  

**Expected result**:  
User provides all valid info to create an account, get success message, and is presented with their taskagotchi  

**Actual result (when you are testing this, how can you tell it worked)**:  
The Taskagotchi is rendered on the page when the user is logged in and they visit the homepage.  

**Status (Pass/Fail, when this test was performed)**:  
Fail - this table is not built yet  

**Notes**: We have not implemented the User avatars yet, we are still building the models  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with the database and successfully signed into their account.  
The taskagotchi is displayed, as it is available.  

---

## Update

**Use case name**: Signup, `create_avatar()`:  (`/avatar`, method=[“POST”])  
**Description**: Test that when a User attempts to modify their Avatar, such as name, color, etc that they are able to do so if they are logged in, authenticated, and a User and Avatar association exists within the database  

**Pre-conditions (what needs to be true about the system before the test can be applied)**:  
User is authenticated using JWT  
The User is logged in  
The Avatar’s user_id field has a proper association with Users table  

**Test steps**:  
Navigate to avatar page  
Attempt to change one or more fields in the Avatar Form  
Click submit  
The function will check that they are authenticated, the User exists, the association between Avatar and User exists  
After a successful change, the user should see their desired changes reflected in the Taskagotchi avatar  

**Expected result**:  
User provides all valid info to update a Taskagotchi avatar, get success message, and is presented with their taskagotchi with the desired changes  

**Actual result (when you are testing this, how can you tell it worked)**:  
The Taskagotchi is rendered on the page when the user is logged in and they visit the homepage with the desired changes  

**Status (Pass/Fail, when this test was performed)**:  
Fail - this table is not built yet  

**Notes**: We have not implemented the User avatars yet, we are still building the models  

**Post-conditions (what must be true about the system when the test has completed successfully)**:  
User is validated with the database and successfully signed into their account.  
The taskagotchi is displayed, as it is available.  
