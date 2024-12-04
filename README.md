Contacts Management UI (Frontend)
Description
This project is the frontend implementation of the Contacts Management Application. It allows users to interact with the backend API to manage their contacts, including adding, editing, deleting, and merging duplicate contacts. It also provides real-time feedback for form validation and allows users to manage contacts via a modern web interface.

Key Features
CRUD Operations UI:

Interface for creating, viewing, updating, and deleting contacts.
Interactive forms for entering contact details (First Name, Last Name, Email, Address).
Contact Merging Interface:

UI components to help users identify and merge duplicate contacts.
Displays suggestions for potential duplicate contacts based on email address.
Validation Feedback:

Provides real-time validation feedback on form fields:
Required fields (First Name, Last Name).
Valid email format.
Error messages for invalid inputs.
Responsive Design:

The application is designed to be responsive, ensuring it works well on both mobile and desktop devices.
Technologies Used
Framework: React.js (Frontend Library)
State Management: React's useState, useEffect (or Context API if necessary)
CSS Framework: Bootstrap or custom CSS for layout and styling
Validation Library: Formik or React Hook Form for form handling and validation
API Communication: Axios or Fetch API for making requests to the backend
Setup Instructions
Prerequisites
Node.js (>= 14.x)
A working backend API for contacts management (see Backend Setup).
Installation Steps
Clone the repository:

bash
Copy code
git clone https://github.com/VanapaliMukesh/Contact_Application_frontend.git
cd Contact_Application_frontend
Install dependencies:

bash
Copy code
npm install
Start the development server:

bash
Copy code
npm start
The frontend will be running on http://localhost:3000.

Environment Variables
If the application requires API endpoint configuration, add the following to your .env file:

bash
Copy code
REACT_APP_API_URL=http://localhost:5000
Folder Structure
src/components: Contains reusable components (e.g., ContactForm, ContactList).
src/pages: Contains the main pages of the application (e.g., HomePage, ContactPage).
src/utils: Utility functions (e.g., for validation, API requests).
How to Use
Contact List Page
View a list of all contacts with options to edit or delete them.
Use the Merge Contacts feature to identify and merge duplicates based on email.
Adding a Contact
Navigate to the Add Contact page.
Fill in the required fields (First Name, Last Name, Email, Address).
Submit the form to create a new contact.
Editing a Contact
Select a contact from the list.
Modify the fields as needed (First Name, Last Name, Email).
Submit the form to save changes.
Merging Contacts
The Merge Contacts feature automatically detects duplicate contacts based on email.
Select duplicate contacts to merge into one.
API Documentation
The frontend interacts with the following API endpoints for CRUD operations:

GET /contacts: Fetch all contacts.
POST /contacts: Create a new contact.
PUT /contacts/:id: Update an existing contact.
DELETE /contacts/:id: Delete a contact.
POST /merge: Merge duplicate contacts based on email.
Example API Usage
Get All Contacts:

bash
Copy code
GET http://localhost:5000/contacts
Response:

json
Copy code
[
  {
    "firstName": "John",
    "lastName": "Doe",
    "email": "john.doe@example.com",
    "address": "123 Main St"
  },
  ...
]
Create a New Contact:

bash
Copy code
POST http://localhost:5000/contacts
Body:

json
Copy code
{
  "firstName": "Jane",
  "lastName": "Doe",
  "email": "jane.doe@example.com",
  "address": "456 Elm St"
}
How to Contribute
Fork the repository.
Create a feature branch (git checkout -b feature/your-feature).
Commit your changes (git commit -am 'Add new feature').
Push to the branch (git push origin feature/your-feature).
Create a new pull request.
License
This project is licensed under the MIT License.
