# Tourism Management System

A modern, full-stack tourism management web application built with Laravel 12, Vue 3, and Inertia.js featuring an orange-themed UI.

## 🚀 Features

### Public-Facing Website

-   **Modern Orange-Themed Home Page** - Clean, responsive layout with hero banner and featured services
-   **Service Marketplace** - Display rentable tourism services (hotels, vehicles, tours)
-   **WhatsApp Integration** - Direct booking via WhatsApp with prefilled messages
-   **Contact Form** - User-friendly contact page with form validation
-   **Responsive Design** - Mobile-friendly interface with modern UI/UX

### Admin Panel

-   **Dashboard** - Statistics overview with cards showing total services, active bookings, categories
-   **Service Management** - CRUD operations for tourism services with image upload
-   **Category Management** - Manage service categories (Hotels, Transport, Experiences)
-   **User Management** - View and manage user accounts with role-based access
-   **Contact Management** - View and respond to customer inquiries

## 🛠 Tech Stack

-   **Backend**: Laravel 12 (PHP 8.3)
-   **Frontend**: Vue 3 with Composition API
-   **Routing**: Inertia.js for seamless SPA experience
-   **Styling**: Tailwind CSS v3+ with custom orange theme
-   **State Management**: Pinia (optional)
-   **Authentication**: Laravel Breeze with Inertia + Vue
-   **File Upload**: Laravel Media Library
-   **Permissions**: Spatie Laravel Permission
-   **Build Tool**: Vite for fast development and hot reload

## 📋 Requirements

-   PHP 8.3+
-   Composer
-   Node.js 18+
-   npm or yarn
-   MySQL/PostgreSQL/SQLite

## 🚀 Installation

1. **Clone the repository**

    ```bash
    git clone <repository-url>
    cd tourism-app
    ```

2. **Install PHP dependencies**

    ```bash
    composer install
    ```

3. **Install Node.js dependencies**

    ```bash
    npm install
    ```

4. **Environment setup**

    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

5. **Configure database**
   Edit `.env` file with your database credentials:

    ```env
    DB_CONNECTION=mysql
    DB_HOST=127.0.0.1
    DB_PORT=3306
    DB_DATABASE=tourism_management
    DB_USERNAME=root
    DB_PASSWORD=
    ```

6. **Run migrations**

    ```bash
    php artisan migrate
    ```

7. **Seed the database (optional)**

    ```bash
    php artisan db:seed
    ```

8. **Build assets**

    ```bash
    npm run build
    ```

9. **Start the development server**
    ```bash
    php artisan serve
    npm run dev
    ```

## 🎨 UI Theme

The application uses a custom orange theme with the following color palette:

-   **Primary Orange**: `#F97316` (bg-orange-500)
-   **Hover Orange**: `#EA580C` (bg-orange-600)
-   **Light Orange**: `#FFEDD5` (bg-orange-100)
-   **Accent Colors**: Various grays and complementary colors

### Design Features

-   Rounded corners (`rounded-2xl`)
-   Hover shadows (`shadow-lg`, `hover:shadow-xl`)
-   Smooth transitions (`transition-all`, `duration-300`)
-   Modern typography with Inter font
-   Responsive grid layouts
-   Card-based design system

## 📱 Pages & Routes

### Public Pages

-   `/` - Home page with hero section and featured services
-   `/rent` - Service marketplace with filtering and search
-   `/contact` - Contact form with business information

### Admin Pages (Protected)

-   `/admin` - Dashboard with statistics
-   `/admin/services` - Service management
-   `/admin/categories` - Category management
-   `/admin/users` - User management

## 🔧 Configuration

### WhatsApp Integration

Update the WhatsApp number in the Rent page component:

```javascript
const phone = "+1234567890"; // Replace with actual WhatsApp number
```

### File Upload

Configure file upload settings in `config/filesystems.php` and ensure the storage directory is writable:

```bash
php artisan storage:link
```

### Permissions

The system uses Spatie Laravel Permission. Configure roles and permissions as needed:

```bash
php artisan permission:create-permission "manage services"
php artisan permission:create-role "admin"
```

## 🚀 Deployment

1. **Production build**

    ```bash
    npm run build
    ```

2. **Optimize for production**

    ```bash
    php artisan config:cache
    php artisan route:cache
    php artisan view:cache
    ```

3. **Set up web server** (Apache/Nginx) pointing to the `public` directory

4. **Configure environment variables** for production

## 📝 License

This project is open-sourced software licensed under the [MIT license](https://opensource.org/licenses/MIT).

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📞 Support

For support and questions, please contact:

-   Email: support@tourism.com
-   Phone: +1 (555) 123-4567

---

**Built with ❤️ using Laravel 12, Vue 3, and Inertia.js**
