POST /blogs
Create a blog document from request body. Get authorId in request body only.

Make sure the authorId is a valid authorId by checking the author exist in the authors collection.

Return HTTP status 201 on a succesful blog creation. Also return the blog document. The response should be a JSON object like this

Create atleast 5 blogs for each author

Return HTTP status 400 for an invalid request with a response body like this



Updates a blog by changing the its title, body, adding tags, adding a subcategory. 
(Assuming tag and subcategory received in body is need to be added)

Updates a blog by changing its publish status i.e. adds publishedAt date and set published to true
Check if the blogId exists (must have isDeleted false). 

If it doesn't, return an HTTP status 404 with a response body like this
Return an HTTP status 200 if updated successfully with a body like this

Also make sure in the response you return the updated blog document.



Returns all blogs in the collection that aren't deleted and are published
Return the HTTP status 200 if any documents are found. The response structure should be like this
If no documents are found then return an HTTP status 404 with a response like this
Filter blogs list by applying filters. Query param can have any combination of below filters.
By author Id
By category
List of blogs that have a specific tag
List of blogs that have a specific subcategory example of a query url: blogs?filtername=filtervalue&f2=fv2




Allow an author to login with their email and password. On a successful login attempt return a JWT token contatining the authorId in response body like this
If the credentials are incorrect return a suitable error message with a valid HTTP status code