# Docker Compose Project

This project uses Docker Compose to manage a multi-container application, including a backend and a frontend.

## Prerequisites

Make sure you have the following installed on your system:

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

## Services

The `docker-compose.yml` file defines the following services:

1. **Backend**:
   - Runs a backend application on port `8000`.
   - Image: `lenvigo/backend:v1`

2. **Frontend**:
   - Runs a frontend application on port `80`.
   - Depends on the backend service.
   - Image: `lenvigo/frontend:v1`

## Usage

### 1. Clone the repository

```bash
git clone <repository-url>
cd <repository-folder>
```

### 2. Start the services

Run the following command to start all services:

```bash
docker-compose up
```

This will build and start the containers as defined in the `docker-compose.yml` file.

### 3. Access the application

- Frontend: [http://localhost:80](http://localhost:80)
- Backend: [http://localhost:8000](http://localhost:8000)

### 4. Stop the services

To stop the services, press `Ctrl+C` in the terminal or run:

```bash
docker-compose down
```

## Troubleshooting

- **Error: `yaml: did not find expected key`**  
  Ensure that the `docker-compose.yml` file has consistent indentation (2 spaces per level).

- **Port conflicts**  
  If ports `80` or `8000` are already in use, modify the `ports` section in the `docker-compose.yml` file to use different ports.

## Customization

If you need to customize the services, you can edit the `docker-compose.yml` file to adjust the configurations, such as environment variables, volumes, or ports.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

This `README.md` provides clear instructions for anyone who wants to understand, run, or modify your project.