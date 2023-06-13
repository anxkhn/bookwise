# BookWise

## Problem Statement :

### Library Management Web Application

A local library is in dire need of a web application to ease their work. The library management system must allow a librarian to track books and their quantity, books issued to members, book fees.

For the sake of simplicity, you don't have to implement sessions and roles, you can assume that the app will be used by the librarian only.

The following functionalities are expected from the application:

#### Base Library System

Librarians must be able to maintain:

- **Books** with stock maintained
- **Members**
- **Transactions**

The use cases included here are to:

- Perform general [CRUD](https://en.wikipedia.org/wiki/Create,_read,_update_and_delete) operations on Books and Members
- Issue a book to a member
- Issue a book return from a member
- Search for a book by name and author
- Charge a rent fee on book returns
- Make sure a member’s outstanding debt is not more than Rs.500

#### Integration for Data Import

The librarian should be able to import books into the system using the [Frappe API](https://frappe.io/api/method/frappe-library) and create book records.

**How the API works?**

- This API will give you only **20** books at a time.
- It accepts `title`, `authors`, `isbn`, `publisher` and `page` as parameters.

**How to use the API?**

- Build an interface in your app to interact with our API.
- Add a field to **specify the number of books to import**, at the very least.
- You may additionally give the librarian any set of parameters; for instance, they should be able to import 30 books titled "Harry Potter".
- Insert book records.

---
# My Submission: BookWise
## Library Management Web Application

# Interface :

## Login

- Uses sha256 hashing 

- demo credentials: admin,password

- all critiacal functions requires login session

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193319.png)

# 

## Books Dashboard

- Shows top ten recentely added books

- Search option retrieves from inventory

- Can issue books from the listing (if due is under 500)

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193348.png)



- Add books and Import books option 

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193401.png)

- Manually add the books

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193457.png)

- Importing books from Frappe API

- Used OpenLibrary API to fetch books cover

- Easy to librarian to verify and add books

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193539.png)

- All the books information will be imported, only stock information is required

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193553.png)

- User feedback upon sucessefully importing

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193617.png)

## 

## Members Dashboard

- View most recentely added members,

- Search for members based on thier ID, name or contact information

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193632.png)

- Add members

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193700.png)

- Delete Members (constrains added if book pending is due)

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193700.png)

- Edit Member Info 

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193726.png)

- View Detailed Member Info

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193739.png)



## Transactions

- View Recent transactions

- Check fees due

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193831.png)

- Detailed Calculation

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193953.png)

- Manual Searching of past transactions

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20193854.png)

- Records of past transactions

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20194016.png)



## Report

- Top performing books 

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20194033.png)

- Top paying members

![](https://raw.githubusercontent.com/anxkhn/bookwise/main/Screenshots/Screenshot%202023-06-13%20194041.png)
