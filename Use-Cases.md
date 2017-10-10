## Use Cases

Written with Gherkin. For information about Gherkin: [Gherkin Language](https://github.com/cucumber/cucumber/wiki/Gherkin)

### Registration

  ```gherkin
Feature: Registration
	User should be registered to use the application's features
	User should enter valid information to register
	If the user enters an email/username that has already been used, a warning message should be displayed

Scenario: Successful Registration with Valid User Information
	Given User is on Home Page
	When User enters Email, UserName, Password and Re-type Password
		And User clicks Sign up button
	Then User is redirected to Followed History Items page
	
Scenario: Unsuccessful Registration with already existing username/email
	Given User is on Home Page
	When User enters Email, UserName, Password and Re-type Password
		And Username/Email is one that already has been registered before
		And User clicks Sign up button
	Then Username/Email is already registered message is displayed
```

### Login

  ```gherkin
Feature: Login
	A user shall login to the system to use its features
	User should enter valid credentials which he/she enters during registration to login

Scenario: Successful Login with Valid Credentials
	Given User is on Home Page
	When User Navigates to Login Page
		And User enters UserName and Password
		And User clicks Login button
	Then User is redirected to Followed History Items page

Scenario: Successful LogOut
	When User clicks Logout button
	Then User is redirected to Home page
```

### Add annotation

  ```gherkin
Feature: Add annotation

Scenario: Adding annotation to description of a living history item
	Given user is logged in to the system
	When User Navigates to a specific history item's page
		And User selects the text to add annotation
		And user selects picture/text/video/sound from the pop up on the right side
		And user uploads a file from the local file system
		And user clicks submit
	Then annotation is added for the selected text
	
Scenario: Adding annotation to picture of a living history item
	Given user is logged in to the system
	When User Navigates to a specific history item's page
		And User drags the cursor around the area he/she wants to annotate on the picture
		And user selects picture/text/video/sound from the pop up on the right side
		And user uploads a file from the local file system
		And user clicks submit
	Then annotation is added for the selected picture area
```

### View Living History Item Annotation

  ```gherkin
Feature: View Living History Item Annotation

Scenario: View annotation on a picture
	Given User is on Home Page
	When User Navigates to a specific history item's page
		And User clicks the highlighted area on the picture
	Then annotations on the highlighted area are listed on the right side
	
Scenario: View annotation on a description
	Given User is on Home Page
	When User Navigates to a specific history item's page
		And User clicks the highlighted text on the description
	Then annotations on the highlighted text are listed on the right side
```