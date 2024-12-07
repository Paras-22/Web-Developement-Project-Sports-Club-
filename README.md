# Sports Club Web Application

## Overview

The **Sports Club Management System** is a web-based application designed to streamline the organization and management of sports activities within a university. This platform aims to provide a user-friendly interface for students, administrators, and club leaders to facilitate event registration, member management, and activity tracking. It was developed specifically for **Auckland International College (AIC)** and **Foundation International College (FIC)** by **Paras**. 

 **Note** - This web application is still under development and requires significant improvements in terms of functionality, design, and user experience.

---

## Features

### User-Focused Features:
1. **User Registration & Login**  
   - Allows students to create accounts and access their personalized dashboards.
2. **Sports Event Browsing**  
   - Enables students to view detailed information about upcoming sports events and recreational activities.
3. **Interest Form Submission**  
   - Students can fill out interest forms to receive additional details about specific activities and events.
4. **Event Participation**  
   - Provides the functionality for students to register for events and receive confirmation emails.

### Admin-Focused Features:
1. **Member and Event Management**  
   - Club administrators can view registered participants, manage activity interest forms, and update event details.
2. **Dynamic Content Management**  
   - Create and update event pages dynamically.

### General Features:
- **Responsive Design**  
   - Accessible on both desktop and mobile devices using **Bootstrap**.
- **Media Gallery**  
   - Showcases images and media content for past and upcoming events.
- **Social Sharing**  
   - Students can share events on their social media profiles.

---

## Use Cases

### Students:
1. Register for the platform and log in.
2. Browse events and activities.
3. Sign up for sports activities or events.
4. Submit interest forms and view confirmation.

### Club Administrators:
1. Manage student sign-ups and interest forms.
2. Update event details and notify participants.
3. View and organize participant lists.

---

## Technologies Used

- **Frontend**:
  - **HTML**: For structuring web pages.
  - **CSS & Bootstrap**: For responsive and visually appealing designs.
  - **JavaScript**: For interactivity and dynamic behavior.
- **Backend**:
  - **Node.js**: For building the server-side application.
  - **Express.js**: For handling routing and HTTP requests.
  - **EJS**: For server-side rendering of dynamic content.
  - **bcrypt**: For secure password hashing.
- **Database**:
  - A database system to store user credentials, event details, and participant information.

---

### Usage Instructions

#### Step 1: Install Required Software
1. Download and install [Node.js](https://nodejs.org/).
2. Download and install [XAMPP](https://www.apachefriends.org/index.html).
3.  Download and install [Visual Studio Code](https://code.visualstudio.com/), which will be used to open and edit the project files.

#### Step 2: Extract the Zip Folder
1. Unzip the provided folder.
2. Inside, you’ll find:
   - **WW Project Folder**: The source code for the web application.
   - **Database Export**: Contains the SQL file (`sports_club.sql`) to set up the database.

#### Step 3: Set Up the Database

##### Option A: Import the Database via phpMyAdmin
1. Launch the **XAMPP Control Panel** and start the **Apache** and **MySQL** services.
2. Open **phpMyAdmin** in your browser at:

3. Create a new database:
- Click **New** on the left-hand menu.
- Enter a name (e.g., `sports_club`) and click **Create**.
4. Import the database:
- Select the database you created.
- Click the **Import** tab.
- Select the provided SQL file (`sports_club.sql`) and click **Go**.

##### Option B: Manually Create the Database
1. Follow steps 1-3 in Option A to create a new database.
2. Navigate to the **SQL** tab in **phpMyAdmin**.
3. Open the provided SQL file, copy its contents, and paste them into the SQL editor.
4. Click **Go** to execute the SQL commands and create the database structure.

#### Step 4: Configure the Application
1. Open the **WW Project Folder** in your code editor.
2. Locate the `app.js` file.
3. Update the database connection settings as follows:
```javascript
const mysql = require('mysql');
const connection = mysql.createConnection({
    host: 'localhost',      // Database host
    user: 'root',           // Your MySQL username (default: root for XAMPP)
    password: '',           // Leave blank if no password is set
    database: 'sports_club' // The database name you created
});



