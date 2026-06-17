# 14. Non-Functional Requirements

**Project:** Restaurant Food Ordering System  
**Document Version:** 1.0  
**Status:** Draft  

---

## 1. Introduction

Non-functional requirements (NFRs) define the quality attributes, constraints, and standards that the Restaurant Food Ordering System must meet. Unlike functional requirements that describe *what* the system does, NFRs describe *how well* the system performs.

---

## 2. Non-Functional Requirements

### 2.1 Performance

| ID | Requirement | Metric |
|----|-------------|--------|
| NFR-01 | The system shall load the homepage within 3 seconds under normal load | Page load ≤ 3s |
| NFR-02 | The system shall process and confirm an order within 5 seconds of submission | Order confirmation ≤ 5s |
| NFR-03 | Search results on the menu page shall appear within 2 seconds | Search response ≤ 2s |
| NFR-04 | The system shall support at least 500 concurrent users without performance degradation | Concurrent users ≥ 500 |
| NFR-05 | The system shall handle a peak of 1,000 order transactions per hour during busy periods | Throughput ≥ 1,000 orders/hr |
| NFR-06 | API response time for all endpoints shall not exceed 500ms under normal load | API latency ≤ 500ms |

---

### 2.2 Availability & Reliability

| ID | Requirement | Metric |
|----|-------------|--------|
| NFR-07 | The system shall maintain an uptime of at least 99.5% per month | Uptime ≥ 99.5% |
| NFR-08 | Planned maintenance windows shall not exceed 2 hours per month and must be communicated 24 hours in advance | Downtime ≤ 2 hrs/month |
| NFR-09 | The system shall automatically recover from server crashes within 60 seconds using auto-restart mechanisms | Recovery time ≤ 60s |
| NFR-10 | The system shall use database replication to prevent data loss in case of primary server failure | Zero data loss on failover |
| NFR-11 | The system shall perform automated database backups every 24 hours | Backup frequency: daily |

---

### 2.3 Security

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-12 | All data transmitted between client and server shall be encrypted using HTTPS/TLS 1.2 or higher | Transport encryption |
| NFR-13 | User passwords shall be stored as hashed values using bcrypt with a minimum salt factor of 10 | Password hashing |
| NFR-14 | The system shall implement JWT (JSON Web Token) based authentication with a token expiry of 1 hour | Token-based auth |
| NFR-15 | The system shall implement role-based access control (RBAC) to restrict access to admin and kitchen features | Access control |
| NFR-16 | The system shall prevent SQL injection, XSS, and CSRF attacks through input validation and security headers | Attack prevention |
| NFR-17 | Payment transactions shall comply with PCI-DSS standards and be processed through a certified payment gateway | Payment security |
| NFR-18 | The system shall lock an account after 5 consecutive failed login attempts for 15 minutes | Brute force protection |
| NFR-19 | All sensitive admin actions (e.g., deleting menu items, cancelling orders) shall be logged with timestamp and user ID | Audit logging |

---

### 2.4 Usability

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-20 | The system shall follow a consistent UI design across all pages (fonts, colors, button styles) | UI consistency |
| NFR-21 | A new customer shall be able to register, browse the menu, and place an order in under 5 minutes without assistance | Onboarding ease |
| NFR-22 | The system shall be fully responsive and usable on mobile devices with screen sizes from 320px to 1920px wide | Responsive design |
| NFR-23 | All form fields shall display clear validation error messages within 1 second of incorrect input | Error feedback |
| NFR-24 | The system shall support both English and Bengali languages (i18n) | Multilingual support |
| NFR-25 | The system shall meet WCAG 2.1 Level AA accessibility standards for users with disabilities | Accessibility |

---

### 2.5 Scalability

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-26 | The system architecture shall support horizontal scaling by adding more server instances without code changes | Horizontal scaling |
| NFR-27 | The database shall be designed to support up to 100,000 registered users and 1,000,000 order records without restructuring | Data scalability |
| NFR-28 | The system shall use caching (e.g., Redis) for frequently accessed data such as menu listings to reduce database load | Caching strategy |
| NFR-29 | The system shall support adding new restaurant branches with minimal configuration changes | Multi-branch support |

---

### 2.6 Maintainability

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-30 | The codebase shall follow a modular MVC or layered architecture to allow independent component updates | Modular design |
| NFR-31 | The system shall maintain an API versioning strategy (e.g., /api/v1/) to allow backward-compatible updates | API versioning |
| NFR-32 | All code shall include inline comments and be accompanied by technical documentation | Code documentation |
| NFR-33 | The system shall include automated unit and integration tests with at least 70% code coverage | Test coverage ≥ 70% |
| NFR-34 | Deployment shall be automated using CI/CD pipelines (e.g., GitHub Actions) | CI/CD automation |

---

### 2.7 Portability

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-35 | The web application shall function correctly on the latest two versions of Chrome, Firefox, Safari, and Edge | Cross-browser support |
| NFR-36 | The system shall be containerized using Docker to allow deployment on any cloud platform (AWS, GCP, Azure) | Containerization |
| NFR-37 | The mobile interface shall work on Android 8.0+ and iOS 13+ | Mobile compatibility |

---

### 2.8 Compliance & Legal

| ID | Requirement | Description |
|----|-------------|-------------|
| NFR-38 | The system shall comply with applicable data protection laws (e.g., GDPR for EU users) | Data privacy compliance |
| NFR-39 | The system shall display a Privacy Policy and Terms of Service that users must accept during registration | Legal agreement |
| NFR-40 | The system shall allow users to request deletion of their personal data (Right to Erasure) | Data deletion right |

---

## 3. NFR Classification Summary

| Category | Count |
|----------|-------|
| Performance | 6 |
| Availability & Reliability | 5 |
| Security | 8 |
| Usability | 6 |
| Scalability | 4 |
| Maintainability | 5 |
| Portability | 3 |
| Compliance & Legal | 3 |
| **Total** | **40** |

---

## 4. Priority Matrix

| Priority | Count | NFR IDs |
|----------|-------|---------|
| High (Must Have) | 18 | NFR-01 to NFR-19 |
| Medium (Should Have) | 14 | NFR-20 to NFR-33 |
| Low (Nice to Have) | 8 | NFR-34 to NFR-40 |

---

*Document prepared by: Farhana*  
*Last updated: 18-06-2026*
