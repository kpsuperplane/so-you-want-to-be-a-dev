# So You Want To Be A Backend Dev

So you want to be a backend dev.  You heard that working on backend development means writing some sort of "server" (whatever _that_ means) and not having to deal with the user interface.  "Perfect," you think to yourself, "I never wanted to touch HTML and CSS anyway."  But what exactly is "backend development"?  It seems that it's an umbrella term that encompasses any code that isn't "directly seen" by the user.  But what does it consist of?  What am I doing when I work on the backend?

## Backend Areas
In this section, we'll try to demystify what it means to work on backend code.  Below is a list of areas that a backend developer might work on:
 - API layer
 - Database layer
 - Architecture
 - Microservices


### API Layer
The API (Application Programming Interface) layer is the segment of code that serves as the "middle man" between your user-facing frontend code and your backend server code.  You can think of it as a set of instructions that your frontend can call to perform a certain task.  Tasks can involve giving a username and getting back the user's details, or updating a user's shopping cart.  More technically, it is a collection of endpoints ([wait... what's an endpoint?](https://stackoverflow.com/questions/2122604/what-is-an-endpoint)) that receives HTTP requests from the client (aka frontend), performs the necessary backend logic, and then returns the appropriate HTTP response back to the client.

[_Side note: we've been assuming that the **client** is the frontend, but it can be anyone calling your server's API endpoints, like another server_]

### Database Layer
The database layer consists of code that interfaces directly with your database (e.g. [SQL](https://www.w3schools.com/sql/), [MongoDB](https://www.mongodb.com/what-is-mongodb)).  It manages the insertion, deletion, and update of database records.

### Architecture
This is arguably the single, most important part of backend.  Just like building architecture, well-designed software architecture can make it super simple to make changes to your code base even years after it was first created.  On the other hand, a badly-designed software architecture is prone to bugs and can even prevent the implementation of certain features without coming up with some hacky solution.  The 2 main categories of software architecture are: 1. Monolithic and 2. Microservices.

Monolithic architectures involve one huge code base that contains all the server code.  It is hard to make changes to the code base and hard to structure teams around it (unscalable for large organizations, but easier to build at the start).  On the other hand, the microservices architecture divides up your backend code into smaller components, called "microservices" (_duh..._), each with its own specific function (promotes *loose coupling*).  Making a change to a function involves just looking within the corresponding microservice.  You can read more about the differences [here](https://medium.com/koderlabs/introduction-to-monolithic-architecture-and-microservices-architecture-b211a5955c63).

Software architecture is more than just the monolithic vs. microservices.  It's the range between them and much more.  It heavily depends on your team's structure and your product.  Coming up with a good backend architecture takes a lot of effort and thinking, but a well-designed one is well worth it.

### Microservices
As mentioned above, microservices are nested components within the larger backend code base that provides certain features for your server.  Some examples include an image server which handles resizing images and applying overlays (which Raphael worked on at Scribd) or a logging tool (like Uber's [zap](https://github.com/uber-go/zap)).



## How Do I Start?
AS seen above, backend development is a big field and has many areas of development.  However, Raphael suggests that a good start would be learning how to create a basic server for a website.  He recommends starting with Node.js as it's relatively to build once you've learnt the basics.  A tutorial on this can be found [here](https://scotch.io/tutorials/build-a-restful-api-using-node-and-express-4). It goes through creating a server, setting up the API layer, and the database layer. You can also check out Raphael's workshop materials on creating a server in Node.js [here](https://github.com/theRoughCode/Road-to-Node).
