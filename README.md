# 📖 API Documentation

Welcome to the API documentation! This readme provides an overview of the various API endpoints available for our services, categorized into four main folders: **provider**,**authentication**, **general**, **tickets**,**employees**,**branches** and "**evaluation** . Each section includes detailed information on how to use the APIs, along with examples and important parameters.

## Table of Contents
- [Headers Information](#-headers-information)
- [Authentication APIs](#-authentication-apis)
- [Provider APIs](#-provider-apis)
- [General APIs](#-general-apis)
- [Tickets APIs](#-tickets-apis)
- [Employees APIs](#-employees-apis)
- [branches APIs](#-branches-apis)



---

## 🚀 Headers Information

All requests must include the following headers:
- `lng`: Language parameter, default is `'ar'`.
- `accept`: Parameter with the value `'application/json'`.

Additionally, all provider APIs require a bearer token in the header Except login and refresh token API:
- `authorization`: Parameter with the value `'Bearer {token}'`.


---

## 🔐 Authentication APIs

The Authentication APIs handle user authentication processes, including login, registration, and token management. These endpoints are crucial for ensuring secure access to the services. You can find details [HERE](docs/authentication)

### Highlights
- **User Authentication**: Manage login and registration processes.
- **Token Management**: Handle access and refresh tokens for secure communication.


## 🧑‍💼 Provider APIs

The provider APIs are designed to handle various provider-related functionalities, such as managing orders, profiles, and evaluations. These endpoints allow providers to interact with the Orders, and provider feedback. Go to provider's APIs [HERE](docs/provider)

### Highlights
- **Follow Orders**: View all orders with ease and filter them by date and service type.
- **Order Details**: Navigate through order steps and upload invoices to finalize the order.
- **Quick Order**: Navigate through order steps and upload invoices to finalize the order.
- **Feedback**: Provide evaluations and feedback on services received.
- **Reschedule Appointments**: Reschedule order appointment times conveniently.
- **Open Tcikets**: Open Supported Tickets for Providers.
- **Messaging**: Communicate with customers effortlessly via chat.

---

## 🌐 General APIs

The General APIs provide access to a variety of services and product-related data. These endpoints are essential for fetching information about available services, products, and providers. They facilitate the process of searching and filtering products based on different criteria.  Go to General APIs from [HERE](docs/general)

---

## 🎟️ Tickets APIs

The Tickets APIs are designed to manage support tickets. These endpoints allow providers to create, list, and manage their support requests efficiently. They ensure that provider issues are tracked and resolved promptly. The full details is [HERE](docs/tickets)

### Highlights
- **Ticket Categories**: Fetch available categories for support tickets.
- **Create Tickets**: Allow providers to submit new support tickets.

---

## 🌳 Branches APIs

The Branches APIs provide endpoints for managing branch information, including adding new branches, editing branch details, managing employees, and setting working zones.[HERE](docs/Branches)


### Highlights
- **Add New Branch**: Create a new branch with specified details.
- **Edit Branch**: Update existing branch information.
- **Delete Branch**: Remove a branch from the system.
- **Add Employee to Branch**: Assign employees to specific branches.
- **Set Working Zones for Branch**: Define working zones for branches.


---
## 👩‍💼 Employees APIs

The Employees APIs allow management of employee information within branches, including adding new employees, editing employee details, deleting employees, setting working hours, and managing banned times.[HERE](docs/users)


### Highlights
- **Add New Employee**: Register a new employee with specified details.
- **Edit Employee**: Update existing employee information.
- **Delete Employee**: Remove an employee from the system.
- **Set Working Hours**: Define regular working hours for employees.
- **Manage Banned Times**: Specify times when employees are unavailable.

