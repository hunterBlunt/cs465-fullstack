# cs465-fullstack
## CS-465 Full Stack Development with MEAN

### Architecture
Compare and contrast the types of frontend development you used in your full stack project, including Express HTML, JavaScript, and the single-page application (SPA).
Express: Besides being the E in the MEAN stack, Express is a framework for the Node.js platform. It has provided a variety of mechanics to aid in development. Such as, easing server setup, having a simple interface to route URL’s to controllers, providing templates for HTML views, and applying sessions to remember users.
HTML: This is the most used language for web development and stands for Hyper Text Markup Language. In this project it was used to describe the structure of the web pages.
JavaScript: Like HTML JS is a highly used language in web development. In this project it is used for web page behavior.
Single-page application (SPA): SPA’s allow everything to be run inside the browser without a full page reload. This allows the everything from data processing, user management, and logic to be run inside the browser.

Why did the backend use a NoSQL MongoDB database?
It is the M in MEAN and the preferred database choice of MEAN stack. Unlike relational databases MongoDB uses document store. The reason the backend uses MongoDB is because it uses binary JSON to store documents. This fits extremely well in the MEAN stack which is centered around JavaScript. 

### Functionality
How is JSON different from JavaScript and how does JSON tie together the frontend and backend development pieces?
JSON is the way JavaScript holds data and based on the structure of JavaScript. It works well in tying together the front and backend because MongoDB stores data as binary-JSON, and node and express can interpret it natively and send it to angular. All parts of the MEAN stack is able to use the same data format.

Provide an instance in the full stack process when you refactored code to improve functionality and efficiencies, and name the benefits that come from reusable user interface (UI) components.
When it came to creating the routes and controllers for the api, server, and admin I found it extremely time and energy efficient to be able to reuse code that I had already made. It saved me countless hours of extra work being able to tie everything together so easily.

### Testing
Methods for request and retrieval necessitate various types of API testing of endpoints, in addition to the difficulties of testing with added layers of security. Explain your understanding of methods, endpoints, and security in a full stack application.
To test endpoints before and after security implementation I used Postman to send GET, POST, and PUT requests. This allowed me to verify the backend independent of the user interface. To show understanding here is my Sequence diagram explanation: 
When the user enters the URL for the Travlr Getaway application the client-side will pick it up and it will hit the router. The router will then send the user input and data to the browser, which accepts them to facilitate transactions/ requests sent to the server. The controller will then translate the actor’s input for the server. Once translated the HTTP request will be sent to the applications api router. Depending on the RESTful endpoint of the request the router will send it to one of the two controller/ model’s containing the appropriate functions. The router will direct to one of two controllers: those being the trips and authentication controllers. 
To view the trips list or see a single trip the authentication controller is not required, and the trips controller will request the data from the MongoDB. If successful the database will send the data back to the controller, which will then send it to the Client. From here the controller will translate the request outcome and send it to browser to be viewed.
To login, register, add a trip, or update a trip the authentication controller is required. This will verify if the user is registered against the database, and if not will not allow access to the add trip or update trip functions. Once logged in the user may view trips and access the add trip and update trip functions located in the trips controller. From here it will follow a similar path as described for the customer site above.

### Reflection
How has this course helped you in reaching your professional goals? What skills have you learned, developed, or mastered in this course to help you become a more marketable candidate in your career field?
This course has helped me in terms of professional development. I feel like I can make applications now that I understand how to tie together the frontend, backend, and database. Which has been my limiting factor. Not only has it helped me understand these concepts it has given me practical experience that I can show to future employers, making me a more marketable candidate. 
