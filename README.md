# Tips

*This chat room is modified from a templete on the Internet*

*It uses socket.io instead of ajax & long polling, and it doesn't use any database, if you need the chatting data, you can require mysql in route.js and save data.msg to your local mysql database*

## Usage

* Run $node app.js
* Use url *localhost:8080* to go to login page.

## How to Merge

* Merge app.js, config.js and route.js to yours.

* Change the route *'/'* to whatever you need in route.js and give two people in a same root a same id before redirecting.

* In this demo, You need to input name and email first. What you should do is:

  * Delete <code> < div class="connected"> </code> part in *chat.html* and send the name and email from your page to *chat.js*.

  * Modify <code> socket.on('peopleinchat', function(data){ </code> part in *chat.js* to receive your massages and save them to variable email and name and run <code> socket.emit('login', {user: name, avatar: email, id: id}); </code> to start chatting!  
