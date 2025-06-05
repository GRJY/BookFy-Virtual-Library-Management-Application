# BookFy - Virtual Library Management Application

## Overview
BookFy is a web application designed to help users manage their physical book collections digitally. It provides a user-friendly interface to organize books, track reading progress, and enhance reading habits through features like search, filtering, and reading statistics visualization. Developed as a capstone project, BookFy integrates modern web technologies and external APIs to deliver a seamless experience.

## Features
- **Book Management**: Add, edit, delete, and categorize books by genre, author, or reading status ("Read", "Reading", "To Read").
- **Search and API Integration**: Search for books using the OpenLibrary API to fetch book details automatically.
- **User Profiles**: Create and manage user profiles with personalized book collections, reading notes, and statistics.
- **Dynamic Visualizations**: Display reading statistics using Chart.js and showcase book collections with OWL Carousel.
- **Social Features**: View other users' profiles and share book collections (optional feature).
- **Security**: Secure user authentication with SESSION and COOKIE-based mechanisms and password hashing.

## Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript, jQuery, Tailwind CSS, Bootstrap, OWL Carousel, Chart.js
- **Backend**: PHP, MySQL, AJAX
- **API**: OpenLibrary API
- **Other Tools**: .htaccess (URL rewriting), Visual Studio Code
- **Development Environment**: Local server (e.g., XAMPP), Windows/Linux

## Installation
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/bookfy.git
   cd bookfy
   ```
2. **Set Up a Local Server**:
   - Install [XAMPP](https://www.apachefriends.org/) or a similar server stack (Apache, MySQL, PHP).
   - Place the project folder in the `htdocs` directory of XAMPP (e.g., `C:\xampp\htdocs\bookfy`).
3. **Configure the Database**:
   - Create a MySQL database (e.g., `bookfy_db`) using phpMyAdmin.
   - Import the provided `database.sql` file from the `db/` folder to set up the schema.
   - Update the database connection settings in `config/db.php` with your MySQL credentials:
     ```php
     define('DB_HOST', 'localhost');
     define('DB_USER', 'root');
     define('DB_PASS', '');
     define('DB_NAME', 'bookfy_db');
     ```
4. **Start the Server**:
   - Launch XAMPP, start Apache and MySQL modules.
   - Access the application via `http://localhost/bookfy` in your browser.

## Usage
1. **Register/Login**: Create a new account or log in to access your virtual library.
2. **Manage Books**:
   - Add books manually or search via the OpenLibrary API.
   - Update reading status, add notes, or upload book cover images.
3. **Explore Features**:
   - Filter books by genre, author, or status.
   - View reading statistics in charts.
   - Explore other users' public profiles (if enabled).
4. **Admin Panel** (if applicable): Manage users and system settings via the admin dashboard.

## Project Structure
```
bookfy/
├── assets/                  # CSS, JS, images, and other static files
├── config/                  # Database and application configurations
├── db/                      # SQL file for database schema
├── includes/                # PHP includes for header, footer, etc.
├── pages/                   # PHP pages for different functionalities
├── index.php                # Main entry point
├── .htaccess                # URL rewriting rules
└── README.md                # Project documentation
```

## Results
- Successfully developed a responsive web application with a user-friendly interface.
- Integrated OpenLibrary API for efficient book data retrieval.
- Achieved secure user authentication and session management.
- Conducted functional and usability tests to ensure a robust user experience.

## Future Improvements
- Develop a mobile application using React Native for broader accessibility.
- Implement machine learning-based book recommendations.
- Enhance social features with book reviews and community forums.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- OpenLibrary API for book data.
- Inspired by platforms like Goodreads and LibraryThing.