# PCSHSNST Booking

<p align="center">
  <img src="https://api.iconify.design/lucide:calendar-check-2.svg?color=%23ffffff" width="64" height="64" alt="PCSHSNST Booking">
</p>

<h3 align="center">A modern booking management system for PCSHSNST.</h3>

<p align="center">
  A simple and responsive platform for managing reservations, schedules, and booking information.
</p>

---

## <img src="https://api.iconify.design/lucide:calendar-days.svg?color=%23ffffff" width="20" height="20" valign="middle"> Overview

PCSHSNST Booking is a web-based reservation system designed to simplify the process of creating and managing bookings.

The system provides two main experiences:

```text
                     PCSHSNST Booking
                            |
              +-------------+-------------+
              |                           |
              v                           v
        Public Booking              Admin Panel
              |                           |
              v                           v
        Create Booking             Manage Bookings
              |                           |
              +-------------+-------------+
                            |
                            v
                       Booking Data
````

Users can submit booking information through the public interface, while administrators can review and manage reservations through a dedicated administration panel.

The repository is structured around a Next.js App Router application with separate admin and API areas.

---

## <img src="https://api.iconify.design/lucide:clipboard-list.svg?color=%23ffffff" width="20" height="20" valign="middle"> Features

### <img src="https://api.iconify.design/lucide:calendar-plus.svg?color=%23ffffff" width="18" height="18" valign="middle"> Booking

The public interface provides a booking workflow for users.

* Select booking information
* Submit reservation details
* Validate form input
* Create booking records
* Display booking status
* Responsive booking interface

Booking records are stored as structured data under the project's `data` directory.

---

### <img src="https://api.iconify.design/lucide:layout-dashboard.svg?color=%23ffffff" width="18" height="18" valign="middle"> Admin Dashboard

Administrators have a dedicated management interface.

```text
Admin
 |
 +-- Dashboard
 |
 +-- Bookings
 |    |
 |    +-- View
 |    +-- Search
 |    +-- Filter
 |    +-- Manage
 |
 +-- Booking Details
 |
 +-- System Management
```

The repository contains a dedicated `app/admin` route with a substantial admin interface for managing the booking system.

---

### <img src="https://api.iconify.design/lucide:search.svg?color=%23ffffff" width="18" height="18" valign="middle"> Booking Management

Administrators can work with submitted booking records through the management interface.

The system is designed around keeping booking information organized rather than requiring administrators to manage reservations manually.

---

### <img src="https://api.iconify.design/lucide:database.svg?color=%23ffffff" width="18" height="18" valign="middle"> Booking Data

The project currently includes a dedicated data source:

```text
data/
└── bookings.json
```

This file contains the booking records used by the application.

---

### <img src="https://api.iconify.design/lucide:shield-check.svg?color=%23ffffff" width="18" height="18" valign="middle"> Validation

The application uses Zod and React Hook Form for structured form handling and validation.

```text
User Input
    |
    v
React Hook Form
    |
    v
Zod Validation
    |
    +---- Invalid ----> Show Error
    |
    v
Booking Request
    |
    v
API
```

---

## <img src="https://api.iconify.design/lucide:monitor-smartphone.svg?color=%23ffffff" width="20" height="20" valign="middle"> Responsive Interface

The interface is designed to work across different screen sizes.

The project uses Tailwind CSS together with Radix UI primitives and a collection of reusable components to build the interface. 

The UI focuses on:

* Responsive layouts
* Clear booking forms
* Accessible controls
* Reusable components
* Calendar-based interactions
* Mobile-friendly interfaces

---

## <img src="https://api.iconify.design/lucide:layers-3.svg?color=%23ffffff" width="20" height="20" valign="middle"> Architecture

The application uses the Next.js App Router.

```text
                        Client
                           |
                           v
                    Next.js Application
                           |
             +-------------+-------------+
             |             |             |
             v             v             v
          Public         Admin          API
          Booking        Panel         Routes
             |             |             |
             +-------------+-------------+
                           |
                           v
                      Booking Data
```

The repository contains:

```text
app/
├── admin/
├── api/
├── layout.tsx
└── page.tsx
```


---

## <img src="https://api.iconify.design/lucide:cpu.svg?color=%23ffffff" width="20" height="20" valign="middle"> Tech Stack

| Technology      | Purpose                  |
| --------------- | ------------------------ |
| Next.js 14      | Application framework    |
| React 18        | User interface           |
| TypeScript      | Type safety              |
| Tailwind CSS    | Styling                  |
| Radix UI        | Accessible UI primitives |
| Lucide React    | Icons                    |
| React Hook Form | Form management          |
| Zod             | Validation               |
| Recharts        | Data visualization       |
| Supabase        | Backend / data services  |
| date-fns        | Date handling            |
| Sonner          | Notifications            |
| Embla Carousel  | Carousel interactions    |
| Next Themes     | Theme management         |

These dependencies are defined in the repository's current `package.json`.

---

## <img src="https://api.iconify.design/lucide:folder-tree.svg?color=%23ffffff" width="20" height="20" valign="middle"> Project Structure

```text
BookingPCSHSNST-Dom4/
│
├── app/
│   ├── admin/
│   ├── api/
│   ├── globals.css
│   ├── layout.tsx
│   └── page.tsx
│
├── components/
│
├── data/
│   └── bookings.json
│
├── hooks/
│
├── lib/
│
├── public/
│
├── styles/
│
├── components.json
├── next.config.mjs
├── package.json
├── tailwind.config.ts
├── tsconfig.json
└── postcss.config.mjs
```

This structure is visible directly in the current repository. 

---

## <img src="https://api.iconify.design/lucide:route.svg?color=%23ffffff" width="20" height="20" valign="middle"> Booking Flow

```text
Visitor
   |
   v
