# Asynchronous-Programming-with-Async-and-Await-Web-Service
An app retrieves data from a website(web service) and display the result in this app.

This is a simple Windows Form Application using an online web service, implementing async, await, and Threads
Task and Task method run as well as LINQ.

#Developing Environment
IDE: Visual Studio
Framwork: .NET
Programming Language: c#

#Steps
1. Create an WebClient object flickrClient to invoke the online web service
2. Initialize a Task<String> object flickrTask to null(query the web service)
3. Windows Form constructor
4. Create a method(when the user input a text in textbox, and then click the submit button, run the method) to query the web service and display the query result.
5. ----First check if the user started a search previouly(flickrTask is not null and the prior search has not completed)
6. ----Second create a URL(flickrURL) for invoking the web service's method(web service is acutually a set of classes)
7. 
