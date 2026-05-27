# File Explorer Application

A full-stack file explorer application built with Node.js GraphQL API and Angular 15+ client, using functional/reactive programming patterns with streams.

## Architecture

- **Backend**: Node.js + Apollo GraphQL Server
- **Frontend**: Angular 15+ with RxJS streams
- **Styling**: Bootstrap 5
- **Containerization**: Docker

## Features

### API
- GraphQL query for directory listing
- Supports large directories (100,000+ files)
- File metadata: name, path, size, extension, created date, permissions
- Differentiates between files and directories
- Stream-based file system operations for optimal performance

### Client
- Responsive UI with Bootstrap
- Real-time directory navigation
- File and folder selection
- Directory breadcrumb navigation
- Works on all devices

## Project Structure

```
jobjack/
├── backend/
│   ├── src/
│   │   ├── schema/
│   │   ├── resolvers/
│   │   ├── services/
│   │   └── index.ts
│   ├── Dockerfile
│   ├── package.json
│   ├── tsconfig.json
│   └── .dockerignore
├── frontend/
│   ├── src/
│   │   ├── app/
│   │   ├── assets/
│   │   └── main.ts
│   ├── Dockerfile
│   ├── angular.json
│   ├── package.json
│   └── tsconfig.json
├── docker-compose.yml
└── README.md
```

## Getting Started

### Using Docker Compose

```bash
docker-compose up
```

The application will be available at `http://localhost:4200`

### Local Development

#### Backend
```bash
cd backend
npm install
npm run dev
```

#### Frontend
```bash
cd frontend
npm install
ng serve
```

## API Documentation

### GraphQL Query

```graphql
query {
  listDirectory(path: "/path/to/directory") {
    entries {
      name
      fullPath
      size
      extension
      createdAt
      permissions
      isDirectory
    }
  }
}
```

## Technologies

- Apollo GraphQL
- TypeScript
- RxJS (Reactive Extensions)
- Node.js Streams
- Angular
- Bootstrap 5
