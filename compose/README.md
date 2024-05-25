# Docker Compose Configuration for Data Analysis with Metabase, PostgreSQL, and MongoDB

This Docker Compose file sets up a local data analysis environment using Metabase for visualization, PostgreSQL as a relational database, and MongoDB as a NoSQL database. The setup is designed to facilitate easy data analysis and visualization, making it suitable for development and testing purposes.

## Services Defined in Docker Compose

![image](https://github.com/rezkmike-study/starbuck-analysis/assets/156246227/9ee2d118-9ea2-40d9-b99b-f34900a3c4d1)

1. **Metabase:**
   - **Image:** metabase/metabase:latest
   - **Ports:** Exposes Metabase on port 3000.
   - **Environment:** Configured to connect to PostgreSQL.
   - **Volumes:** Maps `./metabase` for Metabase data persistence.
   - **Secrets:** Uses external files for database username and password.

2. **PostgreSQL:**
   - **Image:** postgres:latest
   - **Environment:** Uses secrets for setting up the user, password, and database name.
   - **Networks:** Connected to a custom network for internal communication.

3. **MongoDB:**
   - **Image:** mongo:latest
   - **Ports:** Exposes MongoDB on port 27017.
   - **Volumes:** Maps `./mongo-data` for data persistence and `./directory.csv` to a temporary location inside the container.
   - **Environment:** Sets up MongoDB with a root user and password for initialization.

## Network Configuration

- **Network Name (`net`):** Custom network with a subnet configuration to facilitate communication between containers without exposing them to the outside world.

## Secrets Management

- **Secrets:** Database username and password are managed using Docker secrets to enhance security by not exposing sensitive information directly in the Docker Compose file.

## Prerequisites

Before running this Docker Compose setup, ensure you have Docker and Docker Compose installed on your system. Additionally, create the `db_user.txt` and `db_password.txt` files in the directory where you will run the Docker Compose file, containing your database user and password respectively.

## Running the Docker Compose

1. **Clone the Repository:**
   - Ensure you have all the necessary files, including the Docker Compose file and any configuration files or scripts referenced within it.

2. **Start the Environment:**
   - Open a terminal and navigate to the directory containing your `docker-compose.yml`.
   - Run the following command to start all services:
     ```bash
     docker-compose up -d
     ```
   - This will pull the required Docker images, create the defined networks and secrets, and start the services in detached mode.

3. **Accessing Metabase:**
   - Once the services are up, you can access Metabase at `http://localhost:3000` to configure your dashboard and connect to the PostgreSQL database.

4. **Stopping the Environment:**
   - To stop all services, use the following command:
     ```bash
     docker-compose down
     ```

## Data Persistence

The volumes defined in the Docker Compose ensure that data in PostgreSQL and MongoDB is persisted across container restarts. Make sure the paths in the volume mappings are accessible and have the appropriate permissions.

This README file offers a comprehensive guide on how the Docker Compose environment is structured and provides instructions for setup and usage. Adjust paths and configurations as necessary to fit your specific deployment needs.
