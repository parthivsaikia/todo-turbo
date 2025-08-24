# Full-Stack To-Do App with Turborepo, React, and Hono

This repository contains the source code for the comprehensive blog series on building a modern full-stack application. The project is built using a monorepo structure managed by Turborepo, a React Router frontend, a Hono backend, and a PostgreSQL database with Prisma ORM.

---

### 📝 Blog Series

This code corresponds to the following articles. You can follow along to build this project from scratch!

- **Part 1: Project Setup and Database Configuration** - [Part 1](https://dev.to/parthiv_saikia_/building-a-full-stack-app-with-turborepo-react-and-hono-part-1-project-setup-and-database-3lpo)

---

### 🚀 Tech Stack

- **Monorepo:** Turborepo
- **Package Manager:** pnpm
- **Frontend:** React with Vite, React Router v7
- **Backend:** Hono on Node.js
- **Database:** PostgreSQL
- **ORM:** Prisma

---

### 🔧 Getting Started

Follow these instructions to get the project up and running on your local machine.

#### Prerequisites

- Node.js (v18 or newer)
- pnpm installed globally (`npm install -g pnpm`)
- A running PostgreSQL instance

#### Installation & Setup

1.  **Clone the repository:**

    ```bash
    git clone [https://github.com/parthivsaikia/todo-turbo.git](https://github.com/parthivsaikia/todo-turbo.git)
    cd todo-turbo
    ```

2.  **Install dependencies:**

    ```bash
    pnpm install
    ```

3.  **Set up environment variables:**
    There is an example environment file in the `packages/db` directory. Copy it to create your own `.env` file.

    ```bash
    cp packages/db/.env.example packages/db/.env
    ```

    Now, open `packages/db/.env` and replace the placeholder values with your actual PostgreSQL database credentials.

4.  **Run database migrations:**
    This command will sync your Prisma schema with your database, creating the necessary tables.

    ```bash
    # From the root directory
    pnpm --filter @repo/db db:migrate:dev
    ```

5.  **Run the development servers:**
    This will start the frontend and backend applications concurrently.

    ```bash
    pnpm dev
    ```

    - The frontend will be available at `http://localhost:5173`
    - The backend will be available at `http://localhost:3000`

---

### 🌳 Branching Strategy

The repository is structured to follow the blog series. The `main` branch will always contain the latest code. Specific branches are tagged for the end-state of each article to make it easy to follow along.

- `part1-setup-complete`: The complete code for Part 1 of the series.
- `part-2-api-complete`: The complete code for Part 2 _(Coming Soon)_.

---

### 📜 Available Scripts

In the root directory, you can run the following main scripts:

- `pnpm dev`: Starts all applications in development mode.
- `pnpm build`: Builds all applications for production.
- `pnpm lint`: Lints all code in the monorepo.