Booking Page
   |
   v
Fill Information
   |
   v
Validate Form
   |
   v
Submit Booking
   |
   v
API
   |
   v
Booking Data
   |
   v
Admin Dashboard
   |
   v
Review / Manage
```

The public booking interface and admin interface are separated into different application routes. 

---

## <img src="https://api.iconify.design/lucide:calendar-clock.svg?color=%23ffffff" width="20" height="20" valign="middle"> Booking Management

The system is designed to centralize reservation information.

Instead of managing requests through messages or spreadsheets:

```text
Before

User
 |
 +-- Message
 +-- Form
 +-- Chat
 +-- Manual Record
 |
 v
Administrator
```

The system provides:

```text
After

User
 |
 v
Booking System
 |
 v
Centralized Booking Data
 |
 v
Admin Dashboard
 |
 +-- Review
 +-- Search
 +-- Manage
 +-- Monitor
```

This makes the booking workflow easier to organize and gives administrators a single place to manage reservations.

---

## <img src="https://api.iconify.design/lucide:chart-no-axes-combined.svg?color=%23ffffff" width="20" height="20" valign="middle"> Dashboard

The project includes charting support through Recharts, allowing the application to present booking-related information visually.

Possible dashboard views include:

* Booking statistics
* Booking trends
* Reservation summaries
* Status breakdowns

---

## <img src="https://api.iconify.design/lucide:bell.svg?color=%23ffffff" width="20" height="20" valign="middle"> Notifications

The application includes Sonner for displaying user-facing notifications and feedback. 

Notifications can be used to communicate:

* Successful bookings
* Validation errors
* Booking updates
* System actions

---

## <img src="https://api.iconify.design/lucide:rocket.svg?color=%23ffffff" width="20" height="20" valign="middle"> Getting Started

### Requirements

* Node.js
* npm, pnpm, Yarn, or Bun

### Clone

```bash
git clone https://github.com/PUKAN223/BookingPCSHSNST-Dom4.git
cd BookingPCSHSNST-Dom4
```

### Install Dependencies

Using Bun:

```bash
bun install
```

Or npm:

```bash
npm install
```

---

## <img src="https://api.iconify.design/lucide:terminal.svg?color=%23ffffff" width="20" height="20" valign="middle"> Development

Start the development server:

```bash
bun run dev
```

Or:

```bash
npm run dev
```

Then open:

```text
http://localhost:3000
```

The repository defines the standard Next.js development, build, lint, and start scripts. 

---

## <img src="https://api.iconify.design/lucide:package.svg?color=%23ffffff" width="20" height="20" valign="middle"> Production

Build the application:

```bash
bun run build
```

Start the production server:

```bash
bun run start
```

---

## <img src="https://api.iconify.design/lucide:wrench.svg?color=%23ffffff" width="20" height="20" valign="middle"> Scripts

| Command         | Description                  |
| --------------- | ---------------------------- |
| `bun run dev`   | Start development server     |
| `bun run build` | Build production application |
| `bun run start` | Start production server      |
| `bun run lint`  | Run Next.js linting          |

These scripts are defined in `package.json`.

---

## <img src="https://api.iconify.design/lucide:palette.svg?color=%23ffffff" width="20" height="20" valign="middle"> UI Components

The project uses a component-based UI architecture.

```text
components/
    |
    +-- Forms
    +-- Dialogs
    +-- Navigation
    +-- Calendar
    +-- Cards
    +-- Tables
    +-- Controls
    +-- Feedback
```

Radix UI provides the accessible primitives used throughout the interface, while Lucide provides the icon system. 

---

## <img src="https://api.iconify.design/lucide:code-2.svg?color=%23ffffff" width="20" height="20" valign="middle"> Development Goals

The project focuses on building a practical booking workflow that is:

* Simple
* Responsive
* Easy to maintain
* Easy to use
* Centralized
* Suitable for both users and administrators

---

## <img src="https://api.iconify.design/lucide:map.svg?color=%23ffffff" width="20" height="20" valign="middle"> Roadmap

Potential future improvements:

* [ ] Persistent database-backed booking management
* [ ] User authentication
* [ ] Admin authentication
* [ ] Booking status workflow
* [ ] Email notifications
* [ ] QR-based booking confirmation
* [ ] Calendar synchronization
* [ ] Booking history
* [ ] Advanced analytics
* [ ] Export booking data
* [ ] Improved role-based access control

---

## <img src="https://api.iconify.design/lucide:github.svg?color=%23ffffff" width="20" height="20" valign="middle"> Repository

[PUKAN223/BookingPCSHSNST-Dom4](https://github.com/PUKAN223/BookingPCSHSNST-Dom4)

---

## <img src="https://api.iconify.design/lucide:info.svg?color=%23ffffff" width="20" height="20" valign="middle"> Project Status

This repository is a project-specific booking application and is currently under development.

The repository is publicly available and is forked from `pie2309/Booking`. 

---

## <img src="https://api.iconify.design/lucide:scale.svg?color=%23ffffff" width="20" height="20" valign="middle"> License

No license is currently specified in the repository.
