# BulkyBook Store

A full-featured **ASP.NET Core MVC e-commerce application** for selling books online — with shopping cart, order management, user roles, company accounts, and Stripe payment integration.

## What it does

BulkyBook Store is a multi-layered bookstore web application that supports individual shoppers and company customers. It covers the full shopping lifecycle from product browsing to order fulfillment, with admin and employee dashboards for inventory and order management.

## Tech Stack

- **ASP.NET Core MVC** — server-rendered UI with Razor views
- **Entity Framework Core** — Code-First with SQL Server
- **ASP.NET Identity** — authentication and role-based authorization
- **Repository Pattern + Unit of Work** — data access abstraction
- **Stripe** — payment processing

## Key Features

- Product catalog with categories and cover types
- Shopping cart and order checkout flow
- Multiple user roles: Admin, Employee, Company, Individual Customer
- Company accounts with deferred payment support
- Order status management (pending, approved, shipped, cancelled)
- Admin dashboard for products, categories, and order management
- Image upload for book covers

## Project Structure

| Project | Purpose |
|---|---|
| `BulkyBook.DataAccess` | EF Core DbContext, repositories, migrations |
| `BulkyBook.Models` | Domain entities |
| `BulkyBook.Utility` | Constants, email sender, Stripe helper |
| `BulkyBook.Web` | ASP.NET Core MVC web application |

## Getting Started

1. Set your SQL Server connection string and Stripe keys in `appsettings.json`.
2. Apply migrations: `dotnet ef database update`
3. Run: `dotnet run --project BulkyBook.Web`
