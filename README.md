Read [](file:///d%3A/Projects/Fullstack%20projects/Car%20rental%20management%20system/Car_rental_management/README.md)

# Car Rental Management System (CRMS)

A full-stack web application for managing car rentals, built with Angular on the frontend and Spring Boot on the backend. This system supports role-based access for admins, agents, and customers, enabling efficient management of car inventory, bookings, payments, and reporting.

## Features

- **User Authentication & Authorization**: Secure login/registration with JWT tokens and role-based access control (Admin, Agent, Customer).
- **Car Management**: Add, view, and categorize cars with details like make, model, and availability.
- **Booking System**: Create and manage car bookings, with real-time availability checks.
- **Reporting**: Generate booking and payment reports for admins and agents.
- **Responsive UI**: Modern, mobile-friendly interface using Angular Material and Bootstrap.
- **RESTful APIs**: Backend APIs for all CRUD operations, integrated with MySQL database.

## Tech Stack

### Frontend
- **Angular 14**: Framework for building the user interface.
- **TypeScript**: For type-safe development.
- **Angular Material**: UI components (tables, forms, datepickers, etc.).
- **NgRx**: State management for complex application state.
- **Bootstrap**: Additional styling and responsiveness.
- **RxJS**: Reactive programming for asynchronous operations.
- **Karma & Jasmine**: Unit testing framework.

### Backend
- **Spring Boot 2.7**: Java framework for building RESTful services.
- **Java 11**: Programming language.
- **Spring Security**: Authentication and authorization.
- **JWT (JSON Web Tokens)**: Secure token-based authentication.
- **Spring Data JPA**: ORM for database interactions.
- **MySQL**: Primary database for production.
- **H2 Database**: In-memory database for testing.
- **Maven**: Build and dependency management.
- **JUnit**: Unit testing.

## Project Structure

```
Car_rental_management/
├── client/                          # Angular frontend
│   ├── src/
│   │   ├── app/
│   │   │   ├── add-car/             # Component for adding cars
│   │   │   ├── cars/                # Component for viewing cars
│   │   │   ├── category/            # Component for car categories
│   │   │   ├── dashbaord/           # Dashboard component
│   │   │   ├── get-bookings/        # Component for viewing bookings
│   │   │   ├── booking-report/      # Booking reports
│   │   │   ├── payment-report/      # Payment reports
│   │   │   ├── login/               # Login component
│   │   │   ├── registration/        # Registration component
│   │   │   ├── app-navbar/          # Navigation bar
│   │   │   ├── material.module.ts   # Angular Material imports
│   │   │   └── auth.interceptors.ts # HTTP interceptors for auth
│   │   └── services/                # Angular services (auth, http)
│   └── package.json                 # Frontend dependencies
├── server/                          # Spring Boot backend
│   ├── src/main/java/com/wecp/car_rental_management_system/
│   │   ├── controller/              # REST controllers
│   │   ├── entity/                  # JPA entities (User, Car, Booking, etc.)
│   │   ├── repository/              # Data repositories
│   │   ├── service/                 # Business logic services
│   │   ├── jwt/                     # JWT utilities
│   │   └── config/                  # Security and app config
│   ├── src/test/                    # Unit tests
│   └── pom.xml                      # Backend dependencies
├── rest_client/                     # HTTP files for API testing
└── README.md                        # This file
```

## Prerequisites

- **Node.js** (v16 or higher) and **npm** for the frontend.
- **Java 11** and **Maven** for the backend.
- **MySQL** database (or use H2 for development/testing).
- **Git** for cloning the repository.

## Installation & Setup

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/pavanl1122/Car_rental_management.git
   cd Car_rental_management
   ```

2. **Backend Setup**:
   - Navigate to the `server` directory:
     ```bash
     cd server
     ```
   - Configure the database in `src/main/resources/application.properties` (update MySQL credentials if needed).
   - Run the application:
     ```bash
     mvn spring-boot:run
     ```
   - The backend will start on `http://localhost:8080`.

3. **Frontend Setup**:
   - Navigate to the `client` directory:
     ```bash
     cd ../client
     ```
   - Install dependencies:
     ```bash
     npm install
     ```
   - Start the development server:
     ```bash
     npm start
     ```
   - The frontend will run on `http://localhost:3000`.

4. **Testing**:
   - Run backend tests: `mvn test` in the `server` directory.
   - Run frontend tests: `npm test` in the `client` directory.

## API Endpoints

The backend exposes RESTful APIs. Use tools like Postman or the provided `rest_client/*.http` files for testing.

- **Authentication**: `/api/auth/login`, `/api/auth/register`
- **Cars**: `/api/cars` (GET, POST, PUT, DELETE)
- **Bookings**: `/api/bookings`
- **Reports**: `/api/reports/bookings`, `/api/reports/payments`

## Usage

1. Register as a user (customer by default).
2. Admins can add cars and categories.
3. Customers can browse cars and make bookings.
4. Agents can view bookings and generate reports.
5. Access role-specific dashboards via the navbar.

## Contributing

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature-name`.
3. Commit changes: `git commit -m 'Add feature'`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Contact

For questions or support, reach out to the project maintainer.
