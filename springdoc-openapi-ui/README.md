# Steps to set up Swagger for Spring Boot Applications

## OpenAPI UI 
The `springdoc-openapi-ui` library covers most of the functionality provided by the `io.swagger` dependencies.

The `springdoc-openapi-ui` library is an alternative implementation of Swagger for Spring Boot applications.

It leverages the Spring Framework's features and annotations to generate OpenAPI documentation and provides a UI interface (Swagger UI) to explore and interact with the documented APIs.

The library includes the core functionality required for generating OpenAPI documentation, such as scanning and parsing your Spring Boot application's endpoints, handling annotations like `@RestController`, `@RequestMapping`, and generating the corresponding OpenAPI specification.

Additionally, `springdoc-openapi-ui` offers several advanced features, including support for - 
- OAuth 2.0, 
- API versioning, 
- customization of the generated documentation, and 
- integration with third-party tools like ReDoc.


However, for most Spring Boot applications, `springdoc-openapi-ui` is a comprehensive and user-friendly choice for generating and exploring OpenAPI documentation but there are some specific features and customizations that are available in `io.swagger` dependencies but not provided directly by spring `springdoc-openapi-ui` .

To name a few features and customization that are not provided directly by `springdoc-openapi-ui` are:

1. **Code-first approach:**
	- `io.swagger` supports a code-first approach, where you can define your API documentation using Java annotations directly in your code, such as 
		- `@Api`, `@ApiOperation`, and 
		- `@ApiModel`. `springdoc-openapi-ui` 
		primarily follows a convention-based approach, where the documentation is generated based on your existing Spring Boot endpoints and annotations.
		
2. **Fine-grained control over OpenAPI specification:**
	- `io.swagger` provides more options for fine-grained control over the OpenAPI specification generation. 
	- You can directly manipulate the `Swagger` object and its components to customize the generated specification. `springdoc-openapi-ui` focuses on generating the specification automatically based on your Spring Boot application and its annotations, but may have limited options for direct manipulation of the specification.
	
3. **Custom extensions and integrations:** 
	 - `io.swagger` allows you to define and integrate custom extensions to the OpenAPI specification, such as vendor-specific extensions or additional metadata. 
	 - While `springdoc-openapi-ui` provides extension points for customization, the range of extensions and integrations available might be more extensive in the `io.swagger` ecosystem.
	 
4. **Compatibility with older versions of Swagger:** 
	- If you specifically need to work with an older version of Swagger, you might find more flexibility and compatibility in the `io.swagger` dependencies. `springdoc-openapi-ui` typically supports the latest OpenAPI Specification version and related tooling.


### Steps to set up Springdoc OpenAPI UI implementation of Swagger UI for a Spring Boot Application on localhost.

Here are the steps to set up the `springdoc-openapi-ui` version of Swagger (Springdoc OpenAPI UI) on your local Spring Boot application:

Step 1: Add `springdoc-openapi` dependencies to your project's `pom.xml` file:

```xml
<dependencies>
<!-- Other dependencies -->      
<!-- Springdoc OpenAPI dependencies -->   
	<dependency>     
		<groupId>org.springdoc</groupId>     
		<artifactId>springdoc-openapi-ui</artifactId>     
		<version>1.5.12</version>   
	</dependency> 
</dependencies>
```

Step 2: Run your application. Make sure to run your Spring Boot application.

Step 3: Access the Springdoc OpenAPI UI. Open your web browser and access the Springdoc OpenAPI UI at the following URL: `http://localhost:8080/swagger-ui.html` (assuming your application runs on port 8080). You should see the Springdoc OpenAPI UI interface with the available APIs documented.

That's it! You have successfully set up the `springdoc-openapi-ui` version of Swagger (Springdoc OpenAPI UI) on your local Spring Boot application. You can now explore and interact with your APIs through the Springdoc OpenAPI UI interface.


