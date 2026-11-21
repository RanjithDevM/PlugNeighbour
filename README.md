# 🔌 PlugNeighbour – Peer-to-Peer EV Charging Platform

**Connecting EV drivers with nearby home charger owners.**

Created and maintained by **JRD Group Of Companies**

---

## 🌍 About the Project

PlugNeighbour is a peer-to-peer EV charging platform concept that aims to make electric vehicle charging more accessible by connecting EV drivers with individuals who have home charging facilities.

The platform allows charger owners to enrol their charging stations, while EV drivers can discover nearby chargers, request charging sessions, communicate with hosts through WhatsApp, and complete a simulated charging handover process.

The platform also demonstrates a 10% commission model for charging transactions.

### 💡 About the Idea

I don't claim to have invented the concept behind PlugNeighbour. Ideas and inspiration exist everywhere. I collected and explored ideas from different sources and identified a possibility worth experimenting with.

**PlugNeighbour is my attempt to turn those collected ideas into a working prototype and explore how such a platform could function in the real world.**

This project is an experimental implementation focused on learning, problem-solving, and exploring practical possibilities.

---

## ✨ Features

### 🚗 Driver Features
- Driver registration and login.
- Discover available EV charging hosts.
- Request charging sessions.
- Communicate with hosts through WhatsApp.
- Receive a 6-digit charging handover code.
- Track the charging request workflow.

### ⚡ Charger Host Features
- Host registration and login.
- Enrol home charging stations.
- Pin charger location using browser geolocation.
- Manage incoming charging requests.
- Accept or manage charging sessions.
- Verify the driver's 6-digit handover code.
- Complete charging sessions.

### 🛡️ Admin Features
- Dedicated administrator access.
- Review and approve charger registrations.
- Manage the charger approval workflow.
- Maintain an audit log.

### 💰 Business Model Demonstration
- Demonstrates a 10% platform commission.
- Automatically calculates the commission during the simulated charging workflow.
- Explores a possible revenue model for peer-to-peer EV charging.

---

## 🛠️ Technology Stack

| Technology | Purpose |
|---|---|
| HTML5 | Application structure |
| CSS3 | Responsive user interface |
| JavaScript | Application logic and interactions |
| LocalStorage | Browser-based data storage |
| Web Crypto API | Password hashing |
| GitHub Pages | Static website hosting |

**Architecture:** Single-file frontend application.

