# How to Run the MERN Stack Restaurant Reservation Project on a Server

## Prerequisites
- Node.js and npm installed
- MongoDB or your configured database running and accessible
- Environment variables set in `backend/config.env` file:
  - `PORT` - The port number for the backend server (e.g., 5000)
  - `FRONTEND_URL` - The URL where the frontend will be served (e.g., http://localhost:3000)

## Steps

### 1. Build the Frontend
Open a terminal and navigate to the `frontend` directory:
```bash
cd frontend
```
Install dependencies (if not already installed):
```bash
npm install
```
Build the frontend for production:
```bash
npm run build
```
This will create a `dist` folder with the static files.

### 2. Start the Backend Server
Open another terminal and navigate to the `backend` directory:
```bash
cd backend
```
Install dependencies (if not already installed):
```bash
npm install
```
Make sure you have a `config.env` file in the `backend` directory with the required environment variables.

Start the backend server:
```bash
npm start
```
The backend server will serve the frontend static files from the `frontend/dist` folder and API routes.

### 3. Access the Application
Open your browser and go to:
```
http://localhost:<PORT>
```
Replace `<PORT>` with the port number set in your `config.env`.

You should see the frontend application running and be able to use the backend API.

## Notes
- For development, you can run the frontend and backend separately using `npm run dev` in each directory.
- Make sure your database connection string and other sensitive info are correctly set in `config.env`.
- Adjust CORS settings in `backend/app.js` if needed for your deployment environment.
