# HRM and Task Management Backend
This is the backend portion of a web application that focuses on human resource management and task management. It was developed using PHP Laravel and a PostgreSQL database.

## Installation
Clone this repository to your local machine.
Run `composer install` to install all dependencies.
Create a PostgreSQL database and update the DB_* variables in the .env file to match your database settings.
Run `php artisan migrate` to run the database migrations.
Run `php artisan serve` to start the development server.
Usage
The API has the following endpoints:

* prefix - /api/auth - APIs responsible for authentication and authorization. Registration, Login, Password Reset,
* prefix - /api/project - APIs for creating, editing, deleting, and retrieving the project entity.
* prefix - /api/task - APIs for creating, editing, deleting, and retrieving the task entity.
* prefix - /api/calendar - APIs for creating, editing, deleting, and retrieving the calendar and event entities.
* prefix - /api/company - APIs for creating, editing, deleting, and retrieving the company entity.
* prefix - /api/profile - APIs for editing and retrieving the user entity.
* prefix - /api/chat - APIs for sending and storing messages.

## Libraries
* jwt - responsible for authorization processes, generates tokens to validate the user, the token consists of three parts: header, payload, signature.

* mailer - automates the process of sending emails. Applied for email verification system.

* google-api-php-client - for working with Google services, provides a client that can be integrated with Google APIs, used for creating events with video conferencing (Google Calendar API).

# BASUM Frontend

## Installation and Setup Instructions
You will need `node` and `npm` installed globally on your machine.  
Installation:
`npm install`  
To Start Project:
`npm start`  
To Visit App:
`http://localhost:3000`  

## Technologies
##### Ant Design:
Ant Design is a complete design system, a visual language. With its own principles, style guides and a library of components. [link](https://ant.design)
##### React Router Dom v6:
React Router is a solution for switching and routing React pages. [link](https://www.npmjs.com/package/react-router-dom)
##### Axios:
Axios is a Promise-based HTTP client for node.js and the browser. Used to integrate with the project server. [link](https://www.npmjs.com/package/axios)
##### Socket io
Socket.IO is a library for building real-time, bi-directional, and event-based applications. Used to create a chat within the project between the participants. [link](https://www.npmjs.com/package/socket.io)

## Pages
|Page|Description|Route|
|---|---|---|
|**Login**|Authorization page for an existing user|`/auth/login/`|
|**Registration**|New user registration page|`/auth/signup/`|
|**Reset password**|Password reset page for an existing user.|`/auth/reset-password/`|
|**Main**|Main page with all companies|`/`|
|**Profile**|User profile page. You can edit your personal information.|`/profile/`|
|**Projects**|Page with all projects of the company or users who have access.|`/project/`|
|**Project info**|Full project information. Description, contributors, creator, and so on.|`/project/:projectid/home/`|
|**Project chat**|Chat page for project members.|`/project/:projectid/chat/`|
|**Kanban board**|Kanban board page. You can create, edit tasks and move between columns.|`/project/:projectid/tasks/`|
|**Project calendar**|In the form of a calendar, you can see all the deadlines of tasks and upcoming events. You can access Google calendar and create meetings between project members.|`/project/:projectid/calendar/`|
|**Project members**|List page of all project participants with contact details.|`/project/:projectid/members/`|
|**Project dashboard**|The statistics page for a specific project. You can view task statistics, meeting statistics, and so on.|`/project/:projectid/dashboard/`|
