# Laravel REST API with Sanctum  

This is a simple REST API using Laravel Sanctum for token-based authentication.  

## Setup  

1. **Configure Environment:**  
   - Rename `.env.example` to `.env`.  
   - Add your database information in the `.env` file:  
     ```env  
     DB_CONNECTION=mysql  
     DB_HOST=127.0.0.1  
     DB_PORT=3306  
     DB_DATABASE=laravel_sanctum  
     DB_USERNAME=root  
     DB_PASSWORD=12345678  
     ```  

2. **Run the Server:**  
   Start the development server with:  
   ```bash  
   php artisan serve  
   ```  

## API Routes  

### Public Routes  

1. **Login**  
   - **Endpoint:** `POST /api/login`  
   - **Body:**  
     ```json  
     { "email": "example@example.com", "password": "password" }  
     ```  

2. **Register**  
   - **Endpoint:** `POST /api/register`  
   - **Body:**  
     ```json  
     { "name": "John Doe", "email": "john@example.com", "password": "password", "password_confirmation": "password" }  
     ```  

### Protected Route (Requires Authentication)  

1. **Logout**  
   - **Endpoint:** `POST /api/logout`  

