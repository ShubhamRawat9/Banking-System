🏦 Bank of Uttarakhand — Banking System

A front-end banking application built with HTML, CSS, and JavaScript. The project provides a simulated online banking experience where users can log in, view account activity, transfer money, request loans, close accounts, and sort transactions.

Note: This is a client-side educational/demo project. It does not connect to a real banking server or database and should not be used for real financial transactions.

✨ Features

🔐 User login using username and PIN

💰 Display current account balance

📊 Display deposits and withdrawals

📥 Calculate total incoming money

📤 Calculate total outgoing money

💵 Calculate interest

🔄 Transfer money between demo accounts

🏦 Request a loan based on account activity

❌ Close/delete an account

↕️ Sort account movements

🎨 Responsive, modern banking-style interface

⏱️ Banking dashboard layout with operations and transaction summary

🛠️ Technologies Used

Technology

Purpose

HTML5

Application structure

CSS3

Styling, layout, gradients, and UI design

JavaScript (ES6+)

Banking logic and DOM interaction

Google Fonts

Poppins typography

Live Server

Local development server

📂 Project Structure

Banking System/
│
├── index.html
├── script.js
├── style.css
├── settings.json
├── WhatsApp Image 2024-11-25 at 21.21.07_64efe984.jpg
│
└── .vscode/
    └── settings.json

Main Files

index.html

Contains the complete banking dashboard structure, including:

Login section

Account balance

Transaction/movement section

Income/outgoing/interest summary

Money transfer form

Loan request form

Account closing form

Logout timer display

style.css

Contains the application's visual design, including:

Navigation styling

Login form styling

Banking dashboard grid

Transaction cards

Deposit/withdrawal badges

Transfer, loan, and close-account operation cards

Gradients and typography

Responsive layout foundations

script.js

Contains the application's banking functionality and JavaScript logic.

The main operations include:

Login
  ↓
Find Account
  ↓
Validate PIN
  ↓
Display Dashboard
  ↓
Perform Banking Operations

👤 Demo Accounts

The application currently contains five demo accounts.

Owner

Username

PIN

Robin Sajwan

rs

1111

Rohit Negi

rn

2222

Shubham Rawat

sr

3333

Sonaxi Aswal

sa

4444

Ranjan Jajwan

rj

5555

These credentials are hard-coded in script.js and are intended only for demonstration.

💳 Banking Operations

1. Login

Enter a valid username and PIN.

For example:

Username: rs
PIN: 1111

After successful authentication, the banking dashboard becomes visible.

2. View Balance

The application calculates the current balance from all account movements.

Conceptually:

Balance = Deposits - Withdrawals

The calculation is performed using JavaScript's reduce() method.

3. Transaction History

Transactions are stored as positive and negative numbers.

Example:

movements: [200, 450, -400, 3000]

Positive values represent deposits and negative values represent withdrawals.

4. Transfer Money

A logged-in user can transfer money to another registered account.

The transfer validates:

Transfer amount must be greater than zero

Receiver must exist

Sender must have sufficient balance

Sender cannot transfer money to themselves

The sender receives a negative movement while the receiver receives a positive movement.

5. Request Loan

Users can request a loan when they meet the application's simplified eligibility condition.

The current logic checks whether at least one previous movement satisfies the required threshold.

6. Close Account

An account can be closed by confirming:

Username

PIN

The account is then removed from the in-memory accounts array and the dashboard is hidden.

7. Sort Transactions

The SORT button toggles between the original transaction order and ascending numerical order.

🧮 JavaScript Concepts Demonstrated

This project is useful for practicing modern JavaScript concepts such as:

const and let

Objects

Arrays

Array methods

map()

filter()

reduce()

find()

findIndex()

some()

sort()

Template literals

Optional chaining

DOM manipulation

Event listeners

Form handling

Conditional logic

Dynamic HTML generation

For example, usernames are generated automatically from account owner names:

Robin Sajwan → rs
Rohit Negi → rn
Shubham Rawat → sr

🚀 How to Run the Project

Option 1 — Open Directly

Open:

index.html

in a modern web browser.

Option 2 — Use VS Code Live Server

Open the project folder in Visual Studio Code.

Install the Live Server extension if it is not already installed.

Open index.html.

Right-click the file.

Select Open with Live Server.

The project is configured to use port:

5501

🖥️ Application Flow

              ┌─────────────────┐
              │    Login Page    │
              └────────┬────────┘
                       │
                 Username + PIN
                       │
                       ▼
              ┌─────────────────┐
              │ Authentication  │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │ Banking Dashboard│
              └────────┬────────┘
                       │
       ┌───────────────┼────────────────┐
       ▼               ▼                ▼
   Transfer          Loan          Close Account
       │               │                │
       └───────────────┼────────────────┘
                       ▼
              ┌─────────────────┐
              │    Updated UI   │
              └─────────────────┘

📊 Account Data Model

Each account is represented as a JavaScript object:

const account = {
  owner: "Robin Sajwan",
  movements: [200, 450, -400, 3000],
  interestRate: 1.2,
  pin: 1111
};

The application generates an additional username property from the owner's name.

🔒 Security Note

This project demonstrates front-end banking functionality only.

It is not secure enough for production banking because:

User credentials are stored directly in JavaScript.

There is no backend authentication.

There is no database.

PINs are not encrypted or hashed.

Account data exists only in browser memory.

There is no authorization system.

There is no server-side validation.

Transactions are not persisted.

For a production banking system, authentication, authorization, encryption, secure APIs, a database, transaction validation, audit logging, and other security controls would be required.

🔮 Future Improvements

Possible improvements include:

Add a backend using Node.js/Express

Add MongoDB or PostgreSQL

Implement secure authentication

Hash passwords/PINs

Add JWT/session authentication

Store transactions in a database

Add transaction timestamps

Add beneficiary management

Add account statements

Add profile management

Add responsive mobile navigation

Add transaction search/filtering

Add charts for spending and deposits

Add email/SMS notifications

Add two-factor authentication

Add an admin dashboard

Deploy the application to a cloud platform

📌 Project Purpose

This project demonstrates how JavaScript can be used to build an interactive banking dashboard while practicing:

DOM manipulation

Event-driven programming

Array operations

Object-oriented data organization

Form handling

Dynamic UI updates

Basic financial calculations

It is suitable as a frontend/JavaScript learning project and academic demonstration.
