# Store Application - فروشگاه آنلاین

A comprehensive e-commerce web application built with Spring Boot, featuring a modern Persian/English bilingual interface with complete shopping functionality.

یک اپلیکیشن فروشگاه آنلاین جامع ساخته شده با Spring Boot، دارای رابط کاربری دو زبانه فارسی/انگلیسی مدرن با تمامی قابلیت‌های خرید آنلاین.

---

## 🌟 Features - ویژگی‌ها

### Core Features - ویژگی‌های اصلی

- **🛒 Complete Shopping Experience** - تجربه خرید کامل
  - Product catalog with categories - کاتالوگ محصولات با دسته‌بندی
  - Shopping cart functionality - عملکرد سبد خرید
  - Wishlist management - مدیریت لیست علاقه‌مندی‌ها
  - Order processing and tracking - پردازش و پیگیری سفارش
  - Real-time inventory management - مدیریت موجودی در زمان واقعی

- **👤 User Management** - مدیریت کاربران
  - User registration and authentication - ثبت‌نام و احراز هویت کاربر
  - Role-based access control (User, Admin, Provider) - کنترل دسترسی مبتنی بر نقش
  - JWT-based secure authentication - احراز هویت امن مبتنی بر JWT
  - User profile management - مدیریت پروفایل کاربر

- **🛡️ Admin Dashboard** - داشبورد مدیریت
  - Product management with bulk operations - مدیریت محصولات با عملیات دسته‌ای
  - User management and analytics - مدیریت کاربران و آنالیتیکس
  - Order management and fulfillment - مدیریت و تکمیل سفارشات
  - Message management and support - مدیریت پیام‌ها و پشتیبانی
  - Sales reports and insights - گزارش‌های فروش و بینش‌ها

- **💳 Payment Integration** - یکپارچه‌سازی پرداخت
  - ZarinPal payment gateway - درگاه پرداخت زرین‌پال
  - Secure payment processing - پردازش امن پرداخت
  - Multiple payment methods - روش‌های پرداخت متعدد

- **🌐 Bilingual Support** - پشتیبانی دو زبانه
  - Persian (Farsi) interface - رابط کاربری فارسی
  - English interface - رابط کاربری انگلیسی
  - RTL support for Persian - پشتیبانی راست به چپ برای فارسی
  - Seamless language switching - تعویض زبان بدون مشکل

---

## 🛠️ Technology Stack - پشته فناوری

### Backend - بک‌اند

- **Java 21** - جاوا 21
- **Spring Boot 3.5.4** - اسپرینگ بوت 3.5.4
- **Spring Security** - اسپرینگ سکیوریتی
- **Spring Data JPA** - اسپرینگ دیتا جی‌پی‌ای
- **PostgreSQL 15** - پست‌گرس‌کیوال 15
- **JWT Authentication** - احراز هویت جی‌دبلیو‌تی

### Frontend - فرانت‌اند

- **Thymeleaf** - تایم‌لیف
- **HTML5 & CSS3** - اچ‌تی‌ام‌ال 5 و سی‌اس‌اس 3
- **JavaScript (ES6+)** - جاوااسکریپت
- **Bootstrap 5** - بوت‌استرپ 5
- **Font Awesome** - فونت آوسام

### DevOps & Tools - دواپس و ابزارها

- **Docker & Docker Compose** - داکر و داکر کامپوز
- **Maven 3.9+** - میون 3.9+
- **Swagger/OpenAPI 3.0** - سوگر/اوپن‌ای‌پی‌آی 3.0
- **Lombok** - لامبوک

---

## 🚀 Quick Start - شروع سریع

### Prerequisites - پیش‌نیازها

- Java 21 or higher - جاوا 21 یا بالاتر
- Maven 3.9+ - میون 3.9 یا بالاتر
- Docker & Docker Compose - داکر و داکر کامپوز
- Git - گیت

### Installation - نصب

1. **Clone the repository** - کلون کردن مخزن

   ```bash
   git clone https://github.com/MohammadMehriyari/Java-StoreApp.git
   cd Java-StoreApp
   ```

2. **Start the database** - راه‌اندازی پایگاه داده

   ```bash
   docker-compose up -d
   ```

3. **Configure the application** - پیکربندی اپلیکیشن

   Update `src/main/resources/application.properties` if needed:
   
   ```properties
   spring.datasource.url=jdbc:postgresql://localhost:5432/StoreApplicationDB
   spring.datasource.username=postgres
   spring.datasource.password=postgres
   ```

4. **Run the application** - اجرای اپلیکیشن

   ```bash
   ./mvnw spring-boot:run
   # Or on Windows:
   mvnw.cmd spring-boot:run
   ```

