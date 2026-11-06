# Weerbex – Monorepo Starter

**Weerbex** is a scalable, TypeScript-based monorepo starter built with **Turborepo** and **pnpm workspaces**. It provides an organized foundation for developing and maintaining multiple applications and shared packages within a single repository.

The project is structured to support modular development, reusable components, centralized authentication, database management, and shared TypeScript definitions.

This repository serves as the initial project template for building and extending the Weerbex ecosystem.

---

## Project Structure

The repository follows a monorepo architecture, separating applications from shared packages.

```text
weerbex/
│
├── apps/
│   ├── admin/          # Administrative application
│   ├── dashboard/      # Dashboard application
│   └── web/            # Main web application
│
├── packages/
│   ├── auth/           # Shared authentication logic
│   ├── db/             # Database configuration and utilities
│   ├── types/          # Shared TypeScript types and interfaces
│   └── ui/             # Reusable UI components
│
├── .turbo/             # Turborepo local cache and metadata
├── node_modules/       # Installed dependencies
│
├── .gitignore
├── .npmrc
├── AGENTS.md           # Project-specific development instructions
├── package.json        # Root package configuration
├── pnpm-lock.yaml      # Dependency lockfile
├── pnpm-workspace.yaml # pnpm workspace configuration
├── tsconfig.base.json  # Shared TypeScript configuration
├── turbo.json          # Turborepo task configuration
└── README.md
```

## Applications

The `apps/` directory contains the main applications of the project.

| Application | Description                                                                |
| ----------- | -------------------------------------------------------------------------- |
| `admin`     | Administrative application for managing platform operations and resources. |
| `dashboard` | Dashboard application for presenting and managing platform data.           |
| `web`       | Main web application and primary user-facing interface.                    |

Each application is maintained independently while sharing common packages and configurations from the monorepo.

## Shared Packages

The `packages/` directory contains reusable modules shared across applications.

| Package | Description                                                                   |
| ------- | ----------------------------------------------------------------------------- |
| `auth`  | Centralized authentication logic and shared authentication utilities.         |
| `db`    | Database configuration, connection management, and shared database utilities. |
| `types` | Common TypeScript types, interfaces, and definitions.                         |
| `ui`    | Reusable UI components and shared interface elements.                         |

This architecture helps reduce code duplication, maintain consistency, and simplify application development.

---

## Technology and Tooling

The project uses the following tools and technologies:

- **[Turborepo](https://turborepo.dev/)** – Monorepo build system and task orchestration.
- **[pnpm](https://pnpm.io/)** – Fast, efficient package manager and workspace management.
- **[TypeScript](https://www.typescriptlang.org/)** – Static typing and improved code maintainability.
- **[Node.js](https://nodejs.org/)** – JavaScript runtime environment.
- **[Git](https://git-scm.com/)** – Version control and source code management.

---

## Getting Started

### Prerequisites

Before starting development, make sure you have installed:

- Node.js (compatible with the project configuration).
- pnpm.
- Git.

Enable Corepack if you use it to manage pnpm versions:

```bash
corepack enable
```

### Installation

Clone the repository:

```bash
git clone <repository-url>
```

Navigate to the project directory:

```bash
cd weerbex
```

Install all dependencies:

```bash
pnpm install
```

### Environment Configuration

Configure the environment variables required by each application and shared package.

Keep sensitive credentials and API keys in environment files and never commit secrets to the repository.

---

## Development

Turborepo allows you to run development tasks across the monorepo.

Start the development environment:

```bash
pnpm exec turbo dev
```

To start a specific application, use its workspace package name:

```bash
pnpm --filter <package-name> dev
```

For example, if the application's workspace package name is `web`:

```bash
pnpm --filter web dev
```

---

## Building

Build all applications and packages:

```bash
pnpm exec turbo build
```

Build a specific application or package:

```bash
pnpm exec turbo build --filter=<package-name>
```

Turborepo automatically manages task execution and caching according to the configuration defined in `turbo.json`.

---

## Project Configuration

Several files manage the monorepo configuration:

| File                  | Purpose                                                            |
| --------------------- | ------------------------------------------------------------------ |
| `package.json`        | Root scripts, dependencies, and project metadata.                  |
| `pnpm-workspace.yaml` | Defines the workspace directories.                                 |
| `pnpm-lock.yaml`      | Locks dependency versions for consistent installations.            |
| `turbo.json`          | Defines and configures Turborepo tasks and caching.                |
| `tsconfig.base.json`  | Provides shared TypeScript compiler settings.                      |
| `.npmrc`              | Defines pnpm and npm configuration options.                        |
| `AGENTS.md`           | Contains project-specific instructions and development guidelines. |

---

## Development Philosophy

Weerbex follows a modular and maintainable development approach:

- **Modularity:** Applications and shared packages are separated by responsibility.
- **Reusability:** Common functionality is maintained in shared packages.
- **Scalability:** New applications and packages can be added without restructuring the entire repository.
- **Consistency:** Shared configurations help maintain consistent development practices.
- **Maintainability:** Centralized dependencies and workspace management simplify project maintenance.

---

## Useful Resources

- [Turborepo Documentation](https://turborepo.dev/docs)
- [pnpm Documentation](https://pnpm.io/motivation)
- [TypeScript Documentation](https://www.typescriptlang.org/docs/)
- [Node.js Documentation](https://nodejs.org/docs/)

---

**Weerbex – Initial Project Template**

A modular foundation designed for scalable application development.
