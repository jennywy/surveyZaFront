## SurveyZa Front End ReadMe

BACKEND REPO: https://github.com/HashTagTeamRamRod/surveyZa-Express
BACKEND DEPLOYED: http://salty-oasis-73744.herokuapp.com/surveys
FRONT END REPO: https://github.com/HashTagTeamRamRod/surveyZaFront
FRONT END DEPLOYED: https://hashtagteamramrod.github.io/surveyZaFront/

### Team Members:
Chris Guido
Melissa Luna
Jenny Yee
(w/mad props to A-aron, Charlotte Casner, Matt Collins)

### TECHNOLOGIES USED
Javascript
jQuery
Handlebars

### DESCRIPTION
SurveyZa is a web app with authentication that allows users to create, edit and vote on surveys. All users can vote and view the results of surveys, regardless of ownership. Front-end was created using HTML, JavaScript and Handlebars. The back-end was created using MongoDB, Mongoose and Express.

### USER STORIES
As an unregistered user, I would like to be able to sign up with an email, password, and password confirmation, so that I can sign in.
As a registered user, I would like to be able to sign in with an email and password, so that I can create a survey
As a survey author I want to create a survey with a question and two option answers so I can make decisions
As a survey respondent I want to see the results of the surveys I take so I can see what other people think
As a survey author I want to be able to edit my survey if I made a mistake so I can fix it
As a survey author I want to see the results of my survey so I can review what other people think
As a user I want to sign in/up with email, password etc so I can use the site
As a user I want to be able to delete my own survey so I can get rid of surveys I don't care about

### WIREFRAME

((https://imgur.com/LAxpkvt))

### ERD
((https://imgur.com/5ngDZyS))

### ROADBLOCKS
- Creating a survey
When we were creating the survey we were trying to pass through the entire survey with questions and answers on our form. We weren't able to access our responses even though they looked like they were being passed through correctly and we'd done it succesfully before with our cURL script. We weren't sure why this wasn't possbile until Chris remembered that we'd structured our model and our cURL script to create the survey question first, and then PATCH the survey answers after. We then encounted another problem where we had a 500 Internal Server Error when we tried to PATCH the answers after creating the survey. With the help of A-aron we found out that this was a problem with our back end Survey Controller console.logging undefined variables that we didn't need. Once we removed those console.logs we solved our PATCH and could completely create a survey.

- handlebars
 Using Handlebars on our nested models and using the right jQuery Selectors was really difficult. We found out that we had to run each on each item in the survey object and created partials and separate handlebars templates. We then had to refactor it to appear on the same handlebars page when we couldn't access them for our patch.