5. **Access the application** - دسترسی به اپلیکیشن
   - **Application**: http://localhost:8080
   - **API Documentation**: http://localhost:8080/swagger-ui.html
   - **Admin Panel**: http://localhost:8080/dashboard

### Default Credentials - اعتبارنامه‌های پیش‌فرض

| Item | Value |
|------|-------|
| **Admin Username** | admin |
| **Admin Password** | admin123 |
| **Database** | StoreApplicationDB (PostgreSQL) |
| **DB Username** | postgres |
| **DB Password** | postgres |

---

## 📁 Project Structure - ساختار پروژه

```
src/
├── main/
│   ├── java/com/storeapplication/
│   │   ├── config/          # Configuration classes and beans
│   │   ├── controller/      # REST and Web controllers
│   │   ├── dto/            # Data Transfer Objects
│   │   ├── filter/         # Security filters and interceptors
│   │   ├── models/         # JPA entities and domain models
│   │   ├── repository/     # Data access layer
│   │   ├── services/       # Business logic layer
│   │   ├── exception/      # Custom exceptions and handlers
│   │   └── utils/          # Utility classes and helpers
│   └── resources/
│       ├── static/         # Static resources (CSS, JS, images)
│       ├── templates/      # Thymeleaf templates
│       └── application.properties  # Application configuration
└── test/                   # Test classes
```

---

## 🔧 Configuration - پیکربندی

### Database Configuration - پیکربندی پایگاه داده

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/StoreApplicationDB
spring.datasource.username=postgres
spring.datasource.password=postgres
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=false
```

### File Upload Configuration - پیکربندی آپلود فایل

```properties
spring.servlet.multipart.max-file-size=10MB
spring.servlet.multipart.max-request-size=50MB
file.upload-dir=/uploads
```

### JWT Configuration - پیکربندی JWT

```properties
jwt.secret=your-secret-key-here
jwt.expiration=86400000
```

---

## 🎯 API Endpoints - نقاط پایانی API

### Authentication - احراز هویت

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/login` | User login |
| POST | `/api/auth/register` | User registration |
| POST | `/api/auth/logout` | User logout |
| POST | `/api/auth/refresh` | Refresh JWT token |

### Products - محصولات

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/products` | Get all products (paginated) |
| GET | `/api/products/{id}` | Get product by ID |
| POST | `/api/products` | Create product (Admin) |
| PUT | `/api/products/{id}` | Update product (Admin) |
| DELETE | `/api/products/{id}` | Delete product (Admin) |
| GET | `/api/products/category/{categoryId}` | Get products by category |

### Categories - دسته‌بندی‌ها

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/categories` | Get all categories |
| GET | `/api/categories/{id}` | Get category by ID |
| POST | `/api/categories` | Create category (Admin) |
| PUT | `/api/categories/{id}` | Update category (Admin) |

### Orders - سفارشات

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/orders` | Get user orders |
| POST | `/api/orders` | Create new order |
| GET | `/api/orders/{id}` | Get order details |
| PUT | `/api/orders/{id}` | Update order status (Admin) |

### Shopping Cart - سبد خرید

| Method | Endpoint | Description |
|--------|----------|-------------|
| GET | `/api/cart` | Get cart items |
| POST | `/api/cart/add` | Add item to cart |
| PUT | `/api/cart/update` | Update cart item |
| DELETE | `/api/cart/remove/{id}` | Remove item from cart |

---

## 🌐 Frontend Pages - صفحات فرانت‌اند

### Public Pages - صفحات عمومی

- **Home** (`/`) - صفحه اصلی
- **Products** (`/products`) - محصولات
- **Categories** (`/categories`) - دسته‌بندی‌ها
- **Product Detail** (`/product/{id}`) - جزئیات محصول
- **About** (`/about`) - درباره ما
- **Contact** (`/contact`) - تماس با ما

### User Pages - صفحات کاربر

- **Login** (`/login`) - ورود
- **Register** (`/register`) - ثبت‌نام
- **Shopping Cart** (`/cart`) - سبد خرید
- **Wishlist** (`/wishlist`) - لیست علاقه‌مندی‌ها
- **Checkout** (`/checkout`) - تسویه حساب
- **Order History** (`/orders`) - تاریخچه سفارشات
- **User Profile** (`/profile`) - پروفایل کاربر

### Admin Pages - صفحات مدیریت

- **Dashboard** (`/dashboard`) - داشبورد
- **Product Management** (`/dashboard/products`) - مدیریت محصولات
- **Category Management** (`/dashboard/categories`) - مدیریت دسته‌بندی‌ها
- **User Management** (`/dashboard/users`) - مدیریت کاربران
- **Order Management** (`/dashboard/orders`) - مدیریت سفارشات
- **Message Management** (`/dashboard/messages`) - مدیریت پیام‌ها
- **Reports** (`/dashboard/reports`) - گزارش‌ها

---

## 🔒 Security Features - ویژگی‌های امنیتی

- **JWT Token Authentication** - احراز هویت توکن JWT
- **Password Encryption (BCrypt)** - رمزگذاری رمز عبور
- **Role-based Access Control (RBAC)** - کنترل دسترسی مبتنی بر نقش
- **CORS Configuration** - پیکربندی CORS
- **Input Validation & Sanitization** - اعتبارسنجی و پاکسازی ورودی
- **SQL Injection Protection** - محافظت در برابر تزریق SQL (JPA Parameterized Queries)
- **HTTPS Support** - پشتیبانی HTTPS
- **Security Headers** - سرفصل‌های امنیتی

---

## 🧪 Testing - تست

### Run Tests - اجرای تست‌ها

```bash
# Run all tests
./mvnw test

