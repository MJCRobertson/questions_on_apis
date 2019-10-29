# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?

  The create_router.js file within helpers is responsible for pre setting the routes that it will follow.


2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

  The Client folder is responsible for all of the front end work, Vue, JS etc while the server side is responsible for all of the backend stuff and the database handling.

3. What are the the responsibilities of server.js?

  The server.js is responsible for passing along the data from the database (mongodb) to the creat router file which will then in turn pass the data packaged up over to the front end to use within the client directory.

4. What are the responsibilities of the `gamesRouter`?

  The games router is a template for the assigning of the web addresses to each of the restful routes required.

5. What process does the the client (front-end) use to communicate with the server?

  Slightly unsure on this but i think it uses an eventBus?

6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

The fetch method can take a .then method, which if the current action is successfull, will then carry out the next .then until completion. And also it has the .catch method, which is the fallback if the .then cannot be completed.

7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

??????????????????????????????????????????????????????????????????????????????????????????????????

8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

To create and change databases which are non relational.

## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Add to your diagram the dataflow for removing a game.
