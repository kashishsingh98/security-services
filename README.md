
This project is a production-grade Identity & Access Management (IAM) system built with Java & Spring Boot.
It provides secure authentication, authorization, and user management for modern SaaS and enterprise applications.

The system supports:

JWT-based authentication
OAuth2 social login
Role-Based Access Control (RBAC)
Multi-tenant support
API key authentication
Audit logging
Rate limiting
Token management

🚀 Features
  🔑 Authentication
  
    -Email & password login
    -JWT + Refresh Token flow
    -OAuth2 (Google / GitHub)
    -Password reset & email verification
    
  🛡 Authorization
  
    -Role-Based Access Control (ADMIN, USER, MANAGER)
    -Permission-based APIs
    -Tenant-level isolation

  📊 Security
  
    -API Key authentication
    -Rate limiting
    -Token revocation
    -Session management
  
  📝 Audit & Monitoring
  
    -Login activity tracking
    -User action logs
    -Security event logs

🏗 Architecture
    Client
       |
    API Gateway
       |
    -------------------------
    | Auth Service         |
    | User Service         |
    | Audit Service        |
    -------------------------
       |
     Databases (MySQL, Redis)


Auth Service: Authentication, JWT, OAuth2
User Service: User profiles, roles, tenants
Audit Service: Logs & security events
API Gateway: Routing & security layer

🧰 Tech Stack
  Category	Technology
  Backend	Java, Spring Boot
  Security	Spring Security, JWT, OAuth2
  Database	MySQL
  Cache	Redis
  Messaging	Kafka (optional)
  API Docs	Swagger
  DevOps	Docker, Docker Compose
  Build	Maven
📡 API Endpoints (Sample)
    -Auth
    POST /auth/register
    POST /auth/login
    POST /auth/refresh
    POST /auth/logout
    
    -OAuth
    GET /oauth2/authorize/google
    GET /oauth2/authorize/github
    
    -Users
    GET /users/{id}
    PUT /users/{id}
    DELETE /users/{id}
    
    -Admin
    POST /admin/create-role
    POST /admin/assign-role

🔐 JWT Flow

    User logs in
    
    Server issues:
    
    Access Token
    
    Refresh Token
    
    Access token used for API calls
    
    Refresh token generates new access token
    
    Tokens can be revoked

🗄 Database Schema (Simplified)
  -Users
  id, email, password, tenant_id, status
  -Roles
  id, name
  -Permissions
  id, name
  -Audit Logs
  id, user_id, action, timestamp, ip

🛠 How to Run Locally

  1. Clone the Repo
  git clone https://github.com/your-username/java-iam-security-service.git
  cd java-iam-security-service
  2. Start Services
  docker-compose up -d
  3. Run Spring Boot Apps
  mvn spring-boot:run
  4. Open Swagger
  http://localhost:8080/swagger-ui.html

🧪 Testing

    -Unit tests for auth & security
    -API testing with Postman
    -OAuth login flow testing

📈 Future Enhancements

  -2FA (TOTP)
  -Passwordless login
  -Device-based security
  -AI-based anomaly detection
  -Kubernetes deployment

👨‍💻 Author

Kashish Singh
Backend Engineer | Java | Spring Boot | Kafka | Microservices