# Run specific test class
./mvnw test -Dtest=UserServiceTest

# Run with coverage
./mvnw test jacoco:report
```

### Test Coverage - پوشش تست

- **Unit Tests** - تست‌های واحد برای سرویس‌ها و repo
- **Integration Tests** - تست‌های یکپارچگی برای کنترلرها
- **Security Tests** - تست‌های امنیتی و احراز هویت
- **API Tests** - تست‌های API endpoints

---

## 🐳 Docker Support - پشتیبانی داکر

### Using Docker Compose - استفاده از داکر کامپوز

```bash
# Start all services
docker-compose up -d

# Stop all services
docker-compose down

# View logs
docker-compose logs -f

# Rebuild images
docker-compose up -d --build
```

### Database Container - کانتینر پایگاه داده

| Property | Value |
|----------|-------|
| **Image** | PostgreSQL 15 |
| **Port** | 5432 |
| **Database** | StoreApplicationDB |
| **Username** | postgres |
| **Password** | postgres |
| **Volume** | postgres_data |

---

## 📊 Monitoring & Documentation - نظارت و مستندات

### Swagger/OpenAPI - سوگر/اوپن‌ای‌پی‌آی

- **Swagger UI**: http://localhost:8080/swagger-ui.html
- **OpenAPI JSON**: http://localhost:8080/v3/api-docs
- **OpenAPI YAML**: http://localhost:8080/v3/api-docs.yaml

### Application Monitoring - نظارت اپلیکیشن

- **Health Check**: http://localhost:8080/actuator/health
- **Metrics**: http://localhost:8080/actuator/metrics
- **Environment**: http://localhost:8080/actuator/env

---

## 🤝 Contributing - مشارکت

Contributions are welcome! To contribute:

مشارکت شما را خوشامد می‌گوییم! برای مشارکت:

1. Fork the repository - فورک کردن مخزن
2. Create a feature branch (`git checkout -b feature/AmazingFeature`) - ایجاد شاخه ویژگی
3. Make your changes - ایجاد تغییرات
4. Commit your changes (`git commit -m 'Add some AmazingFeature'`) - ثبت تغییرات
5. Add tests for new features - اضافه کردن تست برای ویژگی‌های جدید
6. Push to the branch (`git push origin feature/AmazingFeature`) - ارسال به شاخه
7. Open a Pull Request - باز کردن درخواست کشیدن

---

## 👥 Authors - نویسندگان

- **Mohammad Mehriyari** - [@MohammadMehriyari](https://github.com/MohammadMehriyari) - Lead Developer
- **Mobin Alizadeh** - [@Mobin Alizadeh](https://github.com/mobin-alz) - Co-Developer

---

## 📝 License - مجوز

This project is open source and available under the MIT License.

---

## 📞 Support - پشتیبانی

If you have any questions, issues, or suggestions, please reach out:

اگر سوالی دارید، مشکلی رو بروبار شده‌اید، یا پیشنهادی دارید، لطفاً تماس بگیرید:

- 📧 **Email**: mohhammadmer@gmail.com
- 🐛 **Issues**: [GitHub Issues](https://github.com/MohammadMehriyari/Java-StoreApp/issues)
- 💬 **Discussions**: [GitHub Discussions](https://github.com/MohammadMehriyari/Java-StoreApp/discussions)

---

## 🎨 Screenshots - تصاویر

*Coming soon - بزودی*

---

**Made with ❤️ by Mohammad Mehriyari**

**ساخته شده با ❤️ توسط محمد مهریاری**
