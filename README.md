# Student records manager

## Overview

This project is a **Java Swing** application for managing student data in an educational institution. It provides a user-friendly graphical user interface (GUI) to perform CRUD (Create, Read, Update, Delete) operations on a MySQL database containing student records.

The system helps automate manual record-keeping and provides a centralized platform to quickly access and manipulate student information.

---

## Features

- Add new student records
- Display all student records in a table
- Sort student records by first name, last name, or major
- Search student records by Student ID, last name, or major
- Modify existing student records

---

## Technologies Used

- Java (JDK 8 or above)
- Swing (Java GUI toolkit)
- JDBC (Java Database Connectivity)
- MySQL database
- IntelliJ IDEA (IDE recommended)

---

## Project Structure

- `AppGUI.java`: Main GUI class with buttons and fields to interact with the student database
- `Table.java`: Utility class to convert SQL `ResultSet` into a table model for display
- `dbConnect.java`: Manages connection to the MySQL database
- `Main.java`: Entry point of the application that launches the GUI

---

## Prerequisites

- Java Development Kit (JDK) installed
- MySQL installed and running
- MySQL Connector/J JDBC driver (add this JAR to your project dependencies)
- IntelliJ IDEA or any Java IDE

---

## Database Setup

1. Log into MySQL shell:

    ```bash
    mysql -u root -p
    ```

2. Create database and table:

    ```sql
    CREATE DATABASE studentdata;
    USE studentdata;

    CREATE TABLE students (
      Student_ID VARCHAR(10) PRIMARY KEY,
      first_name VARCHAR(50),
      last_name VARCHAR(50),
      major VARCHAR(50),
      Phone VARCHAR(15),
      GPA DECIMAL(3,1),
      DOB DATE
    );
    ```

3. Insert sample data:

    ```sql
    INSERT INTO students (Student_ID, first_name, last_name, major, Phone, GPA, DOB)
    VALUES 
      ('001', 'Sankar', 'Nagarapu', 'EEE', '9398555299', 7.0, '2002-06-24'),
      ('002', 'Dharani', 'Nagarapu', 'CSE', '9133401412', 9.0, '2004-06-05'),
      ('003', 'Sindhu', 'Makarapu', 'CSE', '9133505025', 10.0, '2004-06-25'),
      ('004', 'Sneha', 'kurma', 'CSE', '9548625756', 10.0, '2004-06-27'),
      ('005', 'meghana', NULL, 'CSE', '9548651652', 10.0, '2004-05-22');
    ```

---

## Running the Application

1. Clone the repository:

    ```bash
    git clone <repository_url>
    cd <repository_folder>
    ```

2. Add MySQL Connector/J JAR file to your project dependencies in your IDE.

3. Update the database credentials in `dbConnect.java`:

    ```java
    String user = "root";
    String pass = "<your_mysql_password>";
    ```

4. Run the `Main.java` file to launch the application.

---

## Usage

- **Add**: Enter student details and click the **Add** button to save a new student record.
- **Display**: View all student records in a table format.
- **Sort**: Choose a field to sort the records.
- **Search**: Search for students by Student ID, last name, or major.
- **Modify**: Modify specific fields of an existing student's record by entering their Student ID.

---

## Future Enhancements

- Add functionality for fee tracking
- Include attendance management
- Implement user authentication
- Improve UI layout and design
- Add export/import options (CSV, Excel)

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## Contact

For any queries or suggestions, feel free to contact:

**Your Name**  
Email: your.email@example.com

---

*Thank you for using the Student Database GUI Application!*
