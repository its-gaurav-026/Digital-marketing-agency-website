
Digital Marketing Website Project - ReadMe

Project Overview:
This project is a digital marketing website designed to showcase various marketing services, client reviews, and provide customers the ability to request quotations, contact the team, or sign up and log in to the system. The project is built with HTML, CSS, JavaScript, Python, and MySQL for the database.

Table of Contents:
1. Project Introduction
2. Prerequisites
3. Installation and Setup
4. Project Structure
5. Database Configuration
6. Running the Project
7. Features and Functionality
8. Troubleshooting and FAQs

1. Project Introduction:
This website is developed to offer digital marketing services for businesses to enhance their online presence. It includes separate pages for showcasing services, project highlights, client reviews, and more. The website also provides functionality for users to sign up, log in, and request quotations.

2. Prerequisites:
Before you begin, ensure you have the following installed on your machine:
- Python (3.6 or above)
- MySQL (for database management)
- Flask (Python web framework)
- MySQLdb (for database connection)

3. Installation and Setup:
1. Clone or download the project repository from GitHub.
2. Open the project folder in Visual Studio Code (VS Code) or any preferred code editor.
3. Install the necessary Python packages:
    pip install flask mysqlclient
4. Set up the MySQL database using the provided database schema.
5. Edit the configuration file with your database credentials (in app.py):
    MYSQL_HOST = 'localhost'
    MYSQL_USER = 'root'
    MYSQL_PASSWORD = 'your_password'
    MYSQL_DB = 'digital_marketing'

4. Project Structure:
- index.html: Main page of the website with navigation to other sections.
- login.html: Contains both the login and signup forms for user authentication.
- services.html: Displays a list of digital marketing services.
- project_highlights.html: Contains details of previous successful projects.
- contact.html: A form for users to get in touch with the team.
- app.py: Backend logic for handling requests, managing database, and more.
- static/: Contains all CSS and JS files.
- templates/: Contains all HTML templates.

5. Database Configuration:
You will need to create the MySQL database and tables as per the project requirement. Run the following SQL commands in MySQL to set up your tables:

CREATE DATABASE digital_marketing;
USE digital_marketing;

CREATE TABLE login (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    password VARCHAR(100) NOT NULL
);

CREATE TABLE signup (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL,
    password VARCHAR(100) NOT NULL
);

6. Running the Project:
1. After setting up the project, run the Flask application using the command:
    python app.py
2. Access the website on http://localhost:5000 in your browser.

7. Features and Functionality:
- User Authentication: Users can sign up and log in.
- Quotation Form: Users can request a quote for digital marketing services.
- Service Pages: Detailed pages describing the available services.
- Project Highlights: Displays previous work and success stories.
- Contact Us: Allows users to contact the team.

8. Troubleshooting and FAQs:
- Issue: Unable to connect to the database.
    Solution: Ensure the MySQL server is running and the database credentials are correctly configured in app.py.

- Issue: CSS is not loading correctly.
    Solution: Check the file paths in the HTML templates for CSS and ensure that the static/ folder is properly set up.
