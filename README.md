# Employee Payroll Application

## UC-1: Employee Payroll Setup
- **Adding Dependencies**
- **Keeping Confidential and Unnecessary Files in `.gitignore`**
  - **`application.properties`** (Configuration file)

## UC-2: Create Controller and Demonstrate REST Requests
- **Created Different REST Requests:** `GET`, `POST`, `PUT`, `DELETE`
- **Configured MySQL Connection**
- **Ensure the Following Steps to Run the Application** *(Since `application.properties` is not mentioned in the repository)*
- **Path to Create `application.properties`**: src/main/java/resources/application.properties

- **Adding Details in `application.properties`**

```properties
# Database Configuration
spring.datasource.url=your_mysql_URL/Dbname
spring.datasource.username=your_username
spring.datasource.password=your_password
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver

# JPA Configuration
spring.jpa.database-platform=org.hibernate.dialect.MySQLDialect  

``` 

## Section-2 UC-1
- **Introducing DTO for request and Response**
- **Introducing the Model(Entity) to save data in database**
- **DTO add  extra abstraction layer to the user interaction**


## Section-2 UC-2
- **Introducing Service Layer for Business Logic**
- **Adding Abstraction Layer for User request**
- **Now Controller Interact with Service Layer then service layer Respond the user request**

## Section-2 UC-3
- **Temporally Storing Data in List**
- **Adding Employee to the List**
- **Getting Employee from the List**
- **Updating Employee in the List**
- **Deleting Employee from the List**

## Section-3 UC-1
- **Introducing Lombok for Reducing Boilerplate Code**
- **Adding Lombok Dependency in `pom.xml`**
- **Using Lombok Annotations to Generate Getters, Setters, Constructors, etc.**
- **Removing Boilerplate Code from DTO Classes**


## Section-3 UC-2: Introducing Logger for Logging Information

### Configuration Code for Logger
*(I used this in UC-2, but `application.properties` is not included in the GitHub repository. To run this, manually add these lines to `application.properties`.)*

```properties
# Set log level for the application
logging.level.root=INFO
logging.level.com.example=DEBUG

# Log output format
logging.pattern.console=%d{yyyy-MM-dd HH:mm:ss} [%thread] %-5level %logger{36} - %msg%n

# Log file output
logging.file.name=logs/app.log
``` 

### 1. Adding Logger to the Project
- Include the necessary logging dependency in `pom.xml` (if using Maven).

### 2. Using Logger to Log Information
- Implement logging in the application using different log levels:
  - `INFO` – General information about the application's flow.
  - `DEBUG` – Detailed debugging information.
  - `WARN` – Warning messages about potential issues.
  - `ERROR` – Errors that need attention.

### 3. Configuring Logger Settings
- Define the log levels and specify how logs should be formatted.


## Section-3 UC-3
- **I have added the application-prod.properties and application-dev.properties in .gitignore make sure for running log create these files**
- **Path to Create `application-dev.properties`**: src/main/java/resources/application-dev.properties
- **Path to Create `application-prod.properties`**: src/main/java/resources/application-prod.properties
- **Determining Different Logging Based on Application Running**
- **like Different for Dev**
- **like Different for Prod**

## Section-3 UC-4
- **I have added the DB_URL, DB_USERNAME and DB_PASSWORD in Environment Variables**
- Steps to configure the environment variable

# Configure Environment Variables in IntelliJ IDEA

#### **Step 1: Open Run/Debug Configurations**
1. Open **IntelliJ IDEA**.
2. Click on **Run** from the top menu.
3. Select **Edit Configurations**.
   ![Image](https://github.com/user-attachments/assets/83061f90-a3fe-45d3-86be-00abfe918a34)
#### **Step 2: Select Your Application**
1. In the left panel, select your application (e.g., `EmployeePayrollAppApplication`).
2. If no configuration exists, click the **+** button and select **Application**.
   ![Image](https://github.com/user-attachments/assets/540e340d-a191-432d-93b0-2a024dd3a665)
#### **Step 3: Add Environment Variables**
1. Find the **Environment variables** field.
2. Click on the **folder icon** 📁 next to it.
3. A new window titled **Environment Variables** will open.

#### **Step 4: Set Environment Variables**
1. Click the **+ (Add)** button.
2. Enter your key-value pair:
- **Key:** `DB_USERNAME`
- **Value:** `USERNAME`
- **Key:** `DB_PASSWORD`
- **Value:** `yourpassword`
3. Click **OK** to save.

#### **Step 5: Apply and Run**
1. Click **Apply** and then **OK**.
2. Run your application using the **Run** button.



---