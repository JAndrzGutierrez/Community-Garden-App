# Community-Garden-App

# Project Overview

## Project Links

- https://github.com/JAndrzGutierrez/Community-Garden-App/()
- [add your deployment link]()

## Project Description

Currently there is a need for an app that allows people to sign up and volunteer in the community garden of New Kent County, VA.
My version 0.1 for this Community Garden app will be coded using the following languages and frameworks.
React.js
Django for the back-end.
anime.js 
This app will allow you to register to sign up to help in the community garden completing different tasks around the garden.

## Database Structure

User Model: 
Name: Juan Andres
Email: techmoney@gmail.com	
Password: 123456

User model  
Routes: 
/sign-up/
/sign-in/
/sign-out/
/change-password/

Garden_Tasks Model:
task:
status:
gardener

Routes
garden_tasks/


Full CRUD Actions implemented


## Wireframes

Upload images of wireframe to cloudinary and add the link here with a description of the specific wireframe. Also, define the the React components and the architectural design of your app.

- [add link to your wireframes]()
- [add link to your react architecture]()


### MVP/PostMVP - 5min

The functionality will then be divided into two separate lists: MPV and PostMVP.  Carefully decided what is placed into your MVP as the client will expect this functionality to be implemented upon project completion.  

#### MVP
- The user should be able to Register 
- The user should able to see tasks and completion 
- Allow user to interact with the page

#### PostMVP 

- Donations model
- Shop



## Additional Libraries
anime.js


## Code Snippet
TASK_STATUS = (
    ("Pending", "Pending"),
    ("Completed", "Completed"),
    ("Cancelled", "Cancelled"),
)

class Garden_Tasks(models.Model):
    task = models.CharField(max_length=100)
    status = models.CharField(max_length=100, choices = TASK_STATUS,
    default = "Pending")
    gardener = models.ForeignKey( get_user_model(), on_delete=models.CASCADE, related_name="Garden_Tasks")
    created_at = models.DateTimeField(auto_now_add=True)
    updated_at = models.DateTimeField(auto_now=True)

