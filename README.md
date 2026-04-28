## Culinardea – Recipe Discovery Web App

Culinardea is a modern web application designed to help users explore, filter, and interact with recipes through a clean and intuitive interface. Culinardea is a digital cooking journal web application that allows users to explore cooking-related content and create their own personalized recipes and notes.

The application focuses on usability, data persistence, and security, offering users a structured and interactive way to manage their cooking ideas.

## Status

https://culinardea.app/

---

## Preview

<img width="1434" height="773" alt="Captură de ecran din 2026-04-12 la 12 55 08" src="https://github.com/user-attachments/assets/1b2b03ce-e233-4558-bd35-83a361aa3f1b" />

---

## What makes it different

- Recipe filtering system
- User interaction (favorites / tried / my tips / categories / add their own data)
- Clean UI focused on usability

---

## Why this project

Recipe applications are often cluttered or hard to navigate.

Culinardea focuses on simplicity, usability, and fast interaction to improve the user experience.

---

## Screenshots of the app working and layout

<img width="1376" height="768" alt="presentation_image3" src="https://github.com/user-attachments/assets/7ba9f8c6-8589-49f9-be70-0723fcbddd80" />


<img width="1200" height="891" alt="presentation_image2" src="https://github.com/user-attachments/assets/d25ca8e8-62c1-44c1-b767-3406b34d1c65" />

---

## Features
- User authentication (login & registration)
- Email verification system
- Add, edit, and delete personal recipes
- Persistent data storage using PostgreSQL
- Account deletion with complete data removal
- Feedback & issue reporting system
- Responsive UI with custom design (header, footer, layout)
- Responsive design complet
- Recipes loaded dynamically from Supabase PostgreSQL with local fallback
- Professional email — contact@culinardea.app 

---

## Security

### Authentication & Authorization
- OAuth 2.0 Google Authentication via Supabase
- Email + Password authentication with JWT session management
- Secure email change — confirmation required on both addresses
- Secure password change — recent session required
- Password reset via signed email link
- Account selector forced at every Google login 

### Password Security
- Password strength checker — 5 levels: WEAK → MEDIUM → GOOD → STRONG → FORTRESS
- HaveIBeenPwned API integration — k-anonymity check against 600M+ compromised passwords
- Minimum 8 characters with complexity requirements (uppercase, lowercase, digits, special characters)
- Blacklist of 30 common/forbidden passwords
- Weak pattern detection (repetitions, sequences, keyboard patterns)

### Anti-Abuse & Bot Protection
- Cloudflare Turnstile — anti-bot protection
- Rate limiting with exponential backoff
- Supabase Attack Protection enabled

### Database Security
- Row Level Security (RLS) enforced on all PostgreSQL tables
- Each user accesses exclusively their own data
- Automatic profile creation via database trigger
- Cascade delete — complete data removal on account deletion
- Foreign key constraints on all relational tables
- Admin role system via dedicated admins table — role-based access control for privileged operations
- Recipe images protected by RLS — only admin can upload, update or delete images
- Secure storage of sensitive data (environment variables, secrets)

### Frontend Security
- XSS protection: global sanitizer on all user inputs
- Tips sanitizer: strict whitelist 
- URL validation: only https:// permitted 
- Zero sensitive data in localStorage
- Local HTTP server replacing insecure file:// protocol

### Legal & Compliance
- GDPR compliant: Privacy Policy, Terms & Conditions, Cookie Policy
- Cookie consent banner with Accept/Reject options
- Explicit consent checkbox at registration
- Data operator identified (Art. 13 GDPR)
- Data retention periods documented
- User rights documented and accessible (access, rectification, deletion, portability)

---

## Backend Architecture

- Supabase service key secured 
- Routes: /api/auth, /api/recipes, /api/email
- Middleware: rate limiting, admin-only protection
- Recipes loaded via backend API 

---

### Backend & API Security
- Backend API layer separating frontend from database
- Admin-only middleware protecting sensitive endpoints
- Server-side rate limiting via express-rate-limit (5 req/15min login, 100 req/15min general, and so on)
- CORS configured to accept only trusted origins
  
---

## Advanced Security (Planned)
- Performing basic security testing (penetration testing principles)
- Identifying and mitigating common vulnerabilities (OWASP Top 10)
- Improving API security and access control mechanisms
- Enhancing overall application security posture
- Two-Factor Authentication (2FA)
- Secure API design and protection against common attacks
- Protection against SQL Injection
  
---

## PWA — Progressive Web App
- Installable on iPhone and Android as native app
- Offline support via Service Worker cache
- Custom theme color and splash screen
- Apple mobile web app optimized

---

## UI / UX
- Clean and modern interface
- Warm color palette
- Structured layout for intuitive navigation
- Focus on user-friendly experience
- 3D effect
- Split Login Page Transition

---

## Database Architecture
- 15 PostgreSQL tables with RLS (added: recipe_images, admins)- Automatic profile creation via database triggers
- 152 recipes migrated from static JavaScript to PostgreSQL (recipes_catalog)
- Cascade delete for complete data removal
- Foreign key constraints on all tables
  
---

## Tech Stack
- HTML, CSS, JavaScript
- Node.js (local development server)
- PostgreSQL (database)
- Supabase (backend services & database management)
- Docker (containerization)
- Git / GitHub (version control)
- iTerm2 (development environment)
- Cloudflare Turnstile (bot protection)
- VS Code (programming)
- Dynamic recipe catalog via Supabase (migrated from static JavaScript)
- Node.js + Express (backend API server, port 3001)
- Nodemailer (email service — configured)
- dotenv (environment variables management)

---

## Next Improvements
- Advanced search functionality
- AI-based recipe suggestions
- Performance optimization
- Loading state optimization for Supabase recipe fetching
- Recipe order persistence from database

---

## Future Infrastructure & Security Improvements
- Deployment in a cloud environment (e.g., AWS / Azure / GCP)
- Implementation of scalable and highly available architecture
- Secure configuration of cloud resources (networking, access control)
- Continuous monitoring and logging

---

## For further information about the app: contact@culinardea.app 

---

## Note
The full source code is maintained in a private repository for security and intellectual property protection.

© 2026 Culinardea. 
