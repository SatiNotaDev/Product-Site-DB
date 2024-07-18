Project Description
This project is a PHP-based web application designed to manage and display product information. The application uses a combination of different adapters to handle data persistence and retrieval, supporting both database and JSON file storage methods. The structure of the application follows the Model-View-Controller (MVC) pattern to separate concerns and improve maintainability.

Project Structure
/project-root
│
├── /controllers
│   ├── DefaultController.php
│   ├── ProductController.php
│
├── /models
│   ├── Product.php
│
├── /repositories
│   ├── ProductRepository.php
│
├── /adapters
│   ├── DatabaseAdapter.php
│   ├── JsonFileAdapter.php
│   ├── PersistenceAdapter.php
│
├── /views
│   ├── index.html.twig
│
├── index.php
│
└── README.md


Detailed Description
1. Controllers:
DefaultController.php: Handles general application requests and directs them to the appropriate views.
ProductController.php: Manages product-related operations such as listing products, displaying product details, and updating product information.
2. Models:
Product.php: Represents the Product entity with attributes like ID, name, description, price, etc. It includes methods to manipulate product data.
3. Repositories:
ProductRepository.php: Acts as an intermediary between the data source and the application. It uses adapters to fetch and persist product data.
4. Adapters:
DatabaseAdapter.php: Provides methods to interact with a database for storing and retrieving product data.
JsonFileAdapter.php: Allows the application to read from and write to JSON files for product data persistence.
PersistenceAdapter.php: An abstract layer that defines the common interface for data persistence operations, implemented by DatabaseAdapter and JsonFileAdapter.
5. Views:
index.html.twig: A Twig template file used for rendering the product list and details in a web page.
6. Entry Point:
index.php: The main entry point of the application, routing requests to the appropriate controllers.


Usage Instructions
Setup:

Ensure you have PHP installed on your system.
Configure your web server to serve the project directory.
Set up the database if using DatabaseAdapter.php and update the configuration accordingly.
Running the Application:

Access the application through the web server (e.g., http://localhost/your-project).
Configuration:
- Modify DatabaseAdapter.php and JsonFileAdapter.php to set the correct paths and database connection parameters.
Extending the Application:
To add new features, create additional controllers, models, repositories, and views as needed.
Implement additional adapters if other data persistence methods are required.

Tools and Technologies.
 - PHP: The core programming language used to develop the application.
 - Twig: A templating engine for rendering views.
 - MVC Pattern: Architectural pattern used to separate application logic, data, and presentation.
 - Database: (Optional) For storing product data using DatabaseAdapter.php.
 - JSON Files: For storing product data using JsonFileAdapter.php.

Contribution Guidelines.
* Code Style: Follow PSR-12 coding standards for PHP.
* Branching Model: Use the Gitflow workflow for managing branches.
* Pull Requests: Submit pull requests for any new features or bug fixes. Ensure all tests pass before submission.
* Issue Tracking: Use the project's issue tracker to report bugs and request features.
License.
This project is licensed under the MIT License.
