# Basic cURL Command

- [Documentation](https://curl.haxx.se/docs/) 
- [Basic cURL Tutorial](https://www.youtube.com/watch?v=7XUibDYw4mc&t=2s) by Traversy Média Tutorial
- The cURL command prompt comes with Git Bash when Git is installed
- [JSONPlaceholder](https://jsonplaceholder.typicode.com/) - Fake Online REST API for Testing

This help text
````
curl -h or --help  
````
Get the cURL current installed version 

````
curl -V or --version
````

Make http request to the API to return json response

````
curl https://jsonplaceholder.typicode.com/posts
````
passing URL argument to return the post id = 2

````
curl https://jsonplaceholder.typicode.com/posts/2
````

**Using options** 

Include protocol response headers in the output

````
-i or --include
````

````
curl -i https://jsonplaceholder.typicode.com/posts/2
````

Only include the headers

````
-I or --head
````

````
curl -I https://jsonplaceholder.typicode.com/posts/2
````

Write to file instead of terminal output
note : run Git bash into the your directory

````
-o or --output 
````

````
curl -o test.json https://jsonplaceholder.typicode.com/posts/2
````

Read the file in the terminal

````
cat test.json
````
Open the file in the code editor (VSCode)

````
code . test.json
````
Delete test.json

````
rm test.json
````

Download file
note: the O flag is uppercased

````
curl -O https://jsonplaceholder.typicode.com/posts
````
note : the generated file has no extension

Read the file in the terminal

````
cat posts
````

Download an image from its URL 

````
curl -O https://www.google.com/images/branding/googlelogo/2x/googlelogo_color_272x92dp.png
````

note : now the folder contains googlelogo_color_272x92dp.png file

HTTP POST request - creating a resource/data 

````
object sent
-d or --data <data>
````

````
curl --data "title=Hello&body=Hello world" https://jsonplaceholder.typicode.com/posts
````

HTTP PUT request - updating a resource

````
-X or --request <command> Specify request command to use
-d or --data <data>   HTTP POST data
````
````
curl --request PUT --data 'title=Hello&body=Hello world' https://jsonplaceholder.typicode.com/posts/3
````
or 
````
curl -X PUT -d "title=Hello&body=Hello world" https://jsonplaceholder.typicode.com/posts/3
````

HTTP DELETE request - deleting a resource

````
curl --request DELETE https://jsonplaceholder.typicode.com/posts/3
````
or 
````
curl -X DELETE https://jsonplaceholder.typicode.com/posts/3
````
pause at https://youtu.be/7XUibDYw4mc?t=626





