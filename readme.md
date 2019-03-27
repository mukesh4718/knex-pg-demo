User App
------------

This app is to handle user. It provides three endpoints:
1. Migrate users table and seed dummy data
2. Get All Users
3. Get User By Id
4. Update User By Id

---------------------------------------------------------

Update User EndPoint:

	Method: POST
	EndPoint: http://localhost:8080/api/users/1
	Header: {
		"Content-Type":"application/json"
	}

	body: {
    "email": "mukesh@technologies33.com",
    "first_name": "Mukesh Kumar",
    "last_name": "Pandey"
  }


---------------------------------------------------------

Get User List EndPoint

	Method: GET
	EndPoint: http://localhost:8080/api/users
	Header: {
		"Content-Type":"application/json"
	}


---------------------------------------------------------

Get One User EndPoint

	Method: GET
	EndPoint: http://localhost:8080/api/users/<userId>
	Header: {
		"Content-Type":"application/json"
	}


---------------------------------------------------------



  Note :
    Assuming Node v6 and Postgresql latest is installed, if not please install both. Following steps are used to migrate database and seeding: 

    1. npm install
    2. ./node_modules/.bin/knex migrate:latest
    3. ./node_modules/.bin/knex seed:run