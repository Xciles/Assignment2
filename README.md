# Assignment 2
The customer approved your previous Assignment and would like your help again to fix an issue they are having.

The customer manages Cars for various companies and projects assigned to various users. A developer created an API which 3rd parties can use and consume when updating information. 
Unfortunately, the developer left the company and never told where they could find the source code for this API. 

You have been hired to recreate the API based on the swagger documentation and the following tiny bit of information the customer has.

## Info

The customer told us that they manage the following entities:
* Company
* Car
* User 
* Project (opt)
* Skill (opt)

Relationships between the entities are as follows (*all are One-to-Many relationships*): 
* A Company can have multiple Cars
* A Car can have a User
* A Car can have a Company
* A User can have multiple Cars
* A User can have multiple Projects
* A Project can have multiple Skills

## Tasks

1. Create ASP.NET Core API project
2. Define Entities
3. Create the Database (DbContext)
4. Define the API based on the swagger.json

## Tasks V2

1. Implement the new custom API Calls
	* All cars from a specific company, including the current user. (either by id or by name)
	* All cars from a specific company, order by name, return sets of 20 and start on x.
	* Batch insert of multiple cars. 
		* Parallel processing
2. Split or seperate the application logic in logical more manageable parts.
3. Introduce some Many To Many relationships. 
	* Project <-> Skill
	* Skill <-> User
	* User <-> Project

## Tasks V3

You now have multiple controllers and repeated logic. Please:
1. Move the logic out of the controllers into custom classes that handle database communication for a certain type.
2. Introduce generics to minimize code duplication.
3. Use dependency injection. 
4. Find out and descibe the pros and cons when using generics in this situation.
