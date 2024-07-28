# recipeProSeleniumProject
 

1. Setting Up pgAdmin and Importing SQL File 

1) Install pgAdmin: 

Download and install pgAdmin from the official website: pgAdmin Download. 

Follow the installation instructions specific to your operating system. 

2) Create a New Server: 

Open pgAdmin and right-click on "Servers" in the Browser panel. 

Select "Create" > "Server...". 

Fill in the details: 

Name: Enter “recipe”. 

Connection: 

Host name/address: localhost 

Port: 5432 

Maintenance database: postgres 

Username: postgres 

Password: admin 

Click "Save". 

3) Import SQL File: 

Right-click on the newly created server and select "Create" > "Database...". 

Name the database as per your project requirements. 

Open the query tool (right-click on the database and select "Query Tool"). 

Load your SQL file by clicking on the folder icon and select the file.(recipeDataWebsite.sql) 

Click the play button (or press F5) to execute the SQL file. 

2. Download Project Files 

4) Clone the Repository: 

Open Git Bash. 

Navigate to the desired directory using the cd command. 

Clone the repository: 

bash 

Copy code 

git clone https://github.com/Bernardasko/recipe_website.git 
git pull origin main 

code .  

3. Running the Project 

5) Open Two Bash Terminals: 

First Terminal (Front-end): 

bash 

cd front 
npm i 
npm run dev 
 

Second Terminal (Back-end): 

bash 

cd back 
npm install 
npm run dev 
 

4. Configure PostgreSQL 

Open the postgres.mjs file in VSCode (located in the back-end directory). 

Ensure the password is set to “admin” If not, change it: 

const sql = postgres({ 

  host: 'localhost', // Postgres server 

  port: 5432, // Postgres server port 

  database: 'recipe', // Database name 

  username: 'postgres', // Database username 

  password: 'admin', // Database password 

}); 

 

5. Access the Front-end 

Go back to the front-end terminal where npm run dev is running. 

Click on the link provided in the terminal output to open the project in your web browser. 

 

 

 

Application Functionalities 

Main Page 

Unregistered User: 

Can view information about the page. 

Can view top-rated recipes. 

Can see the comment field but cannot comment. A prompt to register appears when attempting to comment. 

Can click the "Sign Up" button to register. 

Can click the “Login” button to login. 

Can click the “About” button to go to the home page. 

Registration Page 

Sign Up: 

The user must fill in the following fields: First Name, Last Name, Email, Password, Confirm Password. 

Field Restrictions: 

First Name: Cannot be empty, must be shorter than 100 characters. 

Last Name: Cannot be empty, must be shorter than 100 characters. 

Email: Cannot be empty, must be unique, and must have a valid format (contains an "@" and a ".", with a valid domain). 

Password: Cannot be empty, must be at least 8 characters long, contain at least one uppercase letter, one lowercase letter, one number, and one symbol. 

Confirm Password: Must match the Password field. 

If any field is incorrect error message is displayed. 

 

Login Page 

Login: 

A registered user can click the "Login" button on the homepage. 

The user has possibility to see a message: “ Don't have an account? Sign Up”. User can register from login page. 

The user must enter their registered email and password to log in. 

If any field is incorrect error message is displayed. 

Registered User Functionalities 

Logout: 

A registered user can click the "Logout" button to log out of their account. 

Profile: 

A registered user can click the "Profile" button to view their profile card. 

The profile card displays the user's first name, last name, email, and profile photo. 

There are two buttons: "Recipes" and "Add Recipe". 

Recipes: 

Clicking the "Recipes" button shows all recipes created by the user. 

Each recipe is displayed as a card with the following details: 

Name 

Cuisine 

Category 

Image 

Each recipe card has two buttons: "Edit" and "Delete". 

Edit: Allows the user to change any field of the recipe. There is a "Discard" button to cancel changes, and an "Update Recipe" button. Upon updating, a confirmation message is displayed. 

Delete: Prompts a confirmation dialog with "Delete" and "Cancel" buttons to confirm or cancel the deletion. 

Add Recipe: 

Clicking the "Add Recipe" button allows the user to add a new recipe. 

Add New Recipe Form: 

Fields: 

Title: Required 

Amount 1: Required 

Ingredient 1: Required 

Amounts and ingredients can be added or deleted. 

Steps: Required, default is Step 1, additional steps can be added or deleted. 

Category: Required, dropdown with options: Drinks, Appetizer, Main Dish, Dessert. 

Cuisine: Required, dropdown with a list of cuisines. 

Image URL: Optional 

All fields except the image URL are required to submit a recipe. 

Cuisines Page 

Cuisines: 

A registered user can click the "Cuisines" button in the navbar to view all cuisines that have recipes. 

The page displays a list of cuisines, sorted by the number of recipes. 

The user can filter recipes by category and change the number of recipes displayed (10, 20, 30). 

Clicking "View Recipe" under a cuisine navigates the user to a recipe page. 

Recipe Page: 

Displays the following details of the recipe: 

Image 

Name 

Rating 

Cuisine 

Category 

Ingredients 

Steps 

Allows the user to leave a comment and give a rating from 1 to 5 stars. 

Shows comments below the recipe, where users can press "Like" on comments. 

Users can change the number of comments displayed per page (5, 10). 

Category Page 

Categories: 

A registered user can click the "Category" button in the navbar to view all categories that have recipes created by the user. 

The page displays a list of categories. 

The user can filter recipes by cuisine and change the number of recipes displayed (10, 20, 30). 

Each recipe is displayed as a card with a default image (if not added), name, cuisine, and category. 

Clicking "View Recipe" on a recipe card navigates the user to the recipe page. 

Recipe Page: 

Displays the following details of the recipe: 

Image 

Name 

Rating 

Category 

Cuisine 

Ingredients 

Steps 

Allows the user to leave a comment and give a rating from 1 to 5 stars. 

Shows comments below the recipe, where users can press "Like" on comments. 

Users can change the number of comments displayed per page (5, 10). 

 

 

 
