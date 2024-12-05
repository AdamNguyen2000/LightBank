## Screenshots
![Copy of High Level drawio](https://github.com/user-attachments/assets/c443f909-c42f-4352-8ee5-63ece496ff7c)
![2024-12-04_18h57_29](https://github.com/user-attachments/assets/10378e23-be3d-4e7c-bec7-5b70b26df470)
![2024-12-04_18h57_38](https://github.com/user-attachments/assets/f67ec562-24dc-4fad-a3d5-7256e3b15d20)

---

# LightBank Banking Program

## Description
The program includes functionalities for online banking such as user registration, login, account management, and various banking operations.

---

## Features Implemented

### 1. User Registration Flow
- **Page:** `Register User Account`
  - Input fields for:
    - **User** (Username)
    - **Pin** (4-digit code)
    - **Name** (Full Name)
  - **Submit Button:**
    - Stores user data in the database.
    - Redirects to the `Login Page` upon successful submission.
    
### 2. User Login Flow
- **Page:** `Home Page`
  - Input fields for:
    - **User** (Username)
    - **Pin** (4-digit code)
  - Buttons for:
    - **Login:** Authenticates user credentials against the database and redirects to the `Status Page` if successful.
    - **Register:** Redirects to the `Register User Account` page for new user registration.
  - Invalid credentials:
    - Returns an error message and redirects back to the `Login Page`.

### 3. Status Page
- Displays the user's current balance based on database information.
- Provides six main actions:
  1. **Open Account:** Adds a new account for the user in the database.
  2. **Close Checking Account:** Removes the user's checking account and its balance from the database.
  3. **Transfer Balance:** Moves balance from one user to another in the database.
  4. **Upload Image to Deposit Check:** Prompts for an image and updates the user's account balance based on the deposited amount.
  5. **Withdraw:** Removes balance from the user's account and simulates cash withdrawal.
  6. **Logout:** Ends the session and redirects to the `Home Page`.

### 4. Database Schema
- **Table Structure:**
  - **User:** Unique identifier for each user.
  - **Pin:** Authentication code for the user.
  - **Name:** Full name of the user.
  - **Checking:** Status indicator (1 for active, 0 for inactive).
  - **Saving:** Status indicator (1 for active, 0 for inactive).
  - **Balance 1:** Balance in the checking account.
  - **Balance 2:** Balance in the saving account.

---

## Workflow Diagram
A visual representation of the application workflow has been attached to this pull request for reference.

---

## Testing
- Unit tests have been implemented for each feature:
  - User registration and validation.
  - Login authentication and error handling.
  - Account management actions (open, close, deposit, withdraw, transfer).
- Integration tests ensure end-to-end functionality of the application workflow.

---

## How to Run
1. Clone the repository.
2. Open XAAMP and start Apache and MySQL
2. Put the project directory in to htdocs in XAMPP
3. Setup database tables in http://localhost/phpmyadmin
4. Access the web interface at http://localhost/LightBank/UI/Homepage.php

---

## Notes
- Future enhancements:
  - Add user roles and permissions.
  - Implement additional security measures for PIN validation.
  - Enhance UI/UX design.
