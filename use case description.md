
# Use Case Descriptions

## Login
### User:
**Trigger:** The user navigates to the application's homepage
**Precondition:** If the user has an account, they can log in
**Postcondition:** The user is logged in and can use the application
**Flow of Events:**
- The user enters their username and password
- The user presses the "Log in" button
- The application verifies the username and password
**Exceptional Behavior:**
- If either field is empty, a message will appear: "Enter username!" or "Enter password!"
- If the username or password is incorrect, an error message will appear: "Incorrect username or password!"
### Administrator:
**Trigger:** The administrator navigates to the application's homepage
**Precondition:** The administrator has created an account and assigned themselves the admin role
**Postcondition:** The administrator is logged in and can manage the polls
**Flow of Events:**
- The administrator enters their username and password
- The administrator presses the "Log in" button and can manage polls
**Exceptional Behavior:**
- If either field is empty, a message will appear: "Enter username!" or "Enter password!"
- If the username or password is incorrect, an error message will appear: "Incorrect username or password!"

## View Polls
### User:
**Trigger:** The user navigates to the application's homepage
**Precondition:** The user does not need to be logged in to view polls
**Postcondition:** The user can view ongoing polls
**Flow of Events:**
- The user sees the ongoing polls
**Exceptional Behavior:**
- If there are no ongoing polls, a message will appear: "No ongoing polls!"

## Vote
### User:
**Trigger:** The user selects a poll and presses the "Vote" button
**Precondition:** The user is logged in and has selected a poll
**Postcondition:** The user's vote is recorded, and the results are updated
**Flow of Events:**
- The user selects a poll
- The user selects their preferred option
- The application updates the poll results in the database
**Exceptional Behavior:**
- If the user is not logged in, instead of the "Vote" button, the text "Log in to vote" will be displayed
- If the user tries to vote multiple times on the same poll, the application prevents it and shows a message

## Create New Polls
### Administrator:
**Trigger:** The administrator logs in and navigates to create a poll
**Precondition:** The administrator enters the poll's title
**Postcondition:** The administrator adds the necessary options and adds them to the poll
**Flow of Events:**
- The administrator adds the title
- The administrator adds the poll options
- Once all required fields are added, the administrator presses the "Add Poll" button
**Exceptional Behavior:**
- If the title or option field is empty, the application displays a message: "Field is empty!"

## Delete Polls
### Administrator:
**Trigger:** The administrator presses the "Delete" button
**Precondition:** The administrator is logged in and can delete polls
**Postcondition:** The administrator has deleted the poll from the database
**Flow of Events:**
- The administrator selects the poll they want to delete and presses the "Delete" button
- The application asks for confirmation: "Are you sure you want to delete this poll?"
- The administrator confirms the deletion
- The poll is deleted from the database
**Exceptional Behavior:**
- If there is nothing to delete, the message "You have not created any polls!" will be displayed