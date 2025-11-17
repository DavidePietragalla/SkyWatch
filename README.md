# SkyWatch Project 🚀

This project simulates a drone management system, complete with a control center, drone agents, and database integration. It orchestrates drone path planning, task execution, and monitoring, leveraging Redis for inter-process communication and PostgreSQL for persistent data storage. The system addresses the challenge of efficiently managing and coordinating multiple drones to achieve specific objectives, such as area coverage or data collection.

## 🚀 Key Features

- **Drone Path Planning:** The control center generates optimized paths for drones to cover a designated area.
- **Redis Communication:** Uses Redis streams for real-time communication between the control center and drone agents.
- **PostgreSQL Integration:** Stores drone data, session information, and monitoring failures in a PostgreSQL database.
- **Multi-threading:** Employs multi-threading to simulate concurrent drone operations and control center tasks.
- **Failure Monitoring:** Tracks and logs failures, such as missing reports or control center overload, for improved system reliability.
- **Dynamic Drone Management:** Dynamically adjusts the number of drones based on real-time conditions and requirements.
- **Dockerized Deployment:** Provides a Docker Compose configuration for easy setup and deployment of all system components.

## 🛠️ Tech Stack

*   **Backend:** C++
*   **Database:** PostgreSQL (with `libpq-fe.h` client library)
*   **Message Broker:** Redis (with `hiredis` client library)
*   **Containerization:** Docker, Docker Compose
*   **Operating System:** POSIX-compliant (for `unistd.h`)
*   **Build Tools:** (Assumed: `make`, `gcc`, or similar, based on C++ project structure)
*   **Other Libraries:**
    *   `<stdio.h>`, `<stdlib.h>`, `<math.h>`, `<string>`, `<vector>`, `<thread>`, `<chrono>`, `<mutex>`

## 📦 Getting Started

### Prerequisites

- Docker Engine: Make sure you have Docker installed on your system. You can download it from [Docker's official website](https://www.docker.com/get-started).
- Docker Compose: Docker Compose is typically included with Docker Desktop. If you're using Docker Engine separately, ensure Docker Compose is installed.

### Installation

1.  **Clone the repository:**

    ```bash
    git clone <repository_url>
    cd <repository_directory>
    ```

2.  **Create the database directory:**

    ```bash
    mkdir db
    ```

3.  **Start the services using Docker Compose:**

    ```bash
    docker-compose up --build
    ```

    This command builds the Docker images and starts all the defined services (Redis, PostgreSQL, test, and testdrone) in detached mode.

### Running Locally

1.  **Ensure Docker containers are running:** Verify that all containers defined in `docker-compose.yml` are up and running using `docker ps`.

2.  **Access the services:**
    *   PostgreSQL: Accessible on port 5432 (defined in `docker-compose.yml`).  Use the credentials specified in the `docker-compose.yml` file (user, password, database name) to connect.
    *   Redis: Accessible on port 6379 (defined in `docker-compose.yml`).

3.  **Interact with the application:** The `test` and `testdrone` containers likely contain the application logic.  Refer to their respective Dockerfiles (`Dockerfile.test` and `Dockerfile.drone`) and entry points to understand how to interact with them (e.g., through command-line arguments or API calls).
