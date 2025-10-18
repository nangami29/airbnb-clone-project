Airbnb Clone Project
Overview

The Airbnb Clone Project is a comprehensive full-stack web application designed to simulate the core functionality of the Airbnb platform. It allows users to explore property listings, make bookings, and manage reservations in a secure and scalable environment.

This project focuses on backend architecture, database design, API development, and application security, preparing developers to handle real-world full-stack challenges using modern tools and technologies.

Project Goals

Build a scalable and secure web application with core Airbnb features.

Strengthen understanding of backend architecture and database management.

Implement RESTful APIs with advanced security measures.

Practice collaborative software development using GitHub.

Learn how to design and manage CI/CD pipelines for efficient deployment.

Gain experience integrating multiple technologies into a unified system.

Tech Stack

Backend Framework: Django (Python)
Database: MySQL
API Technology: GraphQL / REST Framework (Django REST Framework)
Version Control: Git & GitHub
Deployment Tools: Docker, GitHub Actions (for CI/CD)
Security: Django authentication, environment variables, and API key management

Team Collaboration
This project emphasizes teamwork and simulates real-world development workflows. Each team member contributes to specific roles such as:

Backend Developer: API creation, database models, authentication.

DevOps Engineer: CI/CD setup, deployment automation.

Documentation Lead: Ensures clear, structured documentation.

Project Manager: Oversees milestones and team coordination.

Key Features 
User authentication and profile management

Property listing and filtering

Booking and payment simulation

Reviews and ratings system

Admin dashboard for listing management

Secure API endpoints with token-based authentication

Database Design

The database is designed to support the core functionality of the Airbnb Clone application, including users, property listings, bookings, reviews, and payments. Below is a breakdown of the main entities, their important fields, and relationships.

Key Entities
1. Users

Fields: id (primary key), username, email, password, role (guest/host/admin)

Description: Stores information about all users of the platform.

Relationships:

A user can list multiple properties (as a host).

A user can make multiple bookings (as a guest).

A user can write multiple reviews.

2. Properties

Fields: id (primary key), title, description, location, price, host_id (foreign key to Users)

Description: Stores information about the properties listed on the platform.

Relationships:

A property belongs to one host (user).

A property can have multiple bookings.

A property can receive multiple reviews.

3. Bookings

Fields: id (primary key), user_id (guest), property_id, start_date, end_date, status

Description: Tracks reservations made by users for properties.

Relationships:

Each booking belongs to one user (guest).

Each booking is linked to one property.

4. Reviews

Fields: id (primary key), user_id, property_id, rating, comment, created_at

Description: Stores feedback and ratings left by users for properties.

Relationships:

Each review is written by a user.

Each review belongs to a property.

5. Payments

Fields: id (primary key), booking_id, amount, payment_method, payment_status, payment_date

Description: Records payment transactions for bookings.

Relationships:

Each payment is linked to a booking.

Through the booking, the payment is associated with a user and a property.

Entity Relationship Overview

A user can host multiple properties and make multiple bookings.

A property can have multiple bookings and reviews.

Each booking is connected to one user and one property, and has an associated payment.

Reviews are connected to both users and properties.