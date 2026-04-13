# 🐾 PetCore

> A comprehensive backend ecosystem for pet care management — connecting pet owners, veterinarians, products, and services through a clean, scalable RESTful API.

![.NET](https://img.shields.io/badge/.NET-8.0-512BD4?style=flat-square&logo=dotnet)
![ASP.NET Core](https://img.shields.io/badge/ASP.NET_Core-Web_API-512BD4?style=flat-square&logo=dotnet)
![EF Core](https://img.shields.io/badge/EF_Core-ORM-512BD4?style=flat-square)
![SQL Server](https://img.shields.io/badge/SQL_Server-Database-CC2927?style=flat-square&logo=microsoftsqlserver)
![Clean Architecture](https://img.shields.io/badge/Architecture-Clean-brightgreen?style=flat-square)
![JWT](https://img.shields.io/badge/Auth-JWT-orange?style=flat-square)

---

## 📌 Overview

**PetCore** is a feature-rich backend API built with **ASP.NET Core** and **Clean Architecture**, designed to serve as the backbone of a full pet care platform. It handles everything from pet management and vet appointments to product marketplaces and real-time chat.

---

## ✨ Features

- 🔐 **Authentication & Authorization** — JWT-based auth with role support (Owner, Vet)
- 🐶 **Pet Management** — Register, manage, and subscribe pets to the platform
- 🛒 **Product Marketplace** — Browse and list products with hierarchical category filtering (Category → Animal Type)
- 🏥 **Vet Directory** — Search vets by specialization, view profiles, CVs, and availability
- 📅 **Appointment Booking** — Book vet appointments with availability management
- 🛍️ **Pet Listings** — Owners can list pets for sale with availability control
- 💬 **Chatbot Integration** — Built-in chatbot messaging system
- ❤️ **Social Features** — Likes, comments, and reviews on products and listings
- 📦 **Subscription System** — Pet subscription management

---

## 🏗️ Architecture

This project follows **Clean Architecture** principles with clear separation of concerns:

```
PetCore/
├── PetCore.API/              # Presentation Layer — Controllers, Middleware, Extensions
├── PetCore.Application/      # Application Layer — Services, CQRS, DTOs, Validators
├── PetCore.Core/             # Domain Layer — Entities, Interfaces, Domain Logic
├── PetCore.Infrastructure/   # Infrastructure Layer — EF Core, Repos, External Services
└── PetCore.sln
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Framework | ASP.NET Core 8 |
| Language | C# |
| ORM | Entity Framework Core |
| Database | SQL Server |
| Authentication | JWT + ASP.NET Identity |
| Caching | Redis |
| Architecture | Clean Architecture, CQRS |
| Patterns | Repository, Unit of Work, Specification |
| Mapping | AutoMapper |
| API Docs | Swagger / OpenAPI |

---

## 🚀 Getting Started

### Prerequisites

- [.NET 8 SDK](https://dotnet.microsoft.com/download)
- [SQL Server](https://www.microsoft.com/en-us/sql-server)
- [Redis](https://redis.io/) *(optional — for caching)*

### Installation

```bash
# 1. Clone the repository
git clone https://github.com/Mariam-SM/PetCore.git
cd PetCore

# 2. Restore dependencies
dotnet restore

# 3. Update the connection string in appsettings.json
# "ConnectionStrings": {
#   "DefaultConnection": "Server=.;Database=PetCoreDb;Trusted_Connection=True;"
# }

# 4. Apply migrations
dotnet ef database update --project PetCore.Infrastructure --startup-project PetCore.API

# 5. Run the API
dotnet run --project PetCore.API
```

### API Documentation

Once running, navigate to:
```
https://localhost:{port}/swagger
```

---

## 📂 Key Endpoints *(coming soon)*

| Method | Endpoint | Description |
|---|---|---|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and get JWT token |
| GET | `/api/vets` | Browse vets by specialization |
| POST | `/api/appointments` | Book a vet appointment |
| GET | `/api/products` | Browse products by category & animal type |
| POST | `/api/pets` | Add a new pet |
| GET | `/api/pets-for-sale` | Browse pets listed for sale |

---

## 🗺️ Roadmap

- [x] Project setup & Clean Architecture scaffold
- [x] Authentication (JWT + Identity)
- [ ] Pet management module
- [ ] Vet directory & appointment booking
- [ ] Product marketplace with category filtering
- [ ] Chatbot integration
- [ ] Redis caching layer
- [ ] Angular frontend *(planned)*

---

## 👩‍💻 Author

**Mariam Sayed Mohammed**
Backend .NET Developer

[![LinkedIn](https://img.shields.io/badge/LinkedIn-mariam--sayedd-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/mariam-sayedd)
[![GitHub](https://img.shields.io/badge/GitHub-Mariam--SM-181717?style=flat-square&logo=github)](https://github.com/Mariam-SM)
[![Portfolio](https://img.shields.io/badge/Portfolio-mariam--sm.github.io-ff6b6b?style=flat-square)](https://mariam-sm.github.io/portfolio)

---

## 📄 License

This project is licensed under the MIT License.
