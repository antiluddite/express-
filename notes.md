Make sure you have a separate terminal opened into mongodb
use:

    mongod --dbpath=data 

in the mongodb folder to run.
have that running in the background before you run node-mongoose 



Then install mongoose and mongoose-currency in the nucampsiteServer folder: 
     npm install mongoose@5.10.9 mongoose-currency@0.2.0




What is nodemon?
nodemon is a development tool that automatically restarts Node applications when file changes in the directory are detected. By using it, you will no longer have to stop and restart your running node server every time you make a change. Using nodemon is optional in this course, but highly recommended. 


Installation and usage
Note: In order to prevent nodemon from automatically restarting your application before you've finished updating your code, you will need to turn off Autosave on VS Code and remember to save manually. 
Install it globally with the following command:
npm install -g nodemon
nodemon wraps around the node command. 

To use, it, use nodemon wherever you would normally use the node command. 

example: nodemon server

To use it in the Express server that you just generated, you can go to the package.json file inside the nucampsiteServer folder and replace this line:
     "start": "node ./bin/www"
with
     "start": "nodemon ./bin/www"
Now whenever you run npm start, nodemon will start up and restart your app whenever you make changes to relevant files. Otherwise, you would have to stop your server and restart it manually every time you made a change and wanted to see it take effect.

Use ctrl-c to stop nodemon. 

To be safe, remember to stop nodemon before you install any packages to your project. 

Note: Once again, don't forget you will want to turn off Autosave, so that nodemon will only restart your server when you save manually instead of while you're in the middle of making updates. If you have been used to VS Code auto-saving for you, that means you will need to get in the habit of remembering to save your work manually!
When using node directly from the command line instead of package.json, you can also substitute node with nodemon. In Week 1 of this course, you ran Node applications by entering node followed by the application filename into your terminal, e.g. node app. In that case, you would enter nodemon app instead.
By default, the files watched for changes are  of .js, .json, .mjs, .coffee, and .litcoffee. For information on how to add other file extensions to the watch list, and more details on nodemon, visit the nodemon documentation.

********
workshop 3 mongo db bash terminal:
db.users.update({"username": "admin"}, {$set: {"admin": true}});

db.users.find().pretty()

 "_id" : ObjectId("61fe1a1e1af80da78bec94ea"),
        "firstname" : "robert",
        "lastname" : "smith",
        "admin" : true,
        "username" : "admin",

        "_id" : ObjectId("61fc6df0b451aa74e5fa425e"),
        "firstname" : "maureen",
        "lastname" : "oflynn",
        "admin" : false,
        "username" : "Momo",
*****
to access your mongo shell:
     mongo

     use nucampsite

     db.users.find().pretty()

     db.users.update({"username":"admin}, {$set:{"admin": true}});