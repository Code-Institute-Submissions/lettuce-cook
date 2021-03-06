# Lettuce Cook
## Data Centric Development Milestone Project - Code Institute

The purpose of this site is to provide users a database of recipes which they can add to in order to have a collection of mixed recipes. A user can search for a particular recipe, add a recipe, edit a recipe, or delete the recipe. The landing page is the full collection of recipes in the database.
 
## UX

This website is designed to feel fresh and friendly, in order to appeal to both young and old users who want to add to a collection of recipes. 

#### Strategy
For potential users, the site is aimed at being able to add to the collection of recipes, edit any recipes in the collection, delete a recipe from the collection and to search through the collection of recipes. 
All these need to appear in an easy-to-read format, and intuitive organised layout that is easy for the user to navigate through. 
The home page will provide an interactive base with all the recipes showing, with links to the other actions to the collection.

For potential site owners, the site could be monitored to gauge how popular a certain style of cuisine is by how many views or recipes are added into that category. 

For all users, the site can be used to be a community-based collection of recipes that are easily shared with other users for everyone's cooking benefits. 
Multiple recipes from multiple sources can be viewed on one site, making amalgamating recipe collections more simple.

#### Scope
Key features to include are:
- A navigation panel which is collapsible for smaller screen sizes
- The add / edit pages to add or edit a recipe to or within the collection
- The delete option to be hidden within an edit page so no accidental removals occur
- Photos to have a visual aid to which recipes might appeal best to the users
- A search function with several categories, so the user can search for a particular item

#### Structure
The page will have a standard footer and header in the colour theme chosen. 
There are several pages to show:
- Home page to show the entire collection of recipes and give options to add / view / edit / delete recipes (CRUD functionality)
- Search page which allows the user to search the catalogue of recipes and view results
- New Recipe page - used to add a recipe to the collection
- Edit Recipe page - used to edit any existing recipes in the collection
- Schema is as follows:

| Main Database | Collection    | Fields              |
|---------------|---------------|---------------------|
| lettuce_cook  | recipes       | _id:                |
|               |               | recipe_name:        |
|               |               | recipe_description: |
|               |               | cuisine_type:       |
|               |               | photo:              |
|               |               | difficulty_level:   |
|               |               | prep_time:          |
|               |               | cooking_time:       |
|               |               | serving_size:       |
|               |               | ingredients:        |
|               |               | method:             |
|               | cuisine_style | _id:                |
|               |               | cuisine_type:       |
|               | difficulty    | _id:                |
|               |               | difficulty_level:   |
|               | preparation   | _id:                |
|               |               | preparation_time:   |
|               | cooking       | _id:                |
|               |               | cooking_time:       |
 

#### Skeleton
I created an original skeleton page using Pencil software. The full version of the skeleton can be found [here](static/mockups/wireframe.pdf). 

For ease of viewing, I have attached the main mockups below:
- Mobile Home page: 
    
![Mobile home page wireframe](static/mockups/mobile_home.png)
- Mobile Add Recipe page: 
    
![Mobile add recipe wireframe](static/mockups/mobile_add.png)
- Mobile Edit Recipe page: 
    
![Mobile edit recipe wireframe](static/mockups/mobile_edit.png)
- Mobile Search Recipe page: 
    
![Mobile search recipe wireframe](static/mockups/mobile_search.png)
- Web Home page: 
    
![Web home page wireframe](static/mockups/recipe_home.png)
- Web Add Recipe page: 

![Web add recipe wireframe](static/mockups/recipe_add.png)
- Web Edit Recipe page: 

![Web edit recipe wireframe](static/mockups/recipe_edit.png)
- Web Search Recipe page: 

![Web search recipe wireframe](static/mockups/recipe_search.png)


#### Surface
The colour scheme has been chosen to be welcoming, light and refreshing with positive colours, but without being garish. 
This will hopefully attract users of all ages without being hard to read. 

## Features
The majority of my website is built upon the grid system within Bootstrap, especially using the flex functionality. 
JavaScript and JQuery additions to Bootstrap allowed me to have a smoother drop down box which was collapsible for smaller screen sizes and a user friendly contact form. 
MongoDB Atlas was used as the hosting platform for the database used.
Heroku is the deployment host.

### Existing Features
- Dropdown menu - allows users to have a minimised menu for smaller screen sizes
- Sticky menu - allows users to reach the menu at any point without scrolling to the top on smaller screen sizes
- Form - allows users to input information into the database
- Interactive buttons to maximise use of the screen

### Features Left to Implement
- User-names so only the user who added the recipe can edit / remove that particular recipe
- Ratings for each recipe
- Upload photo functionality rather than using a URL link 

## Technologies Used
- HTML 
    - The project uses **HTML5** as a base language for the webpage
- CSS 
    - The project is styled mainly using **CSS3** 
