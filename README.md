# 🛒 Grocery Store CheckList Application

# Project Title: Grocery Store CheckList

## Video Demo: [https://youtu.be/pNEd-YCJP9g?si=Whnadd9af-GNYsCk](https://youtu.be/pNEd-YCJP9g?si=Whnadd9af-GNYsCk)

## 📝 Description
The **Grocery Store Checklist** application is a versatile and practical web-based tool designed to streamline the grocery shopping experience. Developed using **Flask**, **SQLite**, **HTML**, **CSS**, **JavaScript**, and **Jinja**, this application blends a robust backend with an intuitive and dynamic frontend for a seamless user experience.

On each page load, the app fetches five random grocery items from a database. Users can add or remove items to customize their checklist — making it a handy and interactive utility for planning grocery runs.

---

## ⚙️ Technical Implementation

### Technologies Used
- **Backend**: Flask (Python), SQLite
- **Frontend**: HTML, CSS, JavaScript, Jinja Templates
- **Session Management**: Flask sessions

---

### Backend
The backend is powered by Flask, a lightweight web framework in Python, and SQLite, a self-contained, serverless SQL database engine.

- **Database**: The `grocery_list.db` file, created using SQLite, stores the list of grocery items.
- **Python Script**: A Python script initializes and populates the database with grocery items. Any necessary changes can be made using SQLite.
- **Flask Application**: The `app.py` file is the main part of the application, including routes, request handlers, and the logic behind the application.

### Flask Application Details
- **Imports**: Modules to interact with SQLite, shuffle items, and Flask framework.
- **App Configuration**: Initialization of the Flask application and setting a secret key for session management.
- **Routes**:
  - **Index Route (`/`)**: Handles requests to the homepage.
  - **Add Items Route (`/add_items`)**: Allows users to add items to the shopping list (POST request).
  - **Remove Items Route (`/remove_items`)**: Allows users to remove items from the shopping list (POST request).
- **Database Connection**:
  - `get_db()`: Connects the database with the application and retrieves data.
  - `@app.teardown_appcontext`: Ensures the database connection is closed when the application context ends.
- **Running the Application**:
  - `if __name__ == '__main__'`: Ensures the application runs only if the script is executed directly.

### Database Initialization Script
This Python script demonstrates how to create an SQLite database (`grocery_list.db`) and populate it with a list of groceries.
- **Import SQLite3 Module**: To interact with SQLite databases.
- **Grocery List**: Defines a list of grocery items.
- **Sorting**: Sorts the groceries list alphabetically.
- **Connecting to the Database**: Establishes a connection to the SQLite database.
- **Creating the Table and Inserting Data**: Creates a table and inserts grocery items into the database.
- **Commit and Close**: Commits the transaction and closes the database connection.

### Frontend
The frontend is implemented using HTML, CSS, and JavaScript, providing a user-friendly interface for interacting with the checklist.

- **HTML and CSS**: Define the structure and styling of the web page, ensuring it is visually appealing and easy to navigate.
- **JavaScript**:
  - **Function `check_me(input_id)`**: Enhances user interaction by dynamically updating HTML elements based on user actions, such as checking/unchecking items and updating button styles.

---

## 🌟 Key Features

- **Random Grocery Suggestions**: 5 random products on each visit.
- **Add/Remove Items**: Customizable shopping checklist.
- **Session Memory**: Retains state during browsing.
- **User-Friendly Interface**: Simple, accessible layout.
- **Database Integration**: Dynamically fetches current items.

---

## ✅ Benefits

- **Convenience**: Quick generation of a shopping list.
- **Variety**: Encourages users to consider a wider range of items.
- **Customization**: Users can edit the list based on personal preferences.
- **Efficiency**: Helps users stay organized while shopping.
- **Database Integration**: Ensures the list includes current and relevant products.
- **User-Friendly**: Simple and intuitive interface accessible to all users.

---

## 💼 Conclusion
The Grocery Store Checklist application effectively combines a powerful backend with an interactive frontend to provide a seamless and efficient grocery shopping experience. It leverages Flask and SQLite for robust data management and session handling, while HTML, CSS, and JavaScript ensure a dynamic and user-friendly interface. This project serves as a practical tool for users to manage their grocery shopping lists easily and efficiently.

This was CS50x.

---

## 🖼️ Project Wireframe

![Proj Wireframe](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjSfUyUTkzyuX4YDaYzacQaXdLiwRC5-sDDqYi3PI0f3IrNSBLGyay6jSuqhg13usZDV7No3dctGwUJJKc3SNVXAra-uGvXE5pUsQGav_H4Bb-Yxb2QhHesdeS0e81scf3tDOSET1whSg-Ac6o15RipWb8pvCHhDGH5lt3XIuOMTwUatUisjrmCxW-GtY4/s320/Screenshot%202024-07-05%20203643.png)

---

## 📁 Project Structure

```
GroceryShopping-List/
├── completeApp/
│   ├── app.py
│   ├── grocery_list.db
│   ├── grocery_list.py
│   ├── init_db.py
│   ├── requirements.txt
│   ├── static/
│   │   ├── css/
│   │   │   └── main.css & few required images
│   │   └── js/
│   │       └── main.js
│   │
│   └── templates/
│       └── index.html
│       └── assets/ (logos and images)
└── README.md
```

---

## 🧪 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/GroceryShopping-List.git
   cd GroceryShopping-List
   ```

2. **Create virtual environment (optional but recommended)**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # Windows: venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**:
   ```bash
   python app.py
   ```

> 🔐 **Note**: Replace the Flask `secret_key` with a strong random value for production use.

---

## 🚀 Future Enhancements

- User authentication for personalized lists
- Export options (PDF, CSV)
- Quantity tracking and categories
- Mobile-first responsive design using Bootstrap or Tailwind

---

## 👨🏻‍💻 Acknowledgements

- Developed as part of the [CS50x](https://cs50.harvard.edu/x/) Final Project.
- Thanks to HarvardX, CS50 team & David J. Malan for the incredible course and community!

---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
