# Node js app deployment on Heroku Server
NOTE: ALL COMMANDS NEED SHOULD BE RUN FROM ROOT OF YOUR PROJRCT USING CMD.

Steps to Deploy:

1. Visit this link (https://devcenter.heroku.com/articles/heroku-cli), download and install Heroku CLI.
2. Open Environment variable and add (C:\Program Files\heroku\bin) this in path, so that heroku become accessible in CMD.
3. Check for installed version using (heroku --version) this command, you will get something like this 
    (heroku/7.21.0 win32-x64 node-v11.9.0) based on your node js installed version.
4. Create Procfile ==> This file tells how to start the node js web server or give the entry point once the deployment is successful.

// Procfile will contain the given line, For my application the entry point is server.js ==> web: node server.js

5. Visit this link (https://id.heroku.com/login) and sign up on Heroku to create a account if you don't have one.

6. Logging Into Heroku From Terminal ==> Run this command from cmd (heroku login). It will take you to the      login page, once logged in    close the page and return to CMD.

7. Now you need to initialize git in your app for that run this command (git init) using CMD.
8. Now we need to create a name for our application for that run this command (heroku create). It will give a random name to your              application. Better not to change as this name will get added to your application URL, but you can change it using this command 
   (heroku rename new_name)
   
// My Folder Structure:
    ==> .env --> This file will contain ==> PORT = 8081 --> For my application i used port 8081 you can also used the same if this port is     free
    ==> .gitignore to ignore files from getting added to commit ==> This file will contain ==> /node_modules package-lock.json /.env
    ==> Package.json
    ==> Procfile
    ==> Server.js (Entry Point)
   
9. Now run this command (git add .) to add file to commit.
10. The commit these files by runnig this command (git commit -m "Heroku Deployment")
11. Now Push the changes to the server ==> Run this command (git push heroku master) ==> After that, you can see that we have               successfully deployed our application to heroku.
12.Now run this command (heroku open) to open the application in live.

AFTER DEPLOYMENT STEPS
1. Run this command (heroku logs) to check logs releted to your application.
2. Run this command (heroku ps:scale web=1) to check and verify whether your application is up and running.
3. Run this command (heroku local web) if you want to run the same application from local port, it will open in 8081 port which we gave    in .env file with this link (http://localhost:8081/)

================================HAPPY COADING==============================





