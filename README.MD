FOR BACKEND

1. -- npm init
2. -- npm i express mongoose and cors
   express for hostind and building the server
   mongoose is for contacting the mongoDB API relation
   cors is to relate the front end and backend projects
3. -- npm i -D nodemon concurrently
   nodemon is for automate the saving of the website it will automatically save the code
   concurrently is for to run the front end and backend simontaneously
4. now create a new js file called server.js after creating import the modules

## for to run the backend

1. first you should change the scripts in package.json
   intially it is like this
   <code>
   "scripts": {
   "test": "echo \"Error: no test specified\" && exit 1"
   },
   </code>

but we should change like this
<code>
"scripts": {
"start" : "node server"
},
</code>

2. after that we should write about the nodemon in scripts
   "server" : "nodemon server"
3. the final scripts code is like given below

<code>"scripts": {
"start" : "node server",
"server" : "nodemon server"
},</code>

# final step

1. in terminal -- npm run server

### total boilerplate code for to run server

<code>
const express = require("express")
const mongoose = require("mongoose")
const cors = require("cors")
const app = express()
app.use(cors())
app.use(express.json())
app.listen(6000, () => {
console.log("Server is Running!")
})
</code>
