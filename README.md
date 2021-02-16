![GitHub License](https://img.shields.io/badge/ISC-License-informational) ![GitHub License](https://img.shields.io/badge/Node-JavaScript-informational) ![GitHub License](https://img.shields.io/badge/Passport-Authentication-informational) ![GitHub License](https://img.shields.io/badge/Sequelize-Package-informational) ![GitHub License](https://img.shields.io/badge/Express-Server-informational) ![GitHub License](https://img.shields.io/badge/MySQL2-Database-informational) ![GitHub License](https://img.shields.io/badge/BCrypt-Encryption-informational)

# Reverse-Engineering-Code

## Table of Contents

    * Description
    * Site Structure
    * Installation
    * Usage
    * Contributing
    * Questions
    * License

---

## Description

This application is starter code to configure and set up authentication to a program. It uses sequilized and passport packages to store and prompt the user for authentication.

## Site Structure

    1. Develop Directory - contains the html and Javascript files to run the authentication program

        * config directory
            - middleware directory
                * isAuthenticated.js file (JavaScript code to restrict user routes if not authenticated)
                * config.json file (database access configuration for development, test, and production instances)
                * passport.js file (JavaScript code that prompts the user for authentication and provides error checking
                                    comparing email and password to the database)
        * models directory
                * index.js file (JavaScript code to envokes sequelize to compare user input with database)
                * user.js file (JavaScript code to envokes bcrypt to encrypt both the email and password in the database
                                comparing hash saved hash password with user input passord)
        * public directory
            - js directory
                * login.js file (JavaScript code that gets input from the html forms from the webpage, performs
                                  validation check, and posts via API to members page)
                * members.js file (JavaScript code that use the get API to understand which user is logged in)
                * signup.js file (JavaScript code that references the input forms and when the button is clicked to
                                    submit both email and password, performs validation checks and use a post to
                                    add user to members page with error handling alert message)
            - stylesheet directory
                * style.css file (CSS code to add form signup and login to the webpage)
            - login.html file (HTML code to display login the form webpage)
            - members.html file (HTML code to display the members webpage after successful login)
            - signup.html file (HTML code for the inital login page for authentication)
        * routes directory
            - api-routes.js (JavaScript code to require models and passport packages to route via post and get functions
                              to and from login and signup webpages)
            - html-routes.js (JavaScript code that sets the paths to validate if the user is logged in using get API's
                               to the singup, login, and members webpages)
        * package.json file (Node configuration file list program details, scripts, license, and dependencies packages)
        * server.js file (JavaScript code that envokes and establishes the express service session connection and
                           diplays the webpages via html-routes.js and api-routes.js files)

---

## Installation

    1. Create this repostiory by using the GitHub forking process onto your computer
    2. Install NPM the Node Project Manager to your program directory
    3. Install dependecies to your program directory (npm install "package name"):
        - Node
        - BCrypt
        - Express
        - Express-session
        - MySQL2
        - Passport
        - Passport-local
        - Sequelize
    4. Test script run "test" in terminal
    5. Watch server run "watch" to enable nodemon server.js for testing
    6. Start server run "start" to envoke node server.js in terminal

---

## Usage

This program is designed validate email and password authentication via the Node Passport package.

Start the program with the following command "npm start".

---

## Contributing

GitHub Username - lucpizz

Please list your name here if you are contributing to this project.

---

## Questions

Please contact me at lucpizz@gmail.com for any questions regarding this program.

---

## Snapshot of Program

![Snapshot of Command line Program](./Images/Employee-Tracker-App.png)

---

## License

ISC License

Copyright (c) 4-digit year, lucpizz

Permission to use, copy, modify, and/or distribute this software for any purpose with or without fee is hereby granted, provided that the above copyright notice and this permission notice appear in all copies.

THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.

Source: http://opensource.org/licenses/ISC
