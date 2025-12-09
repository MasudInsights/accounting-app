# accounting-app
This project is a browser-based mini accounting SaaS application that provides essential business management tools such as inventory control, invoice creation, customer order management, and income–expense tracking, all in one interface. It is built with HTML, CSS, JavaScript, and uses Chart.js and XLSX.js for charts and Excel exporting.
🧩 1. Overall Structure

The app has 5 main modules accessible through a navigation bar:

Dashboard

Inventory

Invoice Management

Income & Expense Tracking

Customer Orders

Sections dynamically show/hide using JavaScript tab switching.

🟦 2. Dashboard Module
Purpose

Provides a visual financial summary of the business.

Core Features

Displays a bar chart showing:

Total Income

Total Expense

Chart is automatically updated when user:

Adds income

Adds expense

Navigates back to Dashboard

Technical

Uses Chart.js

Calculates totals from incomeData[] & expenseData[].

🟩 3. Inventory Management Module
Purpose

Allows users to record and monitor product inventory.

Features

Add Product:

Product Name

Price

Quantity

Live table showing all products

Export Inventory to Excel (inventory.xlsx)

Data Structure
inventory = [{name, price, qty}]

Why it's useful

This works like a basic stock ledger for small businesses.

🧾 4. Invoice Module
Purpose

Create invoices based on selected products from inventory.

Key Functions

Enter customer name

Add invoice items dynamically:

Select product from inventory dropdown

Enter quantity

Auto-calculates:

Unit price (from inventory)

Item total

Invoice total

Shows invoice preview in HTML

Export invoice to Excel (invoice.xlsx)

Logic

Pulls product data directly from the inventory array

Automatically builds invoice items:

invoiceItems = [{product, qty, price, total}]

🟧 5. Income & Expense Module
Purpose

Tracks business financial activities.

Features
✔ Add Income

Description

Amount

✔ Add Expense

Description

Amount

✔ Tables display:

All income entries

All expense entries

✔ Export button:

Creates income_expense.xlsx with two sheets:

Income

Expense

Live Chart Update

Adding income or expenses automatically refreshes the dashboard chart.

🟨 6. Customer Orders Module
Purpose

Keeps record of customer product orders.

Features

Enter customer name

Choose product from inventory

Enter quantity ordered

Table shows customer order list

Export to Excel (customer_orders.xlsx)

Data stored as:
customerOrders = [{customer, product, qty}]

🔧 7. Technical Architecture Overview
Front-End Technologies Used

HTML — Structure

CSS — Styling and responsiveness

JavaScript — Logic and interactivity

3rd Party Libraries

Chart.js

For bar chart visualization on dashboard

XLSX.js

Exports inventory, invoices, orders, income & expenses to Excel

Data Handling

Uses JavaScript arrays as temporary in-memory databases

No backend or database is currently connected

Tab Navigation

Uses querySelector and simple DOM manipulation to switch screens

🎨 8. UI/UX Design
What your UI includes:

Clean professional appearance

Mobile-friendly responsive design

Green theme for accounting/finance

Easy navigation bar

Tables for clarity and structure

Forms are simple and intuitive

Consistent button design (“Save”, “Export”, etc.)

📦 9. Real-World Use Cases

Your SaaS accountant app can be used by:

Small shops

Freelancers

Startups

Service providers

Home businesses

They can manage:

Stock

Sales

Invoice generation

Cash inflow/outflow

Customer tracking
