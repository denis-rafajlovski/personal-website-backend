# Personal Website – Backend

A headless CMS backend built with Strapi 5 and TypeScript. It provides content management and REST API functionality for my personal portfolio website.

## Tech Stack

- **Strapi 5** – Headless CMS
- **Node.js** – Backend runtime
- **TypeScript** – Static typing
- **PostgreSQL** – Database
- **Cloudinary** – Cloud-based media storage
- **REST API** – Communication with the frontend

## Features

- Content management through Strapi administration panel
- Project creation and management
- Project descriptions and categories
- Featured project management
- Image and media management
- REST API endpoints
- PostgreSQL database integration
- Cloudinary media upload provider
- User permissions and API access management

## Project Structure

```text
personal-website-backend/
├── config/
├── database/
├── public/
├── src/
│   ├── api/
│   └── ...
├── types/
├── package.json
├── package-lock.json
├── tsconfig.json
└── .env.example
```

## Getting Started

### Prerequisites

- Node.js 20 or newer (up to version 26)
- npm
- PostgreSQL database
- Cloudinary account (if using Cloudinary for media storage)

### 1. Clone the repository

```bash
git clone https://github.com/denis-rafajlovski/personal-website-backend.git
```

### 2. Navigate to the project

```bash
cd personal-website-backend
```

### 3. Install dependencies

```bash
npm install
```

### 4. Configure environment variables

Create a `.env` file based on the provided example:

```bash
cp .env.example .env
```

Configure the required values, including:

- Database connection details
- Strapi application secrets
- API security keys
- Cloudinary credentials

Never commit your actual `.env` file.

### 5. Start the development server

```bash
npm run develop
```

### 6. Access the administration panel

```text
http://localhost:1337/admin
```

Create your administrator account when prompted.

## Available Scripts

| Command           | Description                       |
| ----------------- | --------------------------------- |
| `npm run develop` | Start Strapi in development mode  |
| `npm run dev`     | Start Strapi in development mode  |
| `npm run build`   | Build the Strapi application      |
| `npm run start`   | Start production server           |
| `npm run console` | Open Strapi console               |
| `npm run deploy`  | Deploy using Strapi Cloud tooling |
| `npm run upgrade` | Upgrade Strapi                    |

## API

The backend exposes REST API endpoints consumed by the frontend.

Example endpoint:

```http
GET /api/projects?populate=*
```

The API provides project content and associated media, depending on the configured Strapi permissions and content types.

## Media Storage

Cloudinary is configured as an upload provider for managing and delivering media assets.

## Database

The application uses PostgreSQL through the `pg` driver.

Database credentials and connection settings must be configured through environment variables.

## Frontend

This backend powers the personal portfolio frontend.

**Frontend repository:**  
https://github.com/denis-rafajlovski/personal-website-frontend

## Author

**DENIS RAFAJLOVSKI**

- GitHub: https://github.com/denis-rafajlovski
