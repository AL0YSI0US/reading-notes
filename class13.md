# Code 301 Reading Notes

## Class 13

[<== Previous Lesson](class12.md) [Next Lesson ==>](class14.md)

[<== Home](README.md) 🏠

# Crud

1. In your own words, describe what each group of status code represents:
   * 100’s = headcheck! informational codes before body is sent
   * 200’s = V I C T O R Y ! sans 202...in which case: google
   * 300’s = Mails piling up: no one lives here anymore!
   * 400’s = OOPS invalid request codes
   * 500’s = Your server mad bro?
2. What is a status code 202? **asynchronous** processing of a request [fail]
3. What is a status code 308? please try your call again . . . permanent redirect
4. What code would you use if an update didn't return data to a client? 204
5. What code would you use if a resource used to exist but no longer does? 410
6. What is the ‘Forbidden’ status code? 403

## Additional Resources

### Videos

* [Build A REST API With Node.js, Express, &amp; MongoDB - Quick](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw) - First 20 minutes

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
2. What is middleware?

   1. it is the software that lies btween the operating system and the applications that are being run on it.
3. What does `app.use(express.json())` do?

   1. its the middleware of the application
   2. an inbuilt "express method" used to recognize the incoming request objectas a JSON Object.
4. What does the `/:id` mean in a route?
5. What is the difference beween `PUT` and `PATCH`?

   1. PUT is a method of modifying resource where the client sends data that updates the entire resource. It is used to set an entity’s information completely. PUT is similar to POST in that it can create resources, but it does so when there is a defined URI. PUT overwrites the entire entity if it already exists, and creates a new resource if it doesn''t exist.
   2. For example, when you want to change the first name of a person in a database, you need to send the entire resource when making a PUT request.
   3. **{****“first****": "****John****", "****last****": "****Stone”****}
   4. To make a PUT request, you need to send the two parameters; the first and the last name.
6. How do you make a defalut value in a schema? with a function, you set its key value pairs, the name you choose and the data type: ex : boolean string etc...
7. What does a `500` error status code mean? internal server error
8. What is the difference between a status `200` and a status `201`? 200 means things went well, 201 is the create code

### Reading

* [Sending Form Data](https://developer.mozilla.org/en-US/docs/Learn/HTML/Forms/Sending_and_retrieving_form_data)
* [Status Codes Based On REST Methods](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)

[<== Home](README.md) 🏠
