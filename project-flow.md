# Admin and User Flow

## User Flow
### Front End
1. **Landing Page (index.html)**:
    - User visits the landing page.
    - User can navigate to different sections like Shop, About Us, Services, Blog, and Contact Us.

2. **User Registration and Login**:
    - User registers by providing email, password, and other required details.
    - User logs in using their email and password.
    - User can choose to log in as a regular user or as a seller (admin).

3. **Browsing Books (shop.html)**:
    - User can browse available books.
    - User can search for books by title, author, or genre.
    - User can view book details in an overlay with information such as title, author, genre, summary, and ISBN.

4. **Shopping Cart**:
    - User adds books to the shopping cart.
    - User can view the shopping cart (cart.html) and update quantities or remove items.
    - User proceeds to checkout.

5. **Checkout (checkout.html)**:
    - User provides shipping details and payment information.
    - User reviews the order and places it.
    - User is redirected to the Thank You page (thankyou.html) after successful order placement.

6. **User Profile and Order Management (profile.html)**:
    - User can view and update their profile details.
    - User can view their order history and track current orders.
    - User can cancel pending orders.

## Detailed User Flow Diagram

```plaintext
Start
  |
  v
Landing Page (index.html)
  |
  v
Register/Login
  |---(Register as New User)--> Registration Form --> Submit --> Profile Page
  |---(Login as Existing User)--> Profile Page
  |
  v
Browse Books (shop.html)
  |---(Search Books)--> Search Results
  |---(View Book Details)--> Book Details Overlay
  |
  v
Add to Cart
  |
  v
View Cart (cart.html)
  |---(Update Quantities)--> Update Cart
  |---(Remove Items)--> Update Cart
  |
  v
Checkout (checkout.html)
  |---(Provide Shipping Details)--> Submit
  |---(Provide Payment Details)--> Submit
  |
  v
Order Confirmation
  |
  v
Thank You Page (thankyou.html)
  |
  v
End
```

## Admin Flow
### Front End
1. **Admin Login**:
    - Admin logs in using their credentials.

2. **Admin Dashboard (admin_dashboard.html)**:
    - Admin can view metrics like total users and total sales.
    - Admin can manage books and categories:
        - Add new books by providing details like title, author, genre, summary, ISBN, price, stock, and image.
        - Update existing book details.
        - Delete books.
        - Add and delete categories.
    - Admin can manage users:
        - View a list of registered users.
        - Delete users.

3. **Book and Category Management**:
    - Admin uses the book management section to add, update, or delete books.
    - Admin uses the category management section to add or delete categories.
    - Changes in categories reflect in the shop page for users.

4. **User Management**:
    - Admin views a list of all users.
    - Admin can delete users if necessary.

## Detailed Admin Flow Diagram

```plaintext
Start
  |
  v
Admin Login
  |
  v
Admin Dashboard (admin_dashboard.html)
  |
  v
View Metrics
  |
  v
Manage Books
  |---(Add Book)--> Add Book Form --> Submit --> Dashboard
  |---(Update Book)--> Update Book Form --> Submit --> Dashboard
  |---(Delete Book)--> Confirm Deletion --> Dashboard
  |
  v
Manage Categories
  |---(Add Category)--> Add Category Form --> Submit --> Dashboard
  |---(Delete Category)--> Confirm Deletion --> Dashboard
  |
  v
Manage Users
  |---(View Users)--> User List
  |---(Delete User)--> Confirm Deletion --> User List
  |
  v
End
``` 
## Backend Developement Plan

### Setup the Project
1. Initialize a Python project with Flask and SQLAlchemy.
2. Set up a virtual environment and install required dependencies.

### Database Design
1. Design the database schema using SQLAlchemy ORM.
2. Create models for User, Book, Order, Category, and related entities.

### User Authentication
1. Implement user registration and login using Flask-Security or Flask-Login.
2. Set up session management and user roles.

### Book Management
1. Create CRUD operations for books (Create, Read, Update, Delete).
2. Implement admin views for managing books.

### User Profile and Orders
1. Develop user profile management.
2. Implement order management and history tracking.

### Shopping Cart and Checkout
1. Implement shopping cart functionality.
2. Develop order placement and payment processing.

### Security Measures
1. Implement proper authentication and authorization.
2. Secure the application against common vulnerabilities.

### Testing and Quality Assurance
1. Write unit and integration tests for key functionalities.
2. Conduct user acceptance testing to ensure requirements are met.

### Deployment
1. Set up a deployment pipeline using Docker and CI/CD.
2. Deploy the application to a cloud provider.