- [Bootstrap](https://getbootstrap.com/)
    - The project is structured using the **Bootstrap** grid system, implementing the flex attributes
- [JQuery](https://jquery.com)
    - The project uses **JQuery** to simplify DOM manipulation
- [JavaScript](https://www.javascript.com/)
    - The project uses **JavaScript** to make the functionality more smooth and interactive
- [Font Awesome](https://fontawesome.com/)
    - The project uses **Font Awesome** for icons within the webpage
- [MongoDB Atlas](https://www.mongodb.com/cloud/atlas)
    - The project hosts the database on **MongoDB Atlas** 
- [Heroku](https://www.heroku.com/)
    - The project is deployed from **Heroku** 

## Testing
Testing the search form:
- Attempt to submit an empty form to check an error message for the designated fields appears
- Check the functionality of the queries being sent to MongoDB
- Check that the results section show up "no results" if none are found

Testing the add functionality:
- Check that you can add to the database
- Check that the naming conventions are the same as the database or it will not show properly
- Send the correct data to the database
- Check you can receive the data from the database after adding

Checking using Validator:
- HTML validity was checked using the online validator [W3C Markup Validator](validator.w3.org)
    - Errors were thrown when the Flask references were used within the HTML
- CSS was checked uing the online validator [CSS Jigsaw Validator](http://www.css-validator.org/)
- JS was checked using the online validator [JSHint](https://jshint.com/)
    - Errors were thrown with the 'template literal syntax' used

Screen sizes:
- The website was checked for all the screen sizes available on Chrome Developer Tools
- Special attention was shown for the mobile screen size as the recipe cards are different between the different sized screens
- Attention was taken for the iPad screens as the menu and photos needed manual styling

Browser details:
- All development was done within Chrome browser
- Mozilla was checked and the same functionality was found 
- Safari was also checked, but only in mobile view

Bugs found:
- Could not populate the data into the results section within the search page, so had to create a separate search results page with link back to the search page
- Interactive buttons to add fields to the html in the search filters section did not pass the database variables to the javascript functions
- Static javascript scripts were not accessed until replaced with url_for() static link
- Dropdown would not function with mobiles, so updated version of dropdown was created which works well

Testing was done primarily as I went along manually. If the Python or JavaScript were to be more complicated to test, I would have created a stand-alone unit test for each part needing to be tested using Jasmine or another system. 

## Deployment
This project has been deployed using Heroku.

The process involved consists of:
- Adding regularly to the Git branch, committing with comments each time
- Pushing this Git branch to GitHub
- Pushing it to the Heroku branch
- Creating the necessary Procfile and requirements.txt files
- Deploying to the Heroku webpage
- Adding security to the MongoDB database, and linking any addresses and ports to the Heroku app

Pushing to Heroku from Git:
- I ensured that the Procfile and requirements.txt were saved within the repository
- Within Heroku, I created an app for the page
- All commits were finalised and pushed to the GitHub repository
- The following was entered inside the Git bash terminal:
    - $ heroku login
    - $ heroku apps
    - $ heroku git:remote -a lettuce-cook
    - $ git push heroku master
- The webpage was then deployed to Heroku

To deploy this project locally, you will need to do the following:
- Clone the GitHub repository:
    - Navigate to the repository url: https://github.com/CharOConnell/lettuce-cook 
    - Click on "Clone or Download"
    - To clone the repository using HTTPS, under "Clone with HTTPS", copy the link inside the box
    - To clone the repository using an SSH key, including a certificate issued by your organization's SSH certificate authority, click Use SSH, then copy the link inside the box
    - Open the Git Bash
    - Change the current working directory to the location where you want to clone the directory
    - Type git clone, and then paste the URL you copied before
        - $ git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY
    - Press Enter and your clone will be created
- Once any changes are made, you will need to push to the Heroku server
- Make sure that there is a Procfile and requirements.txt file within the repository
- Ensure you have created your own Heroku app to deploy to 
- To push to Heroku, you must enter the following inside the Git bash terminal:
    - $ heroku login (you will be asked to login with your username and password)
    - $ heroku apps
    - $ heroku git:remote -a app-name-of-heroku-app
    - $ git push heroku master
- Your project will the be published to Heroku

## Credits
### Content
Text was written by me within the site. 

### Media
The photos used in the file system that I created were taken from Google Images under the "Labeled for Reuse" filter. 

### Acknowledgements
All elements which I have used within this page that were inspired by, or are from exteranl sources, are linked below:
- For the base information to create the flex system, I used [this page](https://getbootstrap.com/docs/4.0/utilities/flex/) as a reference
- For the layout for the recipe cards, I used [this page](https://getbootstrap.com/docs/4.1/utilities/display/) as a reference
- The dropdown menu was styled using the Bootstrap "navbar" item, found [here](https://getbootstrap.com/docs/4.0/components/navbar/)
- For extra help with the form to only send the desired values to the database, I used information from this [forum question](https://stackoverflow.com/questions/11556958/sending-data-from-html-form-to-a-python-script-in-flask)
- For cloning a GitHub repository, the instructions were taken from [here](https://help.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository)