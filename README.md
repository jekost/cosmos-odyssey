# Cosmos Odyssey Web Application

A full-stack web application for seamless interplanetary travel booking.

## Key Features

### Data Handling
- Retrieves travel data from an external API and processes it into a readable format.
- Stores data in a **PostgreSQL database** for easy access via API endpoints.

### Interactive UI
- Users can browse and filter travel options based on **departure, destination, price, company,** and more.

### Shopping & Checkout
- Users can add trips to a **cart** and complete purchases using their **name and surname**.
- Before checkout, the system **verifies if the price list is still valid** to prevent outdated transactions.

### Purchase Records
- All **completed purchases** are stored and accessible via API.

### Data Storage & Expiration Handling
- **Valid travel data** is stored indefinitely.
- The system retains **the last 15 expired price lists** for reference.

## Tech Stack
- **Frontend:** React.js  
- **Backend:** Node.js, Sequelize  
- **Database:** PostgreSQL  
- **Automation:** Cron Job