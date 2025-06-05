# BookFy - Virtual Library Management Application

## Overview
BookFy is a web application crafted to empower book enthusiasts to manage their physical book collections digitally. Developed as a capstone project at Beykent University, BookFy provides an intuitive platform for organizing books, tracking reading progress, and fostering community engagement through social features. With seamless integration of the OpenLibrary API, dynamic reading statistics, and a responsive design, BookFy enhances the reading experience for users worldwide.

## Features
- **Book Management**: Create custom libraries, add/edit/delete books, and categorize them by genre, author, or reading status ("Read", "Reading", "To Read").
- **OpenLibrary API Integration**: Search and import book details (titles, authors, cover images) directly from the OpenLibrary API for efficient book management.
- **User Profiles**: Personalize profiles with book collections, reading notes, profile pictures, and biographies; manage libraries and settings effortlessly.
- **Reading Statistics**: Visualize reading habits with interactive bar charts powered by Chart.js, showcasing genre distribution and progress.
- **Social Interaction**: Follow other users' libraries, share collections, and discover new books through community-driven features.
- **Responsive Design**: Enjoy a seamless experience on desktop and mobile devices with a modern, user-friendly interface built using Tailwind CSS and Bootstrap.
- **Secure Authentication**: Log in securely with SESSION and COOKIE-based verification, enhanced by password hashing for robust session management.
- **Dynamic Interactions**: Leverage AJAX for real-time updates, such as library searches and book additions, ensuring a smooth user experience.

## Technologies Used
- **Frontend**: HTML5, CSS3, JavaScript, jQuery, Tailwind CSS, Bootstrap, OWL Carousel, Chart.js
- **Backend**: PHP, MySQL, AJAX
- **API**: OpenLibrary API
- **Tools**: .htaccess (URL rewriting), ijaboCropTool (image cropping), XAMPP (local server)
- **Development Environment**: Visual Studio Code, Windows/Linux

## Live Demo
Explore BookFy's features at [https://bookfy.com.tr](https://bookfy.com.tr), including:
- **Home Page**: Discover trending books via a dynamic carousel and view personalized reading statistics.
- **Library Details**: Browse books in a library with details like genre, page count, and cover images from OpenLibrary.
- **Profile Page**: Manage libraries, update profile details, and connect with other readers.

*Note*: For a demo account or guided tour, contact me at akbulutgiray@gmail.com.

| Home Page | Library Details | Profile Page | Search Results |
|-----------|-----------------|--------------|----------------|
| ![Home Page](home.png) | ![Library Details](librarydetail.png) | ![Profile Page](profile.png) | ![Search Results](search.png) |


## Code Sample
Below is an example of the reading statistics visualization implemented in the home page using Chart.js, demonstrating dynamic data integration with PHP:

```javascript
const ctx = document.getElementById('libraryStatistics');
new Chart(ctx, {
    type: 'bar',
    data: {
        labels: <?php echo json_encode($labels); ?>,
        datasets: [{
            label: 'Okuma istatistiklerin',
            data: <?php echo json_encode($data); ?>,
            backgroundColor: '#2f8ffd'
        }]
    }
});
```

This snippet highlights the use of Chart.js for visualizing user reading habits, with data dynamically fetched from the backend.


**Local Setup (if source code is provided):**
1. **Clone the Repository** (contact for access):
   ```bash
   git clone https://github.com/your-username/bookfy.git
   cd bookfy
   ```
2. **Set Up a Local Server**:
   - Install [XAMPP](https://www.apachefriends.org/) with Apache, MySQL, and PHP.
   - Place the project folder in `htdocs` (e.g., `C:\xampp\htdocs\bookfy`).
3. **Configure Database**:
   - Create a MySQL database named `bookfy_db` using phpMyAdmin.
   - Import the schema (contact for `db/bookfy_db.sql`).
   - Update `config/vt.php` with your credentials:
     ```php
     <?php
     $servername = "localhost";
     $username = "root";
     $password = "";
     $dbname = "bookfy_db";
     $baglanti = new PDO("mysql:host=$servername;dbname=$dbname", $username, $password);
     ?>
     ```
4. **Start the Server**:
   - Launch XAMPP, start Apache and MySQL.
   - Access at `http://localhost/bookfy`.

## Usage
1. **Register/Login**: Sign up or log in at [https://bookfy.com.tr](https://bookfy.com.tr) to access your dashboard.
2. **Create Libraries**: Add new libraries and populate them with books via manual entry or OpenLibrary API search.
3. **Track Reading**: Monitor progress with interactive charts on the home page.
4. **Engage Socially**: Follow other users’ libraries, share collections, and explore new books.
5. **Manage Profile**: Update your profile picture, biography, and library preferences.

## Project Structure
The project follows a modular structure:
- `assets/` - CSS, JavaScript, images, and external libraries (e.g., OWL Carousel, Chart.js).
- `config/` - Database and application configurations (e.g., `vt.php`).
- `db/` - Database schema (e.g., `bookfy_db.sql`).
- `query/` - Backend query scripts (e.g., `istatistik.php`, `croppie.php`).
- `scripts/` - Custom JavaScript (`custom.js`).
- Key Pages:
  - `home.php` - Carousel and reading statistics.
  - `librarydetail.php` - Library management and book details.
  - `profile.php` - User profile and library administration.
- `.htaccess` - URL rewriting for clean URLs.


## Results
- Delivered a responsive web application with dynamic features and a modern UI.
- Integrated OpenLibrary API for efficient book data retrieval.
- Implemented secure authentication and real-time interactions via AJAX.
- Conducted functional and usability tests to ensure a seamless user experience.

## Future Improvements
- Develop a mobile app using React Native for iOS and Android.
- Implement machine learning for personalized book recommendations.
- Enhance social features with book reviews, ratings, and discussion forums.

## Important Notice
This repository is for portfolio purposes only and does not contain the full source code. To explore the application, visit [https://bookfy.com.tr](https://bookfy.com.tr). For source code access or inquiries, contact me at akbulutgiray@gmail.com. Please do not attempt to reproduce or distribute without permission.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
- [Open Library API](https://openlibrary.org/developers) for book data.
- Inspired by platforms like Goodreads and LibraryThing.
- Developed as a capstone project at Beykent University, Istanbul, Turkey.

## Contact
For questions, feedback, or collaboration opportunities, reach out to me at:
- **Email**: akbulutgiray@gmail.com
- **LinkedIn**: [Giray Akbulut]([https://www.linkedin.com/in/giray-akbulut](https://www.linkedin.com/in/giray-akbulut-33a695219/))
- **Portfolio**: [https://bookfy.com.tr](https://bookfy.com.tr)
