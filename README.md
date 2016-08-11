# Asynchronous-Programming-with-Async-and-Await-Web-Service
An app retrieves data from a website(web service) and display the result in this app.

This is a simple Windows Form Application using an online web service, implementing async, await, and Threads
Task and Task method run as well as LINQ.

#Developing Environment
IDE: Visual Studio
Framwork: .NET
Programming Language: c#

#Steps (Control Flow)
1. Create an WebClient object flickrClient to invoke the online web service
2. Initialize a Task<String> object flickrTask to null(query the web service)
3. Windows Form constructor
4. Create a method(when the user input a text in textbox, and then click the submit button, run the method) to query the web service and display the query result.
5. ----1) Check if the user started a search previouly(flickrTask is not null and the prior search has not completed)
6. ----2) Second create a URL(flickrURL) for invoking the web service's method(web service is acutually a set of classes)
7. ----3) Initialize Windows Form's ListBox
8. ----4) Call WebClient object flickrClient's DownloadStringTaskAsync method using the flickrURL specified as the method's string argument to request information from the server. Assign the task returned from the method to flickrTask.
9. ----5) await fickrTask then parse results with XDocument and assign the result xml document to XDocument object xmlResponse
10. ---6) Gather from each photo element in the XML the id, title, secret, server, and farm attributes, then create an object class FlickResult using LINQ.
11. ---7) retreive attributes value from xml document xmlResponse 
12.----8) Invoke to ToList on the flickrPhotos LINQ query to convert it to list, then assign the result to the ListBox's DataSource property and set the ListBox's DisplayMember property to the Title property.
//end of submit button method
12. When select an item from imageListBox, a method will be called(display the selected image in pictureBox)
13. ---1) Get the selected item's URL
14. ---2) Use WebClient to get selected image's bytes asynchronously
15. ---3) Create a MemoryStream object from imagesBytes
16. ---4) Use the Image class's static FromStream method to create an image from the MemoryStream object and assign the image to the PictureBox's image property to display the selected photo //end 

#links
http://web.csulb.edu/~pnguyen/cecs475/pdf/cshtp5_28.pdf
https://msdn.microsoft.com/en-us/library/hh191443.aspx



