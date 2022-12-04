This is a school project about building a distributed chat application using C Sockets. This application has a very similar functioning to Discord, i.e. you can talk in a **general** channel, you can send private messages to other users, and you can create new **channels**.

Demo of running the program step by step:
- in directory /Serveur, use `make`, then `make run` => the server is running!
- in directory /Client, use `make`
- now run as many clients as you want, by using the command **./client `serv address` `user_name`** (e.g. ./client 127.0.0.1 Lucas)
- now the different users can chat!
- ⚠️⚠️ P.S: For the application to work properly, you must run the server from the ./Serveur directory, if you run it from another directory (e.g. from APPLICATION-CHAT-SAAD-ARTHUR), some features may not work (e.g. saving the history). For the client, you can run it from whatever directory you want.

List of developed features so far:
- talk in the *general channel*: when you connect with a new user, you join this channel by default, you will see all messages written in the channel, and be able to send your own message that everyone can see.
- send private message to another user: use command **/m "user_name" [message]** 
- join a private channel: use command **/join [number]** to join a private channel (the parameter needs to be a number, for now strings aren't supported for channel names)
- the historic of every channel is saved and displayed whenever you join the channel. All historics are deleted when the server shut down.