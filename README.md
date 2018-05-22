### A simple demo to show what restful apis are by using springmvc.
---

## Run this project
1. Clone the source.
```
git clone https://github.com/swsmile/RESTfulDemo
```

2. Enter source code and run ```mvn tomcat7:run``` tomcat maven plugin to start the project (which is a Tomcat plugin so you don't need to install a Tomcat manually.


Note: If the running fails, you can use `mvn compile` to generate a `Restful.war` and deploy `.war` in Tomcat manually by copying `.war` into `.../apache-tomcat-9.0.8/webapps/`.

3.Visit [http://localhost:8080/Restful/user](http://localhost:8080/Restful/user) to retrieve the data.

## Get a specific data:

Visit [http://localhost:8080/Restful/user/1](http://localhost:8080/Restful/user/1), and it will return 
```
{  
   "id":1,
   "name":"Beckett",
   "age":38,
   "salary":150000.0,
   "gender":"Male"
}
```

## Update an employee:

Visit http://localhost:8080/Restful/user/1 by using the http verb ```PUT``` to update by ID with the following request body:

```
{  
   "id":1,
   "name":"Beckett-modified",
   "age":38,
   "salary":150000.0,
   "gender":"Male"
}
```

Note: you can use `Postman` to to send a `PUT` request by specifying the HTTP method as `PUT` (remember to set the request header "content-type" as "application/json").

## Delete an employee.
 Visit [http://localhost:8080/Restful/user/1](http://localhost:8080/Restful/user/1) by using the http verb ```DELETE``` to delete by ID.

## Create an new employee
Visit http://localhost:8080/Restful/user/5 by using the http verb ```POST``` to create a new one employee with HTTP header ```Content-Type = application/json``` and the following body:

 ```
 {  
   "id":5,
   "name":"Tom",
   "age":38,
   "salary":150000.0,
   "gender":"Male"
}
 ```



This repo forks from https://github.com/loveppears/SpringMVC_RESTful.