# Cinema Management System (CMS)

A **web-based Cinema Management System** built with **Flask, Python, and MySQL**, designed to streamline cinema operations. The system allows management of **customers, movies, ticket bookings, and food items**, while providing detailed **reporting and analytics**. It supports **admin and cashier roles**, ensuring smooth management of cinema scheduling, ticket sales, and inventory.

---

## Features

### Customer Management
- Add, update, delete, and search customers
- Customer login and registration functionality
- Display a list of all customers

### Movie Management
- Add, update, delete, and search movies
- Display movie details and list of available movies
- Movie schedule and booking management

### Ticket Booking
- Book tickets for movies in different halls
- Check seat availability for movie shows

### Food Management
- Add, update, delete, and search food items available in the cinema
- Manage food inventory, prices, and quantities

### Reporting and Analytics
- Total customers and bookings
- Revenue breakdown by movies and genres
- Most popular movies, peak revenue days, and hall utilization rate

### Admin and Cashier Login
- Admin login to manage movies, customers, and food items
- Cashier login for handling food item management and transactions

---

## Technologies Used
- **Flask** – Python-based micro web framework  
- **MySQL** – Database for storing cinema data  
- **SQLAlchemy** – ORM for interacting with MySQL  
- **HTML, CSS, Bootstrap** – Frontend design and responsive UI  
- **Jinja2** – Template engine for dynamic content  

---

## Database Schema

### Customer Table
| Column | Type |
|--------|------|
| customer_id | Primary Key |
| customer_name |  |
| customer_phone |  |
| customer_feedback |  |
| customer_password |  |

### Movie Table
| Column | Type |
|--------|------|
| MovieID | Primary Key |
| MovieName |  |
| Director |  |
| Language |  |
| Genre |  |
| Release_Date |  |
| Duration |  |
| Movie_Description |  |
| PosterPath |  |
| Price |  |

### Ticket Table
| Column | Type |
|--------|------|
| TicketID | Primary Key |
| MovieID | Foreign Key |
| CustomerID | Foreign Key |
| HallID | Foreign Key |
| ShowDate |  |
| ShowTime |  |
| Price |  |

### Food Item Table
| Column | Type |
|--------|------|
| item_id | Primary Key |
| Item_name |  |
| Quantity_Available |  |
| Price |  |

### Hall Table
| Column | Type |
|--------|------|
| Hall_ID | Primary Key |
| Hall_name |  |
| Capacity |  |

### Movie Show Table
| Column | Type |
|--------|------|
| ShowID | Primary Key |
| MovieID | Foreign Key |
| HallID | Foreign Key |
| ShowDate |  |
| ShowTime |  |

### Hall Seat Table
| Column | Type |
|--------|------|
| SeatID | Primary Key |
| ShowID | Foreign Key |
| IsBooked |  |
| Seat_Row |  |
| Seat_Column |  |

---
## Application Routes
| Route                                | Method    | Description                                  |
| ------------------------------------ | --------- | -------------------------------------------- |
| `/`                                  | GET       | Home page                                    |
| `/next_operation`                    | GET       | Page showing available movies                |
| `/add_customer`                      | GET, POST | Add a new customer                           |
| `/list_customers`                    | GET       | List all customers                           |
| `/delete_customer/<int:customer_id>` | GET, POST | Delete a specific customer                   |
| `/update_customer/<int:customer_id>` | GET, POST | Update customer details                      |
| `/search_customer`                   | GET, POST | Search for a customer                        |
| `/Tlog`                              | GET, POST | Ticket vendor login page                     |
| `/Tmanager`                          | GET, POST | Ticket manager dashboard                     |
| `/movie/<int:movie_id>`              | GET       | View details of a specific movie             |
| `/movie-schedule/<int:movie_id>`     | GET       | View movie schedule                          |
| `/food_item`                         | GET, POST | Manage food items (add/update/delete/search) |
| `/report`                            | GET       | View system reports                          |

---


## 👥 Contributors
- [Aya Fares](https://github.com/AyaF2005/Cinema-Management-System-CMS-/edit/main/README.md)
- [Asmaa Fares]([https://github.com/partner-username](https://github.com/itsAsmaa))

