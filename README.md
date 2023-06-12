# DBMS

## 1. Write SQL query to get the details of employees from emp table except for employees whose first name is Amrit and Ankit

select * from employees where not (first_name like 'Amrit' or firstname like 'Ankit');

## 2. Create an XPath of an element that has a text. This XPath should be created in such a way that even if the developer changes the text from upper case to lower case or vice versa, the XPath should work.

//*[lower-case(text()) = lower-case('Your Text')]

## 3. How to validate response data.

For API response check this things:
1. status code
2. response content type
3. response body

General way:
1. Understand the response data format:  Determine the format of the response data, such as JSON, XML, or plain text. This will help you choose the appropriate method or library for parsing and extracting data.
2. Parse the response if required
3. Extract the relevant the data
4. Define validation criteria
5. Implement validation logic


## 4. If response data in an API contains Id in String and integer format. How will you check that it should be a string? Answer-Using JSON Schema Validator

```python
import jsonschema
schema = {
  "type":"object",
  "properties": {
    "Id": {
      "type":"string"
  },
  "required":["Id"]
}

try:
  jsonshema.validate(response_data, schema)
  print("Object has valid data")
except jsonschema.exceptions.ValidationError:
  print("Validation error")
```

## 5. Where you will keep the schema file and why?
The location where you keep the schema file depends on various factors, such as the structure of your project and the specific needs of your application. Here are a few common options for storing the schema file:

1. **In the same directory as the code**: You can keep the schema file in the same directory as your code files. This approach is simple and convenient, especially if the schema is closely related to the code that uses it.

2. **In a separate "schemas" directory**: You can create a dedicated directory named "schemas" or something similar to store all your JSON schema files. This helps in organizing and centralizing your schema files, making it easier to maintain and manage them.

3. **In a version control repository**: If you're using version control, you can store the schema file in the same repository as your code. This allows you to track changes to the schema over time and collaborate with others effectively.

4. **As a part of a documentation system**: If you have a documentation system or platform for your API, you may consider including the schema file as part of the documentation. This ensures that the schema is easily accessible to developers and can be referenced when working with the API.

The choice of location for the schema file depends on your specific requirements and development practices. It's important to consider factors such as code organization, collaboration needs, and ease of access when deciding where to store the schema file.

## 6. If you have an API that has 4 attributes in each record like firstName, lastName, id, address. The same fields are present on UI. Now if the developer changes keyName from firstName to Name. What will be the impact on UI? Will you get an error. If yes, then why. If not, then why?

Ofc, we will get error. As we are getting value through key from the object.

## 7. Explain the framework that was used in your project.

## 8. In the object repository can you place locators as per CSS and Xpath both. How?

No, we should be using any one on the basis of following notes:-

-> CSS is faster than XPath, because it allows the browser to do less work for identifying the UI element. Also, IE cannot do XPath natively (which might have changed with recent versions).

-> CSS is cleaner and easier to write than XPath. Think “#username” vs. “//*/[@id='username']”.

-> XPath is much more versatile than CSS and allows you to identify any elements by partial text, or identify an element and then select it’s parent, etc.

## 9. Can we make an abstract class static?

## 10. What are inner and outer class?

## 11. What modification happened to Interfaces after Java8?

## 12. Can we have static methods in interfaces?

## 13. Create a phone directory using the oops concept and retrieve the details of the 10th record.

## 14. Program to find duplicate characters in a string.

## 15. Explain dropdown handling in selenium.
