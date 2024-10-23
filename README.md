# Sky Watch Project

## Introduction
The **Sky Watch** project implements a surveillance system for a 6 km² area using drones controlled by a control center. The system ensures that every point in the area is checked at least every 5 minutes. The drones operate at a speed of 30 km/h with a verification radius of 10 meters, and a 30-minute flight autonomy. The project includes the management of drones, route calculation, and integration with a database to log all relevant operations.

## Key Features
- **Real-Time Surveillance**: Continuous monitoring of a 6 km² area using drones that verify all points every 5 minutes.
- **Autonomous Drone Control**: Drones are fully managed by a control center, which calculates routes, monitors drone status, and handles recharge cycles.
- **Redis Exploitation**: The system grants full coverage with fewer than 9000 drones and uses Redis streams for efficient communication between components.
- **Database Logging**: Information about sessions, drones and potential failures is stored in a PostgreSQL database for analysis and reporting.
- **Optimized Route Calculation**: The system calculates drone routes to minimize the number of drones needed while ensuring consistent area coverage.

## How To Run
- **If a server redis is running on your system**: `sudo service redis-server stop`
- **To start services**: `docker-compose up`
- **To delete containers**: `docker-compose down`

## Further Information
For more details, please refer to the **Sky_watch.pdf** document.
