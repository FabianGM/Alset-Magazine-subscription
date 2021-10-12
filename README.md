# Alset Magazine subscription
**This project is made with Blazer and .NET Core MVC**
It is a project that was finished in 24 hours and there are a few additional things missing. The time limit to develop it was 48 hours, but hey, it is interesting to take on the challenge in less time.
---
[![Alt text](img/2.png)](https://youtu.be/Z8Hlo6yAaRI)

## Video showing its operation
---
https://youtu.be/Z8Hlo6yAaRI

Once the project is downloaded, the following steps must be performed:
---
## Step 1 Installation
1. Install ASP .NET CORE
2. Use Postman or a tool to run the API
3. SQL Server

## Step 2 Initialize the Back-End and Front-End of the application

Move to the folder BlazorStore.Client and run dotnet run in this way the Fron-End will be executed as shown in the following image:

![alt text](img/BlazorClient.png)

Move to the Blazor Store.Server folder and run dotnet run in this way the Banck-End will be executed as shown in the following image:

![alt text](img/BlazorServer.png)

Both must be kept running for the Back-End and Fron-End to work.
## Step 3 Create User

There is a default user in the project which can be accessed in the following way:
You must send a POST to activate the authentication by JASON WEB TOKEN in this way
---
https://localhost:5011/api/login
---
`
{
    "user":"user",
    "password":"user"
}

`
---
![alt text](img/user_default.png)

and then you can enter with these credentials

1. username: user
2. password: user

This user is only a test user but below I will show how to create another test user but from the database:

### First

We create a database with the name Store
---
![alt text](img/Store_DB.png)

### Second

Run the endpoint to add new users
---
https://localhost:5011/api/userprofile
---

`
{
    "userName":"user1",
    "password":"user1",
    "email":"user1@gmail.com",
    "name":"user1",
    "country":"Ecuador"
}

`
---
![alt text](img/endpoint1.png)
---
![alt text](img/data1.png)
---
You can see that thanks to the use of Entity Framework the necessary tables will be created automatically and in turn you will also see that the users that you wrote will be added

## Step 4 Add magazines
---
Run the following endpoint and add the necessary journals to the body
---
https://localhost:5011/api/game
---
`
{
    "title":"Serious Game Design and Clinical Improvement in Physical Rehabilitation: Systematic Review",
    "description":"Serious video games have now been used and assessed in clinical protocols, with several studies reporting patient improvement and engagement with this type of therapy. Even though some literature reviews have approached this topic from a game perspective and presented a broad overview of the types of video games that have been used in this context, there is still a need to better understand how different game characteristics and development strategies might impact and relate to clinical outcomes.",
    "image":"https://asset.jmir.pub/assets/5f03caff26a1910489ddec937b01fe44.png",
    "price":"90",
    "discountRate":"0"
}

`
---
![alt text](img/data1.png)