The entire application is implemented in one file: `index.html`, containing HTML, CSS, and JavaScript.

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/PlugNeighbour.git
```

### 2. Open the Project

```bash
cd PlugNeighbour
```

### 3. Run the Application

Since this is a static frontend project, you can simply open:

```text
index.html
```

in your browser.

Alternatively, use the VS Code Live Server extension to run it locally.

No backend installation or database configuration is required for this prototype.

---

## 🔐 Demo Accounts

The project includes preloaded accounts to explore different user roles.

| Role | Email | Password |
|---|---|---|
| Driver | driver@plugneighbour.app | Driver@Plug2026 |
| Charger Host | host@plugneighbour.app | Host@Plug2026 |
| Admin | admin@plugneighbour.app | Admin@Plug2026 |

**Important:** These are demonstration credentials, not real user accounts. Change the credentials before publishing the repository publicly.

### Admin Access

The administrator interface is accessed through a hidden route.

```text
https://YOUR_USERNAME.github.io/PlugNeighbour/#ops-k9x2m7
```

Replace `YOUR_USERNAME` and `PlugNeighbour` with your GitHub username and repository name.

There is no administrator registration option or visible admin navigation button.

**Security note:** The hidden URL is only an interface-level obscurity measure. It does not provide secure administrator access.

---

## 🧪 How to Test the Complete Workflow

Follow these steps to explore the main application workflow.

### Step 1 – Register a Charger
1. Open the application.
2. Select **I have a charger**.
3. Log in using the host demo account.
4. Enrol a charging station.
5. Use the location pin feature if you want to test browser geolocation.

### Step 2 – Approve the Charger
1. Open the administrator route.
2. Log in using the admin demo account.
3. Review the submitted charger.
4. Approve the charger listing.

### Step 3 – Request a Charging Session
1. Return to the home page.
2. Select **I need a charge**.
3. Log in using the driver demo account.
4. Discover the approved charger.
5. Submit a charging request.

### Step 4 – Accept the Request
1. Log in as the charger host.
2. Review the incoming request.
3. Accept the charging request.

### Step 5 – Complete the Charging Handover
1. Open the driver account.
2. Display the generated 6-digit handover code.
3. Open the host account.
4. Enter the driver's code.
5. Complete the simulated charging session.
6. Observe the automatic 10% commission calculation.

**Note:** The demo workflow is intended for testing. Use the same browser and website origin when switching between demo accounts because the application uses browser LocalStorage.

---

## 🔒 Security Implementation

The prototype demonstrates several security-focused implementation practices:

- PBKDF2-SHA256 password hashing.
- Individual salts for password hashing.
- 210,000 hashing iterations.
- Five-attempt login lockout.
- 15-minute session expiry.
- Role and ownership checks within application actions.
- Output escaping to help prevent XSS.
- Content Security Policy.
- Administrator approval workflow.
- Six-digit charging handover codes.
- Audit logging.
- Phone number visibility restrictions until host acceptance.

### ⚠️ Security Limitations

This is a frontend-only prototype, not a production-ready platform.

The application currently uses browser LocalStorage for data persistence.

Consequently:

- Users can modify browser-side data through developer tools.
- Browser-side role checks cannot provide genuine authorization.
- The hidden admin route is discoverable.
- LocalStorage data is not shared across different users' browsers.
- The commission calculation is only a demonstration and does not process actual payments.
- Published demo credentials must never be reused for real accounts.

**Never use this prototype to handle real customers, sensitive personal information, or financial transactions.**

---

## 🔮 Future Improvements

Potential improvements for a production-oriented version include:

- Backend development using Spring Boot or Node.js.
- Centralized database using PostgreSQL or Supabase.
- Secure authentication and server-side role management.
- Real-time charger availability.
- Google Maps integration.
- Real booking and cancellation management.
- Secure payment gateway integration using Razorpay.
- Server-side commission verification.
- Notifications for drivers and charger hosts.
- Improved admin dashboard.
- Mobile application support.

These are potential future enhancements and should not be considered implemented features.

---

## 🌐 Deployment – GitHub Pages

You can host the current prototype using GitHub Pages.

1. Push the project to a GitHub repository.
2. Open the repository's **Settings**.
3. Select **Pages**.
4. Under Build and Deployment, choose **Deploy from a branch**.
5. Select the `main` branch.
6. Select `/ (root)` as the folder.
7. Click **Save**.
8. Wait for GitHub Pages to publish the website.

Your application will be available at:

```text
https://YOUR_USERNAME.github.io/PlugNeighbour/
```

---

## 👨‍💻 Project Information

**Project Name:** PlugNeighbour

**Category:** Peer-to-Peer EV Charging / Web Application

**Development Type:** Frontend Prototype

**Maintained By:** JRD Group Of Companies

**Repository:** PlugNeighbour

**Status:** Prototype / Experimental Development

---

## 📜 Disclaimer

PlugNeighbour is an independently developed experimental prototype based on collected ideas and inspiration.

The project is intended for educational purposes, experimentation, and demonstrating a possible peer-to-peer EV charging model.

It is not currently a commercial EV charging service and does not facilitate verified real-world charging transactions or payments.

**Ideas are everywhere. Innovation begins when we explore the possibilities and try to build something from them.**

---

**Built with curiosity, experimentation, and a willingness to turn ideas into working prototypes.**

© JRD Group Of Companies
