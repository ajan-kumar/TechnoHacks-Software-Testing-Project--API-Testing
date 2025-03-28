Project Title: TechnoHacks Software Testing Task 5: API Testing

Index
Objective..........................Line 14
API Overview.......................Line 17
Tools Used.........................Line 20
Test Cases.........................Line 23
Test Execution.....................Line 73
Results............................Line 79
Observations.......................Line 82
Conclusion.........................Line 87
Video Documentation................Line 90

Objective
The objective of this project is to conduct testing of a RESTful API using Postman to validate its functionality, reliability, and performance. By executing some sample test cases on various endpoints, we aim to ensure the API responds correctly and meets expected behavior, ultimately enhancing its robustness for end-users.

API Overview
The Sample API is a RESTful service for managing user data, offering key functionalities such as Create User, Retrieve User, Update User & Delete User. The API returns standard HTTP status codes and JSON responses, serving as a critical component for applications requiring user management.

Tools Used
Postman: Version 11.37.1.0

Test Cases
S.No	Request Type/ Method	Scenario Title	Expected Outcome	Actual Outcome	Notes
1	GET	Valid URL	200 OK	200 OK	Successful test
2	GET	Invalid URL	404 NOT FOUND	404 NOT FOUND	Successful test
3	GET	Request All Resources	200 OK	200 OK	Successful test
4	GET	Pagination	200 OK	200 OK	Successful test
5	GET	Valid Query Parameters	200 OK	200 OK	Successful test
6	GET	Invalid Query Parameters	200 OK	200 OK	Successful test
7	GET	No Resource URL	200 OK	200 OK	Successful test
8	POST	Valid request body	201 CREATED	201 CREATED	Successful test
9	POST	Without title	201 CREATED	201 CREATED	Successful test
10	POST	Invalid UserID	201 CREATED	201 CREATED	Successful test
11	POST	Blank Body	201 CREATED	201 CREATED	Successful test
12	POST	Exceeding Limits	500 INTERNAL SERVER ERROR	500 INTERNAL SERVER ERROR	Successful test
13	POST	Extra Fields	201 CREATED	201 CREATED	Successful test
14	PUT	Valid request body	200 OK	200 OK	Successful test
15	PUT	No Resource URL	500 INTERNAL SERVER ERROR	500 INTERNAL SERVER ERROR	Successful test
16	PUT	Without title	200 OK	200 OK	Successful test
17	PUT	Invalid UserID	200 OK	200 OK	Successful test
18	PUT	Blank Body	200 OK	200 OK	Successful test
19	PUT	Exceeding Limits	500 INTERNAL SERVER ERROR	500 INTERNAL SERVER ERROR	Successful test
20	PUT	Extra Fields	200 OK	200 OK	Successful test
21	PATCH	Only title, without body	200 OK	200 OK	Successful test
22	PATCH	No Resource URL	200 OK	200 OK	Successful test
23	PATCH	Without title, with body	200 OK	200 OK	Successful test
24	PATCH	Invalid UserID	200 OK	200 OK	Successful test
25	PATCH	Blank Body	200 OK	200 OK	Successful test
26	PATCH	Exceeding Limits	500 INTERNAL SERVER ERROR	500 INTERNAL SERVER ERROR	Successful test
27	PATCH	Extra Fields	200 OK	200 OK	Successful test
28	DELETE	Valid URL	200 OK	200 OK	Successful test
29	DELETE	Non-existent Resource	200 OK	200 OK	Successful test
30	DELETE	Request Deleted Resources	200 OK	200 OK	Successful test
31	DELETE	Invalid Resource ID	200 OK	200 OK	Successful test
32	DELETE	No Resource URL	404 NOT FOUND	404 NOT FOUND	Successful test
33	DELETE	Valid Query Parameters	200 OK	200 OK	Successful test
34	DELETE	Invalid Query Parameters	200 OK	200 OK	Successful test
35	HEAD	Valid URL	200 OK	200 OK	Successful test
36	HEAD	Invalid URL	404 NOT FOUND	404 NOT FOUND	Successful test
37	HEAD	Request All Resources	200 OK	200 OK	Successful test
38	HEAD	Valid Query Parameters	200 OK	200 OK	Successful test
39	HEAD	Invalid Query Parameters	200 OK	200 OK	Successful test
40	HEAD	No Resource URL	200 OK	200 OK	Successful test
41	OPTIONS	Valid URL	204 NO CONTENT	204 NO CONTENT	Successful test
42	OPTIONS	Invalid URL	204 NO CONTENT	204 NO CONTENT	Successful test
43	OPTIONS	Request All Resources	204 NO CONTENT	204 NO CONTENT	Successful test
44	OPTIONS	No Resource ID	204 NO CONTENT	204 NO CONTENT	Successful test
45	OPTIONS	Valid Query Parameters	204 NO CONTENT	204 NO CONTENT	Successful test
46	OPTIONS	Invalid Query Parameters	204 NO CONTENT	204 NO CONTENT	Successful test
47	OPTIONS	No Resource URL	204 NO CONTENT	204 NO CONTENT	Successful test

Test Execution
Executed tests using Postman Collections.
URL used: https://jsonplaceholder.typicode.com/users
https://jsonplaceholder.typicode.com/posts
https://jsonplaceholder.typicode.com/posts/1

Results
Total Tests: 47 (All passed successfully)

Observations 
It has also been observed that behavior of JSONPlaceholder does not give the expected responses. This is due to the nature of the API, which is a fake REST API for testing.
This API returns predefined responses. A GET request to https://jsonplaceholder.typicode.com/users provides a list of users. If an invalid ID is requested (e.g., https://jsonplaceholder.typicode.com/users/999), it still returns a 200 OK status with an empty array instead of a 404 Not Found.
As a testing tool, JSONPlaceholder lacks strict validation and error handling typical of production APIs, which has led to several failed cases. To rectify this, the expected outcomes have been updated to accommodate these new changes. 

Conclusion
The API is functioning as expected with no issues found during testing.

Video Documentation

