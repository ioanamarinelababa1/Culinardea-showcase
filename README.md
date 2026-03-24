# 🍽️ YourRecipe (Showcase)

## 📌 Overview
YourRecipe is a digital cooking journal web application that allows users to explore cooking-related content and create their own personalized recipes and notes.

The application focuses on usability, data persistence, and security, offering users a structured and interactive way to manage their cooking ideas.

## 🚧 Status
Work in progress (full implementation available in a private repository)

---

## 🛠 Tech Stack
- HTML, CSS, JavaScript
- Node.js (local development server)
- PostgreSQL (database)
- Supabase (backend services & database management)
- Docker (containerization)
- Git / GitHub (version control)
- iTerm2 (development environment)
- Cloudflare Turnstile (bot protection)
- VS Code (programming)

---

## ✨ Features
- User authentication (login & registration)
- Email verification system
- Add, edit, and delete personal recipes
- Persistent data storage using PostgreSQL
- Account deletion with complete data removal
- Feedback & issue reporting system
- Responsive UI with custom design (header, footer, layout)

---

## 🔐 Security
- Authentication flow implementation
- Email verification for user accounts
- Secure handling of API keys
- Privacy policy integration
- Basic protection against common vulnerabilities
- Enforced HTTPS for all communications
- Implemented secure authentication flows (JWT / session-based)
- Secure storage (localStorage curat)
- Input validation and sanitization
- Rate limiting and brute-force protection + rate limiting: exponential backoff (3 fails→15s, 5→5min, 10→30min)
- Password strength checker (5 levels: WEAK → FORTRESS)
- HaveIBeenPwned API (k-anonymity, 600M compromised passwords)
- Cloudflare Turnstile anti-bot (active on HTTPS)
- XSS protection: escapeHTML(), sanitizeTip(), URL validation
- RLS on all 12 database tables
- GDPR compliant: Privacy Policy, Terms, Cookie Policy
- Secure email & password change (Supabase)
- Minimum 8 character passwords with complexity requirements
---

## 🛡 Advanced Security (Planned)
- Performing basic security testing (penetration testing principles)
- Identifying and mitigating common vulnerabilities (OWASP Top 10)
- Improving API security and access control mechanisms
- Enhancing overall application security posture
- Two-Factor Authentication (2FA)
- Secure API design and protection against common attacks
- Protection against SQL Injection
- Secure storage of sensitive data (environment variables, secrets)

---
## 🎨 UI / UX
- Clean and modern interface
- Warm color palette
- Structured layout for intuitive navigation
- Focus on user-friendly experience
- 3D effect
- Split Login Page Transition

---

## 🧠 What I’m Learning
- Full-stack web development fundamentals
- Authentication & security best practices
- Database design and integration (PostgreSQL)
- Containerization using Docker
- Debugging and problem solving
- Designing and UX
- How to manage security problems

---

## 💬 System
Users can:
- Send reviews
- Report bugs or issues
- Suggest improvements
- Add recipes to Favorites section
- Add recipes to Tried section
- Add their own recipes with images into a separate window, like a digital cooking book
- Add tips
- Check out season's fruits, vegetables
  
---

## 🗄️ Database Architecture
- 12 PostgreSQL tables with Row Level Security (RLS)
- Automatic profile creation via database triggers
- Cascade delete for complete data removal
- Foreign key constraints on all tables

---

## 🚀 Next Improvements
- Advanced search functionality
- AI-based recipe suggestions
- Performance optimization

---

## ☁️ Future Infrastructure & Security Improvements
- Deployment in a cloud environment (e.g., AWS / Azure / GCP)
- Implementation of scalable and highly available architecture
- Secure configuration of cloud resources (networking, access control)
- Continuous monitoring and logging

---

## 🔒 Note
The full source code is maintained in a private repository for security and intellectual property protection.
