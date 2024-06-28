## Getting Started

### Prerequisites

- Java 17
- Maven
- MySQL

### Installation

1. **Clone the repository**

    ```bash
    git clone https://github.com/your-repo/easyshop-capstone.git
    cd easyshop-capstone
    ```

2. **Set up the database**

    Create a MySQL database and user. For example:

    ```sql
    CREATE DATABASE easyshop;
    CREATE USER 'easyshopuser'@'localhost' IDENTIFIED BY 'password';
    GRANT ALL PRIVILEGES ON easyshop.* TO 'easyshopuser'@'localhost';
    FLUSH PRIVILEGES;
    ```

3. **Configure the database connection**

    Update the `application.properties` file in `easyshop-capstone-starter/src/main/resources/` with your database credentials:

    ```properties
    spring.datasource."url"
    spring.datasource.username="username"
    spring.datasource.password="password"
    spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

    spring.jpa.hibernate.ddl-auto=update
    spring.jpa.show-sql=true
    spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL8Dialect
    ```

4. **Build the project**

    Navigate to the root directory of the project and run:

    ```bash
    mvn clean install
    ```

5. **Run the application**

    Navigate to the `easyshop-capstone-starter` module and run:

    ```bash
    cd easyshop-capstone-starter
    mvn spring-boot:run
    ```
