# ptabc-transaction

### Technical Test on PT. Qtasnim Digital Teknologi: Transaction Website

## Table of Contents

- [Technologies Used](#technologies-used)
- [Installation](#installation)

## Technologies Used

- **Frontend**: HTML, Typescript, Tailwind CSS, React.
- **API Fetching**: TypeScript with RTK Query and Mutation – A reliable library for handling API requests and managing application state.
- **Styling**: Bootstrap 5 and CSS for a customizable UI with a clean, modern look.
- **Icons**: Custom SVG icons for unique and consistent web iconography.
- **Framework**: Laravel (PHP) – A powerful, expressive framework that simplifies backend development with a rich set of tools and features.
- **Build Tools**: Laravel Mix for compiling assets, and Webpack for managing JavaScript and CSS.
- **Database**: MySQL – Used to handle structured data storage and management, with Laravel’s Eloquent ORM facilitating easy database queries and relationships.
- **API Development**: RESTful APIs – Built using Laravel's resources and controllers, with JSON responses to enable frontend and mobile application interaction.
- **Security**: Laravel’s CSRF protection, data validation, and input sanitization – Safeguarding against common vulnerabilities for secure application integrity.

## Installation
Follow these steps to set up this project locally (Make sure you have XAMPP, Laragon, or another local server environment and composer is installed):

1. **Clone this repository:**

   ```
   git clone https://github.com/TapZe/ptabc-transaction.git
   ```

2. **Set up the Backend:**
   1. Navigate to the `backend` folder:
    ```
    cd backend
    ```

   2. Install the required packages using Composer:
    ```
    composer install
    ```

   3. Create a .env file:
   
    Copy the `.env.example` file to create a new `.env` file: 
    ```
    cp .env.example .env
    ```

   4. Generate an Application Key:

    Laravel requires an application key, which is set in the `.env` file. Generate it by running:
    ```
    php artisan key:generate
    ```

   5. Set Up the Database:
   
    Update the .env file with your database credentials (MySQL settings). Example:
    ```
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=your_database_name
    DB_USERNAME=root
    DB_PASSWORD=your_password
    ```
   6. Run a fresh Database Migrations and seeding (Remember to start your mysql environment):
    ```
    php artisan migrate:fresh --seed
    ```

   7. Start the Laravel Server:
    ```
    php artisan serve
    ```
    Your Laravel backend should now be running at http://127.0.0.1:8000.

3. **Set Up the Frontend (React with TypeScript):**
   1. Navigate to the `frontend` folder:
    ```
    cd frontend
    ```

   2. Install the required packages using npm:
    ```
    npm install
    ```

   3. Configure Environment Variables, you can copy or rename `.env.example` to `.env.local` or `.env`:
    ```
    VITE_BASE_URI=http://127.0.0.1:8000/api
    ```

   4. Start the React Development Server:
    ```
    npm start
    ```
    The frontend should now be running at http://localhost:5173.

4. **Set Up Laravel Cors:**
    
    Edit your `.env` file in laravel and edit the value below.
    ```
    FRONTEND_URL=http://localhost:5173
    ```