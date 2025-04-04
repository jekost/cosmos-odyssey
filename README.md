# Cosmos Odyssey Web Application
A full-stack web application for seamless interplanetary travel booking. Developed for $${\color{red}Up}{\color{black}Time}$$, Spring 2025

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
- **Frontend:** React + Vite  
- **Backend:** Node.js, Sequelize  
- **Database:** PostgreSQL  
- **Automation:** Cron Job

## Setup Guide using Git & Docker
- Clone this repository: `git clone https://github.com/jekost/cosmos-odyssey`
- Go into the freshly cloned folder: `cd ./cosmos-odyssey`
- Run the entire application using `docker-compose up --build`
- Wait ~5 minutes while it processes and ~1 minute until the database gets populated with some data. 

## Access points
- Access the UI at `http://localhost:5173`
- All current and last 15 pricelists are available here: `http://localhost:5000/api/pricelists`
- All flights recorded during that time are here: `http://localhost:5000/api/travels`
- And all purchases are accessible here: `http://localhost:5000/api/reservations`

## Limitations
- In order to make the setup as efficient as possible, I had to include `.env` files as well. I understand this is not good practice and this is strictly made for the ease of setup.
- `UUIDs` from the given `API` are not utilised to perfection, as I couldn't find the proper logic behind the implementation. For example, each example of the planet `Earth` does not always have the same `UUID`, and there seems to be no similarity between the `UUIDs` between different pricelists.
- Currently the data retrieval is automated using Cron Job. This could very well be replaced with some checker that looks right after the current pricelist expires, however that may not always be the best case.



Seperate front-end and back-end (+db) repositories:

https://github.com/jekost/cosmos-odyssey-frontend

https://github.com/jekost/cosmos-odyssey-backend

### Jan Erik Köst
### jan.erik.kost@hotmail.com
