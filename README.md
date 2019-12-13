# Wohtaku
lets scrape the news
News Scraper
Full Stack website that scrapes headlines from LA Times
Description
This full stack web site scrapes story headlines from the LA Times and allows for user comments to be added/removed to each story. Headlines, summary, link and comments are stored in a mongo database.

Front-End Technology
HTML, CSS, JavaScript (ES6), jQuery, Bootstrap, Handlebars

Back-End Technology
Node.js, Express.js, mongo.js, mongoose ORM, JavaScript (ES6), NPM packages (axios, cheerio,express, mongoose, morgan), Heroku, MVC
Database Model
Database model consists of stories and comment mongo collections
a comment document is tied to one story document
a story document can have 0 or more comment documents through the comment documents story document id
User Stories / Use Cases
user starts on home page

page loads showing existing stories found in database
user clicks 'Get New Stories'

latest LA Times headlines are loaded - up to 20
no duplicate stories will be saved in the database
stories are ordered by database id so newest will appear first
user clicks on Comments for a story

any existing comments appear with delete buttons
form for adding new comment appears
user clicks on Comments again or clicks on comments for a different story

comment section closes and if different story comment button clicked then its comment section opens
user adds or deletes a comment

comment is added and appears in list provided it was not blank (modal appears if it was blank)

comment is deleted and is removed from screen if delete button pressed

Added and Deleted comment activity is saved to database so revisiting page at later time will still reflect the changes

user clicks on story link

new browser tab opens with original LA Times story (if it is still available)
Psuedo Code -
routes
hmtl routes for home page via handlebars - all stories from database are retrieved
api routes for comments
add a comment
delete a comment
get all comments for a story