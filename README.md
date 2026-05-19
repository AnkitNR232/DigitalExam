# DigitalExam

**DigitalExam** is a web-based digital examination platform designed to allow organisations to create, manage, and deliver online assessments to candidates. The project is currently in its early (scaffolding) stage — no application code has been committed yet.

---

## Table of Contents

- [Project Overview](#project-overview)
- [Intended Features](#intended-features)
- [Repository Structure](#repository-structure)
- [Key Technologies](#key-technologies)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [License](#license)

---

## Project Overview

DigitalExam aims to replace paper-based examinations with a secure, browser-based alternative. Core goals include:

- Providing a portal where **administrators** can create and schedule exams.
- Providing a portal where **candidates** can sit exams under controlled conditions.
- Recording answers and automatically or manually grading them.
- Generating result reports for administrators and candidates.

---

## Intended Features

| Feature | Description |
|---------|-------------|
| User authentication | Role-based login (admin, invigilator, candidate) |
| Exam authoring | Create questions (MCQ, short-answer, essay) with a rich-text editor |
| Exam scheduling | Set start/end windows, time limits, and allowed attempts |
| Candidate portal | Secure, timed exam-taking interface |
| Auto-grading | Instant scoring for objective question types |
| Results & reporting | Exportable grade reports and attempt analytics |
| Anti-cheating controls | Tab-switch detection, full-screen enforcement, randomised question order |

---

## Repository Structure

The project has not been fully scaffolded yet. The intended layout is as follows:

```
DigitalExam/
├── README.md               # This file
├── .gitignore
│
├── backend/                # Server-side application
│   ├── src/
│   │   ├── controllers/    # Route handler logic
│   │   ├── models/         # Database schema / ORM models
│   │   ├── routes/         # Express / API route definitions
│   │   ├── middleware/      # Auth, validation, error-handling middleware
│   │   ├── services/       # Business logic (grading, scheduling, etc.)
│   │   └── utils/          # Shared helper functions
│   ├── tests/              # Unit and integration tests
│   ├── package.json
│   └── ...
│
├── frontend/               # Client-side application
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Route-level page components
│   │   ├── services/       # API client wrappers
│   │   ├── store/          # Global state management
│   │   └── utils/          # Shared front-end helpers
│   ├── public/
│   ├── package.json
│   └── ...
│
├── database/               # Migration scripts and seed data
│   ├── migrations/
│   └── seeds/
│
└── docker-compose.yml      # Local development orchestration
```

---

## Key Technologies

### Back-end

| Technology | Purpose |
|------------|---------|
| **Node.js** | JavaScript runtime for the server |
| **Express.js** | HTTP server and API routing |
| **PostgreSQL** | Primary relational database |
| **Sequelize / TypeORM** | ORM for database access |
| **JWT** | Stateless authentication tokens |
| **Jest** | Unit and integration testing |

### Front-end

| Technology | Purpose |
|------------|---------|
| **React** | Component-based UI library |
| **TypeScript** | Static typing for safer, more maintainable code |
| **Vite** | Fast development build tool |
| **React Router** | Client-side routing |
| **Axios** | HTTP client for API calls |
| **Tailwind CSS** | Utility-first CSS framework |

### Infrastructure / DevOps

| Technology | Purpose |
|------------|---------|
| **Docker / Docker Compose** | Containerised local development |
| **GitHub Actions** | CI/CD pipelines |

> **Note:** The technology choices listed above represent the intended stack. These may change as the project evolves.

---

## Getting Started

> Prerequisites and setup steps will be documented here once the initial application scaffold is committed.

1. **Clone the repository**
   ```bash
   git clone https://github.com/AnkitNR232/DigitalExam.git
   cd DigitalExam
   ```

2. **Install dependencies** *(once backend/frontend scaffolding is added)*
   ```bash
   # Back-end
   cd backend && npm install

   # Front-end
   cd ../frontend && npm install
   ```

3. **Configure environment variables**
   Copy `.env.example` to `.env` in both `backend/` and `frontend/` and fill in the required values.

4. **Start development servers**
   ```bash
   docker-compose up
   ```

---

## Contributing

Contributions are welcome! Please open an issue to discuss what you would like to change before submitting a pull request.

1. Fork the repository.
2. Create a feature branch: `git checkout -b feature/your-feature-name`.
3. Commit your changes: `git commit -m "feat: add your feature"`.
4. Push to the branch: `git push origin feature/your-feature-name`.
5. Open a pull request.

---

## License

This project does not yet have a licence file. One will be added before the first public release.
