# 13. Functional Requirements

**Project:** Restaurant Food Ordering System  
**Document Version:** 1.0  
**Status:** Draft  

---

## 1. Introduction

This document defines the functional requirements for the Restaurant Food Ordering System. Functional requirements describe the specific behaviors, features, and functions that the system must perform to satisfy user needs.

---

## 2. System Overview

The Restaurant Food Ordering System enables customers to browse menus, place orders, make payments, and track delivery — all through a web or mobile interface. The system also provides restaurant staff and administrators with tools to manage menus, orders, and reports.

---

## 3. User Roles

| Role | Description |
|------|-------------|
| **Customer** | Registers, browses menu, places and tracks orders |
| **Restaurant Admin** | Manages menu items, views and updates orders |
| **Kitchen Staff** | Views incoming orders, updates preparation status |
| **Delivery Personnel** | Receives delivery tasks, updates delivery status |
| **Super Admin** | Manages system configuration, users, and reports |

---

## 4. Functional Requirements

### 4.1 User Registration & Authentication

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-01 | The system shall allow new customers to register using email and password | High |
| FR-02 | The system shall allow customers to register using Google or Facebook OAuth | Medium |
| FR-03 | The system shall send a verification email upon registration | High |
| FR-04 | The system shall allow registered users to log in with email and password | High |
| FR-05 | The system shall provide a "Forgot Password" feature to reset password via email | High |
| FR-06 | The system shall allow users to update their profile (name, phone, address) | Medium |
| FR-07 | The system shall allow admins to log in through a separate admin portal | High |
| FR-08 | The system shall log out users after a configurable session timeout | Medium |

---

### 4.2 Menu Management

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-09 | The system shall display a list of all available food categories (e.g., Starters, Main Course, Drinks) | High |
| FR-10 | The system shall display menu items with name, description, image, and price | High |
| FR-11 | The system shall allow customers to search menu items by name or keyword | High |
| FR-12 | The system shall allow customers to filter menu items by category, price range, or dietary tag | Medium |
| FR-13 | The system shall allow the restaurant admin to add new menu items | High |
| FR-14 | The system shall allow the restaurant admin to edit existing menu items | High |
| FR-15 | The system shall allow the restaurant admin to mark items as "Available" or "Unavailable" | High |
| FR-16 | The system shall allow the restaurant admin to delete menu items | Medium |
| FR-17 | The system shall support multiple menu item variations (e.g., size: Small / Medium / Large) | Medium |
| FR-18 | The system shall display special offers and discounts on eligible menu items | Low |

---

### 4.3 Shopping Cart

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-19 | The system shall allow customers to add menu items to a shopping cart | High |
| FR-20 | The system shall allow customers to update item quantities in the cart | High |
| FR-21 | The system shall allow customers to remove items from the cart | High |
| FR-22 | The system shall display a real-time cart subtotal, tax, and total amount | High |
| FR-23 | The system shall persist the cart for logged-in users across sessions | Medium |
| FR-24 | The system shall allow customers to apply a promo/coupon code to the cart | Medium |

---

### 4.4 Order Placement

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-25 | The system shall allow customers to place an order after reviewing the cart | High |
| FR-26 | The system shall allow customers to choose between Dine-In, Takeaway, or Delivery | High |
| FR-27 | The system shall allow customers to specify a delivery address for delivery orders | High |
| FR-28 | The system shall allow customers to add special instructions per order | Medium |
| FR-29 | The system shall generate a unique Order ID for every placed order | High |
| FR-30 | The system shall send an order confirmation notification (email/SMS) to the customer | High |
| FR-31 | The system shall forward new orders to the kitchen staff dashboard immediately | High |

---

### 4.5 Payment Processing

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-32 | The system shall allow customers to pay via credit/debit card | High |
| FR-33 | The system shall allow customers to pay via mobile banking (bKash, Nagad) | High |
| FR-34 | The system shall allow cash-on-delivery as a payment option | High |
| FR-35 | The system shall display a payment confirmation screen upon successful payment | High |
| FR-36 | The system shall generate and send a digital invoice/receipt to the customer | High |
| FR-37 | The system shall handle failed payments gracefully and notify the customer | High |
| FR-38 | The system shall support refunds for cancelled orders | Medium |

---

### 4.6 Order Tracking

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-39 | The system shall provide a real-time order status page for customers | High |
| FR-40 | The system shall display order statuses: Pending → Confirmed → Preparing → Out for Delivery → Delivered | High |
| FR-41 | The system shall notify customers via email/SMS at each status change | Medium |
| FR-42 | The system shall allow delivery personnel to update delivery status from their interface | High |
| FR-43 | The system shall display the estimated delivery time to the customer | Medium |

---

### 4.7 Order Management (Admin / Kitchen)

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-44 | The system shall display all incoming orders on the kitchen staff dashboard | High |
| FR-45 | The system shall allow kitchen staff to update order preparation status | High |
| FR-46 | The system shall allow restaurant admin to view all orders with filtering (by date, status, type) | High |
| FR-47 | The system shall allow restaurant admin to cancel an order with reason | Medium |
| FR-48 | The system shall allow restaurant admin to assign delivery orders to delivery personnel | Medium |

---

### 4.8 Reviews & Ratings

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-49 | The system shall allow customers to rate and review a delivered order | Medium |
| FR-50 | The system shall display average ratings on menu items | Medium |
| FR-51 | The system shall allow admin to moderate and respond to reviews | Low |

---

### 4.9 Reports & Analytics (Admin)

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-52 | The system shall generate daily, weekly, and monthly sales reports | Medium |
| FR-53 | The system shall display the most ordered items in a given period | Low |
| FR-54 | The system shall export reports in PDF or CSV format | Low |

---

### 4.10 Notifications

| ID | Requirement | Priority |
|----|-------------|----------|
| FR-55 | The system shall send push notifications for order status updates | Medium |
| FR-56 | The system shall send email notifications for registration, order confirmation, and delivery | High |
| FR-57 | The system shall allow customers to opt-out of promotional notifications | Low |

---

## 5. Summary Table

| Category | Total Requirements | High | Medium | Low |
|----------|-------------------|------|--------|-----|
| Authentication | 8 | 5 | 3 | 0 |
| Menu Management | 10 | 6 | 3 | 1 |
| Shopping Cart | 6 | 4 | 2 | 0 |
| Order Placement | 7 | 6 | 1 | 0 |
| Payment | 7 | 6 | 1 | 0 |
| Order Tracking | 5 | 3 | 2 | 0 |
| Order Management | 5 | 4 | 1 | 0 |
| Reviews | 3 | 0 | 2 | 1 |
| Reports | 3 | 0 | 1 | 2 |
| Notifications | 3 | 1 | 1 | 1 |
| **Total** | **57** | **35** | **17** | **5** |

---

*Document prepared by: Member 1*  
*Last updated: 2025*
