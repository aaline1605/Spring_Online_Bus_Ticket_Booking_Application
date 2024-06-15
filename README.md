# Bus Ticket Booking Management System

## Introduction

This project is a Bus Ticket Booking Management System, which allows users to register, login, search for buses, book tickets, and generate booking confirmation PDFs. 
The system is designed for both regular users and admin users. Admins can manage buses, including adding, updating, and deleting bus details. In Addition, I attached Drive link able to see 
FrontEnd part as well as Documentation and Screenshots. Make Sure to read Mandatory Information.

## Table of Contents

- Introduction
- Features
- Technologies Used
- Project Structure
  - DTO
  - Entities
  - Repositories
  - Services
  - Controllers
- Running the Application
  - Prerequisites
  - Steps
- Usage
  - User Registration and Login
  - Admin Functionalities
  - Booking Tickets
-Mandatory Information
  - To configure Admin Information
-FrontEnd
  - see the frontend Parts


## Features

- User registration and login
- Admin and User roles with different access controls
- Search for buses by origin, destination, and date
- Book bus tickets and specify passenger details
- View individual booking tickets
- Generate booking confirmation PDFs
- Admin functionalities to add, update, and delete bus details

## Technologies Used

- Java
- Spring Boot
- Spring Security
- Thymeleaf
- iTextPDF for PDF generation
- Lombok
- Jakarta Servlet API

## Project Structure

### DTO

Data Transfer Objects used for transferring data between different layers of the application.

- **UserDto.java**: A DTO for user registration and login.

### Entities

Database entities representing the core components of the system.

- **Passengers.java**: Entity representing passengers.
- **Bus.java**: Entity representing buses.
- **Booking.java**: Entity representing bookings.
- **PassengerDetail.java**: Entity representing details of passengers in a booking.

### Repositories

Interfaces for data access operations.

- **PassengerRepository.java**: Repository for `Passengers` entity.
- **BusRepository.java**: Repository for `Bus` entity.
- **BookingRepository.java**: Repository for `Booking` entity.

### Services

Business logic of the application.

- **PassengerService.java**: Implements `UserService` interface and handles passenger-related operations.
- **GeneratePdfService.java**: Service for generating PDFs.
- **CustomUserDetailService.java**: Service for loading user details for Spring Security.
- **CustomHandlerUsers.java**: Custom authentication success handler.
- **BusService.java**: Handles bus-related operations.
- **BookingService.java**: Handles booking-related operations.

### Controllers

Controllers to handle HTTP requests.

- **PassengerController.java**: Handles passenger-related endpoints.
- **BusController.java**: Handles admin and bus-related endpoints.
- **BookingController.java**: Handles booking-related endpoints.

## Running the Application

### Prerequisites

- Java 17 or higher
- Maven 3.6.3 or higher
- A relational database (e.g., MySQL, PostgreSQL)

### Steps

1. Clone the repository
    ```sh
    git clone https://github.com/your-username/BusTicketBookingManagement.git
    cd BusTicketBookingManagement
    ```

2. Configure the database
    - Update the `application.properties` file in `src/main/resources` with your database configuration.

3. Build the project
    ```sh
    mvn clean install
    ```

4. Run the application
    ```sh
    mvn spring-boot:run
    ```

5. Access the application
    - Navigate to `http://localhost:8080` in your web browser.

## Usage

### User Registration and Login

- Register a new user by accessing `/registration`.
- Login with registered credentials at `/login`.

### Admin Functionalities

- Access the admin page at `/admin` after logging in as an admin.
- Add a new bus via `/addBus`.
- View all buses at `/viewAllBuses`.
- Find a bus by ID at `/findBusById`.
- Update bus details via `/updateByBus`.
- Delete a bus via `/delete/{serialNo}`.

### Booking Tickets

- Search for buses from the user home page.
- Book a bus via `/bookBus/{busId}`.
- View bookings at `/bookings`.
- Generate PDF of a booking at `/generatePdf/{bookingId}`.

### Mandatory Information

- Kindly Request, When You evaluate my application at first time you must register first, then go to MySQL table add your ROLE as ADMIN.Otherwise it will save user. For security reasons 
  ADMIN role only add manually to respective database.
- Once you updated your Role as ADMIN then you can login and access ADMIN PAGE.

### FrontEnd

-To see this project FrontEnd Part as well Documentation an ScreenShots. Here, I attached Drive link...,
- Click Here: https://drive.google.com/drive/folders/1A-fCL6w6K1PFeTjDye8xQHdwO_L7IRbi?usp=drive_link

###  Acknowledgements
Thanks to the Spring Boot and Spring Security teams for providing such powerful frameworks.
Special thanks to the Thymeleaf community for the excellent templating engine.
Gratitude to the creators of iTextPDF for the PDF generation library.


***This README provides a comprehensive overview of the project, its structure, how to run it***

---
***Happy Coding!***

  

















Contributions are welcome! Please create a pull request or open an issue to discuss any changes.

