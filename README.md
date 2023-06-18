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

![Screenshot 2023-06-13 193319](https://github.com/anxkhn/bookwise/assets/83116240/5ceca8b1-1142-400c-964f-f89213e9a836)


# 

## Books Dashboard

- Shows top ten recentely added books

- Search option retrieves from inventory

- Can issue books from the listing (if due is under 500)

  
![Screenshot 2023-06-13 193348](https://github.com/anxkhn/bookwise/assets/83116240/3ff0ab60-ce10-4469-b3bb-a07af5916151)



- Add books and Import books option 


![Screenshot 2023-06-13 193401](https://github.com/anxkhn/bookwise/assets/83116240/562dafe5-1356-4f2b-a6a1-1bb5b049d915)

- Manually add the books

![Screenshot 2023-06-13 193457](https://github.com/anxkhn/bookwise/assets/83116240/e7c91eec-ffd6-44e8-85aa-506810c7556e)


- Importing books from Frappe API

- Used OpenLibrary API to fetch books cover

- Easy to librarian to verify and add books

![Screenshot 2023-06-13 193539](https://github.com/anxkhn/bookwise/assets/83116240/d73f579b-2fad-47b2-915e-a959adbd4f38)


- All the books information will be imported, only stock information is required

![Screenshot 2023-06-13 193553](https://github.com/anxkhn/bookwise/assets/83116240/cccad77a-057d-4967-a0d5-22ad6027290f)


- User feedback upon sucessefully importing

![Screenshot 2023-06-13 193617](https://github.com/anxkhn/bookwise/assets/83116240/7508842a-4d8e-437b-8270-3e9d79e0d66d)

## 

## Members Dashboard

- View most recentely added members,

- Search for members based on thier ID, name or contact information

![Screenshot 2023-06-13 193632](https://github.com/anxkhn/bookwise/assets/83116240/6bd1d206-fff9-46d4-8ef9-3870f508c520)


- Add members

![Screenshot 2023-06-13 193700](https://github.com/anxkhn/bookwise/assets/83116240/1b745250-5c25-45f5-806e-f99b1329b189)


- Delete Members (constrains added if book pending is due)

![Screenshot 2023-06-13 193712](https://github.com/anxkhn/bookwise/assets/83116240/d5c32f6c-6257-4e78-ac1b-03f3fc173eed)


- Edit Member Info 

![Screenshot 2023-06-13 193726](https://github.com/anxkhn/bookwise/assets/83116240/fcf67c47-795b-40a2-bb73-8a7dc9e5d9c3)


- View Detailed Member Info

![Screenshot 2023-06-13 193739](https://github.com/anxkhn/bookwise/assets/83116240/6393ba38-25d0-4e68-84ed-97f32f68ea9f)




## Transactions

- View Recent transactions

- Check fees due

![Screenshot 2023-06-13 193831](https://github.com/anxkhn/bookwise/assets/83116240/573f6256-1b70-4dfe-b653-317919507b3d)


- Detailed Calculation

![Screenshot 2023-06-13 193953](https://github.com/anxkhn/bookwise/assets/83116240/92052e85-40c8-4b9c-8a4a-b35026fbf212)


- Manual Searching of past transactions

![Screenshot 2023-06-13 193854](https://github.com/anxkhn/bookwise/assets/83116240/0224e92d-12ef-4427-9d2b-d1b7d584cd6e)


- Records of past transactions

![Screenshot 2023-06-13 194016](https://github.com/anxkhn/bookwise/assets/83116240/b7ac057a-434e-44bc-8468-4d2625f15d86)


## Report

- Top performing books 

![Screenshot 2023-06-13 194033](https://github.com/anxkhn/bookwise/assets/83116240/02a0e93d-dcdb-4c5d-b203-9b8f417284ca)


- Top paying members

![Screenshot 2023-06-13 194041](https://github.com/anxkhn/bookwise/assets/83116240/5e3d6035-ae6d-484e-8b82-83d91139a19c)

---
## Instructions

1. Create a virtual environment using :
```
python -m venv env
```
2. Install the dependencies :
```
pip install -r requirements.txt
```
3. Run the application on `http://localhost:5000` by using:
```
flask run
```

Check out the deployed version of this app on PythonAnywhere:
[bookwise.pythonanywhere.com/login](https://bookwise.pythonanywhere.com/login)
