# authentication-and-authorisation-with-expressjs
Quest 3  of Stackup Nodejs JWT Expressjs

## Challenge Part 2: Explanation

_Explain if this requirement “This delete user functionality can be done after authentication” is a good idea or a bad idea based on your gained knowledge about authentication and authorisation and add additional explanation why these two concepts are different_


1. Authentication is the process of verifying the identity of a user. I usually requires the user to provide some credentials, such as username and password. It gives the server a way of knowing who is trying to access the server and its services. We could say that authentication gives an answer to the server's question: "Who you are?"
2. Authorisation is the process of determining what and how a user can do. I usually requires the user to be logged in. It gives the server a way of knowing who can access the server and which of its services. While authentication is linked to the user which is legally registered into the database, authorization is linked to the permissions of the logged user. According to the defined level of permissions, the user can perform certain actions. Therefore, the authorisation is the answer to the server's question: "What you're allowed to do?"
3. The delete account/user functionality is vital in our application because it permanently removes a user from the system and from the database, and the user cannot be recovered. In order to delete a user, the user needs to be logged in.
4. In our case, we gave the possibility to the authenticated user to delete their account, thus the user automatically loses the ability to log in and needs to register again in order to authenticate themselves. But, we added the functionality to delete other user's account by providing their username. Now, this is something that should be kept reserved for administrators and/or for the owner of the relative account. That is where the authorisation comes in. It checks the permissions for certain actions by the specific roles a user can have. These roles are defined in the database, whilst the controllers are defined in the routes.