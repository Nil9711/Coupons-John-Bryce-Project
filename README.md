# Coupons Management System

A full-stack coupon management application built with Spring Boot and Angular. Final project developed at John Bryce College demonstrating enterprise-level Java and web development skills.

![Java](https://img.shields.io/badge/Java-8-007396?style=flat-square&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-2.0-6DB33F?style=flat-square&logo=spring-boot&logoColor=white)
![Angular](https://img.shields.io/badge/Angular-7-DD0031?style=flat-square&logo=angular&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=flat-square&logo=mysql&logoColor=white)

## Overview

A comprehensive coupon management system that allows companies to create and manage coupons, customers to purchase and use coupons, and administrators to oversee the entire system. Built with a RESTful Spring Boot backend and modern Angular frontend.

## Features

### For Companies
- Create, update, and delete coupons
- Set coupon details (price, category, expiration date)
- Track coupon inventory and sales
- View company-specific dashboard

### For Customers
- Browse available coupons by category
- Purchase coupons
- View purchased coupons
- Track coupon expiration dates

### For Administrators
- Manage companies (CRUD operations)
- Manage customers (CRUD operations)
- System-wide oversight and reporting
- User authentication and authorization

## Tech Stack

### Backend
- **Java 8** - Programming language
- **Spring Boot 2.0** - Application framework
  - Spring Web - REST API
  - Spring Data JPA - Database persistence
  - Spring Boot DevTools - Development utilities
- **MySQL 8.0** - Relational database
- **Maven** - Build and dependency management
- **JAXB** - XML binding

### Frontend
- **Angular 7** - Frontend framework
- **TypeScript 3.2** - Programming language
- **Angular Material 7** - UI component library
- **Angular CDK** - Component dev kit
- **Bootstrap 4** - CSS framework
- **RxJS** - Reactive programming
- **Angular Router** - Navigation and routing

### Testing
- **JUnit** - Java unit testing
- **Jasmine & Karma** - Angular testing
- **Protractor** - End-to-end testing

## Project Structure

```
Coupons-John-Bryce-Project/
├── final/                      # Spring Boot Backend
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/          # Java source code
│   │   │   └── resources/     # Configuration files
│   │   └── test/              # Unit tests
│   ├── pom.xml                # Maven dependencies
│   └── DB_script.sql          # Database schema
│
├── finalAngular/               # Angular Frontend
│   ├── src/
│   │   ├── app/               # Angular components
│   │   ├── assets/            # Static assets
│   │   └── environments/      # Environment configs
│   ├── package.json           # npm dependencies
│   └── angular.json           # Angular configuration
│
└── MyNewCRUDMOCK.sql          # Sample data script
```

## Installation & Setup

### Prerequisites
- Java 8 or higher
- Maven 3.x
- Node.js and npm
- MySQL 8.0
- Angular CLI 7

### Backend Setup

1. **Setup Database**
```bash
# Create MySQL database
mysql -u root -p
CREATE DATABASE coupons_db;

# Run the SQL scripts
mysql -u root -p coupons_db < final/DB_script.sql
mysql -u root -p coupons_db < MyNewCRUDMOCK.sql
```

2. **Configure Database Connection**
Edit `final/src/main/resources/application.properties`:
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/coupons_db
spring.datasource.username=your_username
spring.datasource.password=your_password
```

3. **Run Spring Boot Application**
```bash
cd final
mvn spring-boot:run
```

Backend will run on `http://localhost:8080`

### Frontend Setup

1. **Install Dependencies**
```bash
cd finalAngular
npm install
```

2. **Run Angular Development Server**
```bash
ng serve
```

Frontend will run on `http://localhost:4200`

## API Endpoints

### Company Endpoints
```
GET    /api/companies          # Get all companies
GET    /api/companies/{id}     # Get company by ID
POST   /api/companies          # Create new company
PUT    /api/companies/{id}     # Update company
DELETE /api/companies/{id}     # Delete company
```

### Customer Endpoints
```
GET    /api/customers          # Get all customers
GET    /api/customers/{id}     # Get customer by ID
POST   /api/customers          # Create new customer
PUT    /api/customers/{id}     # Update customer
DELETE /api/customers/{id}     # Delete customer
```

### Coupon Endpoints
```
GET    /api/coupons            # Get all coupons
GET    /api/coupons/{id}       # Get coupon by ID
POST   /api/coupons            # Create new coupon
PUT    /api/coupons/{id}       # Update coupon
DELETE /api/coupons/{id}       # Delete coupon
GET    /api/coupons/category/{category}  # Get by category
```

## Key Features Demonstrated

### Backend
- ✅ RESTful API design
- ✅ Spring Boot configuration
- ✅ JPA/Hibernate ORM
- ✅ MySQL integration
- ✅ CRUD repository pattern
- ✅ Entity relationships
- ✅ Exception handling
- ✅ Dependency injection

### Frontend
- ✅ Angular component architecture
- ✅ TypeScript programming
- ✅ Angular Material components
- ✅ HTTP client services
- ✅ Reactive forms
- ✅ Routing and navigation
- ✅ Observables and RxJS
- ✅ Responsive design with Bootstrap

## Database Schema

The system uses a relational database with tables for:
- **Companies** - Business entities creating coupons
- **Customers** - Users purchasing coupons
- **Coupons** - Coupon details and inventory
- **Customer_Coupons** - Junction table for purchases

## Development Commands

### Backend (Maven)
```bash
mvn clean install    # Build project
mvn test            # Run tests
mvn spring-boot:run # Run application
```

### Frontend (Angular)
```bash
ng serve            # Development server
ng build            # Production build
ng test             # Run unit tests
ng e2e              # End-to-end tests
ng lint             # Lint code
```

## Author

**Nil Golan**
Final Project - John Bryce College

## License

MIT

---

*A full-stack coupon management system built with Spring Boot and Angular*
