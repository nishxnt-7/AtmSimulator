# ATM Simulator

A desktop-based **ATM Simulator / Bank Management System** developed using Java.

This project simulates the basic operations performed through an ATM. 
Users can create a new bank account, log in using their card number and PIN, 
and perform different banking transactions such as cash withdrawal, deposit, 
balance enquiry, fast cash, PIN change, and viewing a mini statement.

---

## Project Overview

The ATM Simulator provides a graphical user interface through which customers 
can interact with the banking system.

The application starts with a login screen where an existing customer can 
sign in using their **Card Number** and **PIN**, or create a new account 
through the **Sign Up** option.

After successful authentication, the customer can access the ATM transaction 
menu and perform various banking operations.

The application uses **MySQL** to store customer and transaction information, 
with **JDBC** used to establish connectivity between the Java application 
and the database.

---

## Main Features

### Account Management

- Create a new bank account
- Support for Savings and Current accounts
- Multi-step account registration
- Store customer and account information in MySQL

### Login & Authentication

- Login using Card Number and PIN
- Validate customer credentials using the database
- Access banking operations after successful login

### ATM Operations

- Deposit money
- Cash withdrawal
- Fast Cash
- Balance enquiry
- Mini statement
- PIN change
- View transaction information
- Exit the application

---

## Technologies Used

| Technology | Purpose |
|------------|---------|
| **Java** | Core application development |
| **Java Swing** | Graphical User Interface |
| **Java AWT** | GUI components and event handling |
| **JDBC** | Database connectivity |
| **MySQL** | Data storage |
| **JCalendar** | Date selection / calendar functionality |

---

## Java Concepts Used

This project was developed to practice and implement several Java concepts, 
including:

- Object-Oriented Programming (OOP)
- Classes and Objects
- Encapsulation
- Inheritance
- Polymorphism
- Abstraction
- Exception Handling
- Methods
- Constructors
- Conditional Statements
- Loops
- JDBC
- Event Handling
- GUI Development using Swing and AWT

---

## Application Flow

```text
                    ┌─────────────────┐
                    │   ATM Simulator │
                    └────────┬────────┘
                             │
                             ▼
                    ┌─────────────────┐
                    │ Login / Sign Up │
                    └────────┬────────┘
                             │
                 ┌───────────┴───────────┐
                 │                       │
                 ▼                       ▼
           ┌───────────┐           ┌───────────┐
           │  Sign Up  │           │   Login   │
           └─────┬─────┘           └─────┬─────┘
                 │                       │
                 ▼                       ▼
        ┌─────────────────┐       ┌─────────────────┐
        │ Create Account  │       │ Verify Card/PIN│
        └────────┬────────┘       └────────┬────────┘
                 │                         │
                 └────────────┬────────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Transaction Menu  │
                    └─────────┬─────────┘
                              │
        ┌─────────────┬───────┼────────┬─────────────┐
        ▼             ▼       ▼        ▼             ▼
     Deposit      Withdraw  Balance  Fast Cash   Mini Statement
        │             │       │        │             │
        └─────────────┴───────┴────────┴─────────────┘
                              │
                              ▼
                        PIN Change
                              │
                              ▼
                            Exit
```

---

## Project Structure

```text
AtmSimulator/
│
├── AtmSimulator/
│   └── src/
│       └── com/
│           └── jsp/
│               └── atm/
│                   └── functionality/
│                       ├── BalanceEnquiry.java
│                       ├── Conn.java
│                       ├── Deposit.java
│                       ├── FastCash.java
│                       ├── Login.java
│                       ├── MiniStatement.java
│                       ├── Pin.java
│                       ├── Signup.java
│                       ├── Signup2.java
│                       ├── Signup3.java
│                       ├── Transactions.java
│                       └── Withdrawl.java
│
├── Db codes/
│   └── Database / SQL files
│
├── jcalendar-tz-1.3.3-4.jar
├── mysql-connector-java-8.0.28.jar
│
└── README.md
```


---

## Database

The application uses **MySQL** as the database.

JDBC is used to establish the connection between the Java application and 
the MySQL database.

The database contains information required for:

- Customer registration
- Account details
- Card number
- PIN
- Account type
- Balance
- Banking transactions
- Transaction history

The SQL/database scripts are provided in the `Db codes` directory.

---

## Required Software

Before running the project, make sure the following are installed:

- Java JDK
- MySQL Server
- MySQL Workbench (recommended)
- Eclipse / IntelliJ IDEA / another Java IDE

---

## How to Run

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/AtmSimulator.git
```

### 2. Set Up MySQL

Open MySQL Workbench or the MySQL command line and execute the SQL 
commands provided in the `Db codes` folder.

Create the required database and tables before running the application.

### 3. Configure Database Connection

Open:

```text
Conn.java
```

Update the MySQL connection details according to your local environment.

Example:

```java
String url = "jdbc:mysql://localhost:3306/your_database";
String username = "root";
String password = "YOUR_PASSWORD";
```

Replace the database name, username, and password with your own values.



### 4. Add Required Libraries

The project uses:

- MySQL Connector/J
- JCalendar

The required JAR files are included in this repository.

### 5. Run the Application

Run:

```text
Login.java
```

The ATM Simulator login window should appear.

---

## Application Screenshots

### Login / Sign Up Interface

<img width="1007" height="601" alt="Screenshot 2026-09-17 122839" src="https://github.com/user-attachments/assets/b143dda4-4fda-4aea-b41b-490ebcb62353" />


### Account Registration

<img width="1040" height="993" alt="image" src="https://github.com/user-attachments/assets/975ccd8d-ef8f-438d-b7a7-f8d478430fb2" />

<img width="1032" height="915" alt="image" src="https://github.com/user-attachments/assets/2ec42e09-b4f1-41a3-891b-2816b96f194e" />

<img width="1037" height="1047" alt="image" src="https://github.com/user-attachments/assets/2213f01f-8176-4851-aabc-66508239263d" />

<img width="377" height="202" alt="image" src="https://github.com/user-attachments/assets/6e534ce7-8081-4a1f-a4ac-63d9397e0b94" />


---

## Main ATM Interface

After successfully signing in with a valid Card Number and PIN, an existing
customer is taken to the ATM transaction menu.

From here, the customer can perform:

- Deposit
- Cash Withdrawal
- Fast Cash
- Mini Statement
- PIN Change
- Balance Enquiry
- Exit

<img width="1177" height="1025" alt="image" src="https://github.com/user-attachments/assets/d7a5f4e5-faba-4e21-a504-12614b2db354" />


---

## Learning Outcomes

Through this project, I gained practical experience in:

- Developing desktop applications using Java
- Building graphical interfaces using Swing and AWT
- Applying Object-Oriented Programming concepts
- Connecting Java applications with MySQL using JDBC
- Performing database operations from Java
- Handling user input and events
- Implementing basic banking transaction logic
- Organizing a Java application into multiple classes

---

## Future Improvements

Some possible improvements for future versions include:

- Improve input validation
- Implement stronger PIN/password security
- Encrypt sensitive user information
- Improve exception handling
- Add money transfer between accounts
- Add account profile management
- Add an admin panel
- Improve the graphical user interface
- Migrate the application to Spring Boot
- Create REST APIs for banking operations
- Develop a web-based frontend

---

## Disclaimer

This project is developed for **educational purposes only**.

It is a simulation of an ATM/banking system and should not be used for 
real banking or financial transactions.

---

## Author

Nishant Mudgal

GitHub: https://github.com/nishxnt-7
