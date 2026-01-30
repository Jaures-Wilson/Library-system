# Library Management System - Java Enterprise Edition

A comprehensive web-based library management system developed using Java Enterprise Edition (JEE) technologies. This application provides complete management of library resources including book cataloging, borrowing operations, returns, and user management through a modern web interface.

## Table of Contents

- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [System Architecture](#system-architecture)
- [Technology Stack](#technology-stack)
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
  - [Windows Installation](#windows-installation)
  - [macOS Installation](#macos-installation)
  - [Ubuntu/Linux Installation](#ubuntu-linux-installation)
- [Configuration and Setup](#configuration-and-setup)
- [Database Schema](#database-schema)
- [Application Structure](#application-structure)
- [User Guide](#user-guide)
- [Security Features](#security-features)
- [API Documentation](#api-documentation)
- [Development Team](#development-team)
- [Troubleshooting](#troubleshooting)
- [Future Enhancements](#future-enhancements)
- [License](#license)

---

## Project Overview

### Context and Purpose

This Library Management System was developed as an academic project at the École Nationale Supérieure Polytechnique de Douala (ENSPD) in Cameroon. The application addresses the need for modern digital library management in educational institutions, replacing traditional manual systems with an efficient, web-based solution.

### Educational Objectives

The project demonstrates practical implementation of:
- Object-Oriented Programming principles in Java
- Enterprise-level web application development
- Database design and management
- Multi-tier architecture implementation
- UML modeling and software engineering methodologies
- Team collaboration and project management

### Problem Statement

Traditional library management at ENSPD relied on manual processes:
- Paper-based book cataloging
- Manual borrowing and return registration
- Limited ability to track borrowing history
- Difficult search and inventory management
- No real-time availability status
- Data security and integrity concerns

This system provides a comprehensive digital solution to these challenges.

---

## Key Features

### Book Management
- **Cataloging**: Add new books with complete metadata (ISBN, title, author, publication year, copies)
- **Inventory Control**: Real-time tracking of available and borrowed books
- **CRUD Operations**: Create, Read, Update, and Delete book records
- **Search Functionality**: Advanced search by title, author, ISBN, or category
- **Category Management**: Organize books by subject categories (Mathematics, Physics, Literature, etc.)
- **Availability Status**: Instant visibility of book availability

### Borrowing Operations
- **Loan Registration**: Record new book borrowings with borrower details
- **Return Processing**: Process book returns and update availability
- **Borrowing History**: Complete historical record of all transactions
- **Due Date Management**: Track borrowing and expected return dates
- **Late Return Tracking**: Identify overdue books and borrowers
- **User Association**: Link borrowings to specific library members

### Reader Management
- **Member Registration**: Add new library members with personal information
- **Profile Management**: Update and maintain reader profiles
- **Borrowing History**: View complete borrowing history per reader
- **Membership Status**: Track active and inactive memberships
- **Contact Information**: Store and manage member contact details

### Librarian Management
- **Staff Accounts**: Create and manage librarian user accounts
- **Role-Based Access**: Different permission levels for staff members
- **Activity Tracking**: Monitor librarian actions and operations
- **Authentication**: Secure login system for authorized personnel

### Administrative Features
- **Dashboard**: Overview of library statistics and recent activities
- **Reporting**: Generate reports on borrowing trends and book utilization
- **User Management**: Comprehensive control over system users
- **Audit Trail**: Logging of all critical system operations

---

## System Architecture

### Multi-Tier Architecture

The application follows the Model-View-Controller (MVC) architectural pattern with clear separation of concerns across multiple tiers:

```
+---------------------------+
|   Presentation Layer      |
|   (Web Browser)           |
+-------------+-------------+
              |
              | HTTP/HTTPS
              v
+-------------+-------------+
|   View Layer              |
|   (JSP, HTML, CSS, JS)    |
+-------------+-------------+
              |
              v
+-------------+-------------+
|   Controller Layer        |
|   (Servlets, Filters)     |
+-------------+-------------+
              |
              v
+-------------+-------------+
|   Business Logic Layer    |
|   (EJB, Services)         |
+-------------+-------------+
              |
              v
+-------------+-------------+
|   Data Access Layer       |
|   (JPA, DAO)              |
+-------------+-------------+
              |
              v
+-------------+-------------+
|   Database Layer          |
|   (SQLite)                |
+---------------------------+
```

### Layer Responsibilities

**Presentation Layer**:
- Client-side interface rendering
- User interaction handling
- Browser-based access

**View Layer**:
- JSP pages for dynamic content generation
- HTML structure
- CSS styling
- JavaScript interactivity
- JSTL for simplified JSP coding

**Controller Layer**:
- Servlet request processing
- Request routing
- Session management
- Security filters
- Authentication filters

**Business Logic Layer**:
- Core application logic
- Business rule enforcement
- Service orchestration
- Transaction management

**Data Access Layer**:
- Database operations
- CRUD implementations
- Query execution
- Data mapping

**Database Layer**:
- Data persistence
- Relational data storage
- Transaction support

---

## Technology Stack

### Frontend Technologies

| Technology | Version | Purpose |
|------------|---------|---------|
| **JSP** | 2.3+ | Dynamic page generation |
| **JSTL** | 1.2+ | JSP tag library for simplified coding |
| **HTML5** | - | Page structure and content |
| **CSS3** | - | Styling and layout |
| **JavaScript** | ES6+ | Client-side interactivity |

### Backend Technologies

| Technology | Version | Purpose |
|------------|---------|---------|
| **Java** | JDK 17+ | Core programming language |
| **Servlets** | 5.0+ | HTTP request handling |
| **EJB** | 4.0+ | Business logic encapsulation |
| **JPA** | 3.0+ | Object-relational mapping |
| **JPQL** | - | Object-oriented query language |

### Database

| Technology | Version | Purpose |
|------------|---------|---------|
| **SQLite** | 3.x | Lightweight relational database |

### Development Tools

| Tool | Purpose |
|------|---------|
| **Eclipse IDE** | Integrated development environment |
| **Apache Tomcat** | Application server (version 10.0+) |
| **Maven** | Build automation and dependency management |
| **Git** | Version control |
| **StarUML** | UML diagram creation |
| **SQLiteStudio** | Database management and SQL editing |
| **Visual Studio Code** | Additional code editing |

---

## System Requirements

### Minimum Requirements

**Hardware**:
- Processor: Dual-core 2.0 GHz or higher
- RAM: 4 GB minimum
- Storage: 500 MB for application, additional space for database
- Network: Required for multi-user access

**Software**:
- Operating System: Windows 10+, macOS 10.15+, Ubuntu 20.04+ or compatible Linux
- Java JDK: Version 17 or higher
- Web Browser: Chrome 90+, Firefox 88+, Safari 14+, or Edge 90+

### Recommended Requirements

**Hardware**:
- Processor: Quad-core 2.5 GHz or higher
- RAM: 8 GB or more
- Storage: 2 GB free space
- Network: Stable connection for concurrent users

**Software**:
- Java JDK: Latest LTS version (21 recommended)
- Apache Tomcat: Version 10.1 or newer
- Modern web browser with JavaScript enabled

---

## Installation Guide

### Prerequisites

Before installation, ensure you have:
1. Java Development Kit (JDK) 17 or higher installed
2. Apache Tomcat 10.0 or higher downloaded and extracted
3. Eclipse IDE for Enterprise Java and Web Developers
4. Git for version control (optional but recommended)

### Windows Installation

#### Step 1: Install Java JDK

1. **Download JDK**:
   - Visit: https://www.oracle.com/java/technologies/downloads/
   - Download JDK 17 or higher (e.g., jdk-17_windows-x64_bin.exe)

2. **Install JDK**:
   - Run the installer
   - Accept default installation path or choose custom location
   - Complete installation wizard

3. **Verify Installation**:
   ```cmd
   java -version
   ```
   Expected output: `java version "17.0.x"` or higher

4. **Set JAVA_HOME Environment Variable**:
   - Right-click "This PC" → Properties
   - Advanced system settings → Environment Variables
   - Under System Variables, click "New"
   - Variable name: `JAVA_HOME`
   - Variable value: `C:\Program Files\Java\jdk-17` (your JDK path)
   - Click OK

5. **Update PATH**:
   - Edit Path variable
   - Add: `%JAVA_HOME%\bin`
   - Click OK

#### Step 2: Install Apache Tomcat

1. **Download Tomcat**:
   - Visit: https://tomcat.apache.org/download-10.cgi
   - Download "32-bit/64-bit Windows Service Installer" (apache-tomcat-10.x.x.exe)
   - OR download ZIP archive for manual installation

2. **Install Tomcat** (Installer method):
   - Run the installer
   - Choose installation directory (e.g., `C:\apache-tomcat-10.1.40`)
   - Set HTTP port (default: 8080)
   - Set admin username and password
   - Complete installation

3. **Install Tomcat** (Manual/ZIP method):
   - Extract ZIP to desired location (e.g., `C:\apache-tomcat-10.1.40`)
   - No further installation needed

4. **Verify Tomcat**:
   - Navigate to Tomcat's bin directory
   - Run `startup.bat`
   - Open browser: http://localhost:8080
   - You should see Tomcat welcome page
   - Stop server: run `shutdown.bat`

#### Step 3: Install Eclipse IDE

1. **Download Eclipse**:
   - Visit: https://www.eclipse.org/downloads/
   - Download "Eclipse IDE for Enterprise Java and Web Developers"

2. **Install Eclipse**:
   - Run the installer
   - Select "Eclipse IDE for Enterprise Java and Web Developers"
   - Choose installation folder
   - Complete installation

3. **Launch Eclipse**:
   - Choose a workspace directory
   - Eclipse opens with Java EE perspective

#### Step 4: Clone/Download the Project

**Option A: Using Git**:
```cmd
git clone https://github.com/your-repository/library-management-system.git
cd library-management-system
```

**Option B: Manual Download**:
- Download project ZIP from repository
- Extract to desired location
- Remember the extraction path

#### Step 5: Import Project into Eclipse

1. Launch Eclipse
2. Navigate: **File → Import**
3. Select: **General → Existing Projects into Workspace**
4. Click **Next**
5. Click **Browse** and navigate to project folder
6. Select the project: `projetBIBLIOTHEQUE(POO)`
7. Ensure project is checked
8. Click **Finish**

#### Step 6: Configure Tomcat in Eclipse

1. **Open Servers View**:
   - Window → Show View → Servers
   - If no servers exist, click: "No servers are available. Click this link to create a new server..."

2. **Add Tomcat Server**:
   - Select: **Apache → Tomcat v10.0 Server**
   - Click **Next**
   - Click **Browse** and select your Tomcat installation directory
   - Click **Finish**

3. **Configure Server**:
   - Double-click the server in Servers view
   - Set deployment location
   - Save configuration (Ctrl+S)

#### Step 7: Add Project to Server

1. In **Servers** tab, right-click on Tomcat server
2. Select **Add and Remove...**
3. Move project from "Available" to "Configured"
4. Click **Finish**

#### Step 8: Configure Database

1. **Locate Database File**:
   - Navigate to project folder
   - Find `bibliotheque.db` (SQLite database file)
   - Ensure it's in the correct location (usually in project root or `WEB-INF` folder)

2. **Verify Database Structure** (optional):
   - Install SQLiteStudio
   - Open `bibliotheque.db`
   - Verify tables exist: LIVRE, LECTEUR, EMPRUNT, UTILISATEUR, CATEGORIE

#### Step 9: Run the Application

1. **Start Tomcat Server**:
   - Right-click server in Servers tab
   - Select **Start**
   - Wait for server to start (console shows "Server startup complete")

2. **Run Application**:
   - Navigate: `src → main → java → servlet → DemarrerLaBibliothequeServlet.java`
   - Right-click on the file
   - Select: **Run As → Run on Server**
   - Select your Tomcat server
   - Click **Finish**

3. **Access Application**:
   - Browser automatically opens to: http://localhost:8080/projetBIBLIOTHEQUE(POO)
   - You should see the login page

#### Step 10: Login

**Default Credentials Format**:
- **Username**: Your student ID (matricule)
- **Password**: Student ID + Full Name (no spaces)
- **Example**: 
  - Username: `22G00249`
  - Password: `22G00249MBOUMELATIFFAJAURESWILSON`

---

### macOS Installation

#### Step 1: Install Java JDK

1. **Download JDK**:
   - Visit: https://www.oracle.com/java/technologies/downloads/
   - Download macOS version (e.g., jdk-17_macos-x64_bin.dmg)

2. **Install JDK**:
   - Open the DMG file
   - Run the installer package
   - Follow installation wizard

3. **Verify Installation**:
   ```bash
   java -version
   javac -version
   ```

4. **Set JAVA_HOME** (add to `~/.bash_profile` or `~/.zshrc`):
   ```bash
   export JAVA_HOME=$(/usr/libexec/java_home -v 17)
   export PATH=$JAVA_HOME/bin:$PATH
   ```
   
   Reload:
   ```bash
   source ~/.bash_profile  # or source ~/.zshrc
   ```

#### Step 2: Install Apache Tomcat

1. **Download Tomcat**:
   - Visit: https://tomcat.apache.org/download-10.cgi
   - Download "tar.gz" archive

2. **Extract Tomcat**:
   ```bash
   cd ~/Downloads
   tar -xzf apache-tomcat-10.x.x.tar.gz
   sudo mv apache-tomcat-10.x.x /usr/local/tomcat
   ```

3. **Set Permissions**:
   ```bash
   sudo chmod +x /usr/local/tomcat/bin/*.sh
   ```

4. **Test Tomcat**:
   ```bash
   /usr/local/tomcat/bin/startup.sh
   ```
   - Open: http://localhost:8080
   - Stop: `/usr/local/tomcat/bin/shutdown.sh`

#### Step 3: Install Eclipse

1. **Download Eclipse**:
   - Visit: https://www.eclipse.org/downloads/
   - Download "Eclipse IDE for Enterprise Java and Web Developers" for macOS

2. **Install**:
   - Open DMG file
   - Drag Eclipse to Applications folder
   - Launch Eclipse from Applications

#### Steps 4-10: Same as Windows

Follow steps 4-10 from the Windows installation guide. The process is identical once Eclipse is installed.

---

### Ubuntu/Linux Installation

#### Step 1: Install Java JDK

```bash
# Update package index
sudo apt update

# Install OpenJDK 17
sudo apt install openjdk-17-jdk -y

# Verify installation
java -version
javac -version

# Set JAVA_HOME (add to ~/.bashrc)
echo 'export JAVA_HOME=/usr/lib/jvm/java-17-openjdk-amd64' >> ~/.bashrc
echo 'export PATH=$JAVA_HOME/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

#### Step 2: Install Apache Tomcat

```bash
# Download Tomcat
cd /tmp
wget https://dlcdn.apache.org/tomcat/tomcat-10/v10.1.40/bin/apache-tomcat-10.1.40.tar.gz

# Extract to /opt
sudo tar xzvf apache-tomcat-10.1.40.tar.gz -C /opt

# Create symbolic link
sudo ln -s /opt/apache-tomcat-10.1.40 /opt/tomcat

# Set permissions
sudo chmod +x /opt/tomcat/bin/*.sh

# Test Tomcat
/opt/tomcat/bin/startup.sh
```

Open browser: http://localhost:8080

Stop Tomcat:
```bash
/opt/tomcat/bin/shutdown.sh
```

#### Step 3: Install Eclipse

```bash
# Download Eclipse Installer
cd ~/Downloads
wget https://www.eclipse.org/downloads/download.php?file=/oomph/epp/2024-12/R/eclipse-inst-jre-linux64.tar.gz -O eclipse-installer.tar.gz

# Extract
tar -xzf eclipse-installer.tar.gz

# Run installer
cd eclipse-installer
./eclipse-inst

# Select "Eclipse IDE for Enterprise Java and Web Developers"
# Choose installation directory
# Complete installation
```

#### Steps 4-10: Same as Windows

Follow steps 4-10 from the Windows installation guide.

---

## Configuration and Setup

### Project Structure Verification

After importing, verify the project structure:

```
projetBIBLIOTHEQUE(POO)/
├── src/
│   └── main/
│       ├── java/
│       │   ├── dao/              # Data Access Objects
│       │   ├── model/            # Entity classes
│       │   ├── service/          # Business logic
│       │   └── servlet/          # Controllers
│       └── webapp/
│           ├── WEB-INF/
│           │   ├── web.xml      # Deployment descriptor
│           │   └── lib/         # JAR dependencies
│           ├── css/             # Stylesheets
│           ├── js/              # JavaScript files
│           ├── images/          # Image resources
│           └── *.jsp            # JSP pages
└── bibliotheque.db              # SQLite database
```

### Configuring as Dynamic Web Project

If project is not recognized as a Dynamic Web Project:

1. Right-click project → **Properties**
2. Navigate to **Project Facets**
3. Enable:
   - **Dynamic Web Module** (version 5.0)
   - **Java** (version 17)
4. Click **Apply and Close**

### Database Configuration

The application uses SQLite with the following configuration:

**Database File**: `bibliotheque.db`

**Location**: Project root directory or `WEB-INF` folder

**Connection**: Automatically configured via JDBC

If database file is missing or corrupted:
1. Create new SQLite database
2. Execute schema creation scripts
3. Update database path in configuration

---

## Database Schema

### Entity Relationship Overview

The database consists of five primary tables:

1. **LIVRE** (Books)
2. **LECTEUR** (Readers/Members)
3. **EMPRUNT** (Borrowings)
4. **UTILISATEUR** (System Users)
5. **CATEGORIE** (Categories)

### Table Structures

#### LIVRE Table

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique book identifier |
| isbn | VARCHAR(20) | UNIQUE, NOT NULL | International Standard Book Number |
| titre | VARCHAR(200) | NOT NULL | Book title |
| auteur | VARCHAR(100) | NOT NULL | Author name |
| annee_publication | INTEGER | | Publication year |
| nombre_exemplaires | INTEGER | DEFAULT 1 | Total copies available |
| exemplaires_disponibles | INTEGER | DEFAULT 1 | Currently available copies |
| id_categorie | INTEGER | FOREIGN KEY | Reference to CATEGORIE table |

#### LECTEUR Table

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique reader identifier |
| nom | VARCHAR(100) | NOT NULL | Reader's full name |
| adresse | VARCHAR(200) | | Residential address |
| numero_cni | VARCHAR(50) | UNIQUE | National ID number |
| telephone | VARCHAR(20) | | Contact phone number |
| email | VARCHAR(100) | | Email address |
| date_inscription | DATE | DEFAULT CURRENT_DATE | Registration date |
| statut | VARCHAR(20) | DEFAULT 'ACTIF' | Account status |

#### EMPRUNT Table

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique borrowing identifier |
| id_livre | INTEGER | FOREIGN KEY, NOT NULL | Reference to LIVRE |
| id_lecteur | INTEGER | FOREIGN KEY, NOT NULL | Reference to LECTEUR |
| id_bibliothecaire | INTEGER | FOREIGN KEY | Reference to UTILISATEUR |
| date_emprunt | DATE | NOT NULL | Borrowing date |
| date_retour_prevue | DATE | NOT NULL | Expected return date |
| date_retour_effective | DATE | | Actual return date |
| statut | VARCHAR(20) | DEFAULT 'EN_COURS' | Borrowing status |

#### UTILISATEUR Table

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique user identifier |
| matricule | VARCHAR(50) | UNIQUE, NOT NULL | Employee/Student ID |
| nom | VARCHAR(100) | NOT NULL | Full name |
| mot_de_passe | VARCHAR(255) | NOT NULL | Hashed password |
| role | VARCHAR(20) | DEFAULT 'BIBLIOTHECAIRE' | User role |
| date_creation | TIMESTAMP | DEFAULT CURRENT_TIMESTAMP | Account creation date |

#### CATEGORIE Table

| Column | Type | Constraints | Description |
|--------|------|-------------|-------------|
| id | INTEGER | PRIMARY KEY, AUTOINCREMENT | Unique category identifier |
| nom | VARCHAR(100) | UNIQUE, NOT NULL | Category name |
| description | TEXT | | Category description |

### Relationships

- **LIVRE** → **CATEGORIE**: Many-to-One (Many books belong to one category)
- **EMPRUNT** → **LIVRE**: Many-to-One (Many borrowings for one book)
- **EMPRUNT** → **LECTEUR**: Many-to-One (Many borrowings by one reader)
- **EMPRUNT** → **UTILISATEUR**: Many-to-One (Many borrowings processed by one librarian)

---

## Application Structure

### Model Layer (Entity Classes)

**Location**: `src/main/java/model/`

**Livre.java** (Book Entity):
```java
@Entity
@Table(name = "LIVRE")
public class Livre {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @Column(unique = true, nullable = false)
    private String isbn;
    
    @Column(nullable = false)
    private String titre;
    
    private String auteur;
    private Integer anneePublication;
    private Integer nombreExemplaires;
    private Integer exemplairesDisponibles;
    
    @ManyToOne
    @JoinColumn(name = "id_categorie")
    private Categorie categorie;
    
    // Getters, setters, constructors
}
```

**Lecteur.java** (Reader Entity):
```java
@Entity
@Table(name = "LECTEUR")
public class Lecteur {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    private String nom;
    private String adresse;
    
    @Column(unique = true)
    private String numeroCni;
    
    private String telephone;
    private String email;
    private LocalDate dateInscription;
    private String statut;
    
    // Getters, setters, constructors
}
```

**Emprunt.java** (Borrowing Entity):
```java
@Entity
@Table(name = "EMPRUNT")
public class Emprunt {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @ManyToOne
    @JoinColumn(name = "id_livre", nullable = false)
    private Livre livre;
    
    @ManyToOne
    @JoinColumn(name = "id_lecteur", nullable = false)
    private Lecteur lecteur;
    
    @ManyToOne
    @JoinColumn(name = "id_bibliothecaire")
    private Utilisateur bibliothecaire;
    
    private LocalDate dateEmprunt;
    private LocalDate dateRetourPrevue;
    private LocalDate dateRetourEffective;
    private String statut;
    
    // Getters, setters, constructors
}
```

**Utilisateur.java** (User Entity):
```java
@Entity
@Table(name = "UTILISATEUR")
public class Utilisateur {
    @Id
    @GeneratedValue(strategy = GenerationType.IDENTITY)
    private Long id;
    
    @Column(unique = true, nullable = false)
    private String matricule;
    
    private String nom;
    
    @Column(nullable = false)
    private String motDePasse;
    
    private String role;
    private Timestamp dateCreation;
    
    // Getters, setters, constructors
}
```

### Data Access Layer (DAO)

**Location**: `src/main/java/dao/`

**LivreDAO.java**:
- `List<Livre> findAll()`
- `Livre findById(Long id)`
- `Livre findByIsbn(String isbn)`
- `void save(Livre livre)`
- `void update(Livre livre)`
- `void delete(Long id)`
- `List<Livre> search(String keyword)`

**LecteurDAO.java**:
- `List<Lecteur> findAll()`
- `Lecteur findById(Long id)`
- `Lecteur findByCni(String cni)`
- `void save(Lecteur lecteur)`
- `void update(Lecteur lecteur)`
- `void delete(Long id)`

**EmpruntDAO.java**:
- `List<Emprunt> findAll()`
- `Emprunt findById(Long id)`
- `List<Emprunt> findByLecteur(Long lecteurId)`
- `List<Emprunt> findByLivre(Long livreId)`
- `List<Emprunt> findEmpruntsEnCours()`
- `void save(Emprunt emprunt)`
- `void update(Emprunt emprunt)`

**UtilisateurDAO.java**:
- `Utilisateur findByMatricule(String matricule)`
- `Utilisateur authenticate(String matricule, String password)`
- `void save(Utilisateur utilisateur)`
- `void update(Utilisateur utilisateur)`

### Service Layer (Business Logic)

**Location**: `src/main/java/service/`

**LivreService.java**:
- Book catalog management
- Availability checking
- Search operations
- Inventory updates

**EmpruntService.java**:
- Borrowing logic
- Return processing
- Overdue tracking
- History management

**LecteurService.java**:
- Reader account management
- Membership validation
- Profile updates

**AuthentificationService.java**:
- User authentication
- Password hashing
- Session management

### Controller Layer (Servlets)

**Location**: `src/main/java/servlet/`

**AuthentificationServlet.java**:
- Handles login requests
- Session creation
- Authentication validation

**LivreServlet.java**:
- Processes book-related requests
- CRUD operations routing

**EmpruntServlet.java**:
- Borrowing operations
- Return processing

**LecteurServlet.java**:
- Reader management operations

**DashboardServlet.java**:
- Dashboard data preparation
- Statistics aggregation

### View Layer (JSP Pages)

**Location**: `src/main/webapp/`

**login.jsp**: Authentication interface

**dashboard.jsp**: Main dashboard

**livres/**:
- `liste.jsp`: Book catalog listing
- `details.jsp`: Individual book details
- `ajouter.jsp`: Add new book form
- `modifier.jsp`: Edit book form

**emprunts/**:
- `gestion.jsp`: Borrowing management
- `historique.jsp`: Borrowing history

**lecteurs/**:
- `liste.jsp`: Reader list
- `profil.jsp`: Reader profile
- `ajouter.jsp`: Add reader form

---

## User Guide

### Authentication

#### Login Process

1. **Access Application**:
   - Open web browser
   - Navigate to: `http://localhost:8080/projetBIBLIOTHEQUE(POO)`

2. **Enter Credentials**:
   - **Matricule** (Student/Employee ID): Enter your ID number
   - **Password**: Matricule + Full Name (no spaces)
   - Example:
     - Matricule: `22G00249`
     - Password: `22G00249MBOUMELATIFFAJAURESWILSON`

3. **Submit**:
   - Click "Se connecter" (Login)
   - System validates credentials
   - On success: Redirected to welcome page
   - On failure: Error message displayed

4. **Welcome Screen**:
   - Click "Continuer" (Continue)
   - Access main dashboard

### Book Management

#### Viewing Book Inventory

1. From dashboard, click "Livres" (Books)
2. View complete book catalog with:
   - ISBN
   - Title
   - Author
   - Publication year
   - Total copies
   - Available copies
   - Category

3. **Search Books**:
   - Use search bar
   - Enter: title, author, or ISBN
   - Results display matching books

4. **Filter by Category**:
   - Select category from dropdown
   - View books in selected category

#### Adding a New Book

1. Navigate to: **Livres → Ajouter un livre** (Add Book)

2. Fill required fields:
   - **ISBN**: International Standard Book Number
   - **Titre**: Book title
   - **Auteur**: Author name
   - **Année de publication**: Publication year
   - **Nombre d'exemplaires**: Number of copies
   - **Catégorie**: Select from dropdown

3. Click "Enregistrer" (Save)

4. Confirmation message appears

5. Book added to inventory

#### Modifying Book Information

1. From book list, click "Modifier" (Edit) on desired book

2. Update fields as needed:
   - Title
   - Author
   - Year
   - Number of copies
   - Category

3. Click "Enregistrer" (Save)

4. Changes reflected immediately

#### Deleting a Book

1. From book list, locate book to delete

2. Click "Supprimer" (Delete)

3. Confirmation dialog appears

4. Confirm deletion

5. Book removed from system

**Note**: Books with active borrowings cannot be deleted

### Reader Management

#### Viewing Readers

1. Click "Lecteurs" (Readers) from main menu

2. View all registered readers:
   - Name
   - CNI number
   - Address
   - Contact information
   - Registration date
   - Status

#### Adding a Reader

1. Navigate to: **Lecteurs → Ajouter un lecteur** (Add Reader)

2. Enter information:
   - **Nom**: Full name
   - **Adresse**: Residential address
   - **Numéro CNI**: National ID number
   - **Téléphone**: Phone number (optional)
   - **Email**: Email address (optional)

3. Click "Enregistrer" (Save)

4. Reader account created

#### Viewing Reader Profile

1. From reader list, click on reader name

2. View profile showing:
   - Personal information
   - Borrowing history
   - Current borrowings
   - Account status

#### Modifying Reader Information

1. Open reader profile

2. Click "Modifier" (Edit)

3. Update necessary fields

4. Save changes

### Borrowing Operations

#### Recording a New Borrowing

1. Navigate to: **Emprunts → Nouvel emprunt** (New Borrowing)

2. **Select Reader**:
   - Search by name or CNI
   - Select from list

3. **Select Book**:
   - Search by title, author, or ISBN
   - Verify availability
   - Select from available books

4. **Set Dates**:
   - Borrowing date (default: today)
   - Expected return date

5. Click "Enregistrer l'emprunt" (Record Borrowing)

6. System:
   - Decrements available copies
   - Creates borrowing record
   - Updates book status

#### Processing a Return

1. Navigate to: **Emprunts → Retours** (Returns)

2. Locate borrowing:
   - Search by reader name
   - Search by book title
   - View active borrowings

3. Select borrowing to return

4. Click "Enregistrer le retour" (Record Return)

5. System:
   - Sets actual return date
   - Increments available copies
   - Updates borrowing status
   - Checks for late return

#### Viewing Borrowing History

1. Navigate to: **Emprunts → Historique** (History)

2. View all borrowings with:
   - Reader name
   - Book title
   - Borrowing date
   - Expected return date
   - Actual return date
   - Status (IN_PROGRESS, RETURNED, OVERDUE)
   - Processing librarian

3. **Filter Options**:
   - By reader
   - By book
   - By date range
   - By status

### Librarian Management

#### Adding a Librarian

1. Navigate to: **Bibliothécaires → Ajouter** (Add Librarian)

2. Enter information:
   - Matricule (Employee ID)
   - Full name
   - Password
   - Role

3. Save

#### Managing Librarian Accounts

1. View all librarians

2. Modify information as needed

3. Deactivate accounts if necessary

### Dashboard Features

The dashboard provides:

**Statistics Cards**:
- Total books in catalog
- Total readers registered
- Active borrowings
- Overdue returns

**Recent Activity**:
- Latest borrowings
- Recent returns
- New book additions
- New reader registrations

**Quick Actions**:
- Record new borrowing
- Process return
- Add book
- Register reader

**Alerts**:
- Overdue borrowings
- Low stock books
- Inactive readers

---

## Security Features

### Implemented Security Measures

#### Authentication
- Form-based authentication
- Session management
- Secure password storage
- Automatic logout on inactivity

#### Password Security
- Passwords hashed (not stored in plain text)
- Format: Matricule + Full Name
- Strong password enforcement possible
- Brute force protection

#### Access Control
- Role-based access control (RBAC)
- Three roles defined:
  - **Administrator**: Full system access
  - **Bibliothécaire** (Librarian): Borrowing and catalog management
  - **Lecteur** (Reader): Personal account view only

#### Data Protection
- SQL injection prevention via parameterized queries
- XSS protection through input validation
- CSRF token protection for forms
- Session timeout configuration

#### Filters
- **AuthenticationFilter**: Validates user sessions
- **SecurityFilter**: Enforces role-based permissions

### Security Configuration

**web.xml** security constraints:
```xml
<security-constraint>
    <web-resource-collection>
        <web-resource-name>Protected Area</web-resource-name>
        <url-pattern>/dashboard/*</url-pattern>
        <url-pattern>/livres/*</url-pattern>
        <url-pattern>/emprunts/*</url-pattern>
    </web-resource-collection>
    <auth-constraint>
        <role-name>BIBLIOTHECAIRE</role-name>
        <role-name>ADMINISTRATEUR</role-name>
    </auth-constraint>
</security-constraint>
```

---

## API Documentation

### Authentication Endpoints

**POST /login**

Authenticates user and creates session.

**Request Parameters**:
- `matricule`: User ID (String)
- `motDePasse`: Password (String)

**Response**:
- Success: Redirect to dashboard
- Failure: Error message on login page

**POST /logout**

Invalidates user session.

**Response**: Redirect to login page

### Book Management Endpoints

**GET /livres/liste**

Retrieves list of all books.

**Response**: JSP page with book catalog

**GET /livres/details**

Shows detailed information for specific book.

**Parameters**:
- `id`: Book ID (Long)

**POST /livres/ajouter**

Creates new book entry.

**Parameters**:
- `isbn`: ISBN (String)
- `titre`: Title (String)
- `auteur`: Author (String)
- `anneePublication`: Year (Integer)
- `nombreExemplaires`: Copy count (Integer)
- `idCategorie`: Category ID (Long)

**POST /livres/modifier**

Updates existing book.

**Parameters**:
- `id`: Book ID (Long)
- Plus book fields to update

**POST /livres/supprimer**

Deletes book from catalog.

**Parameters**:
- `id`: Book ID (Long)

### Reader Management Endpoints

**GET /lecteurs/liste**

Retrieves list of all readers.

**POST /lecteurs/ajouter**

Registers new reader.

**Parameters**:
- `nom`: Full name (String)
- `adresse`: Address (String)
- `numeroCni`: ID number (String)
- `telephone`: Phone (String, optional)
- `email`: Email (String, optional)

**POST /lecteurs/modifier**

Updates reader information.

### Borrowing Endpoints

**GET /emprunts/gestion**

Shows borrowing management interface.

**POST /emprunts/nouveau**

Records new borrowing.

**Parameters**:
- `idLivre`: Book ID (Long)
- `idLecteur`: Reader ID (Long)
- `dateEmprunt`: Borrowing date (Date)
- `dateRetourPrevue`: Expected return (Date)

**POST /emprunts/retour**

Processes book return.

**Parameters**:
- `idEmprunt`: Borrowing ID (Long)
- `dateRetourEffective`: Return date (Date)

**GET /emprunts/historique**

Displays borrowing history.

**Parameters** (optional filters):
- `idLecteur`: Reader ID
- `idLivre`: Book ID
- `statut`: Status filter

---

## Development Team

This project was developed by a team of 10 students from the École Nationale Supérieure Polytechnique de Douala (ENSPD):

### Team Members

1. **KAMGANG NGAMIGNI MARC AUREL** - 22G00178
2. **KOUTA ERIC DONALD** - 24G01097
3. **MINKO NYANGONO ULRICH** - 22G00257
4. **MBOUMA ANNIE ORNELLA** - 22G00247
5. **MBOUMELA TIFFA JAURES WILSON** - 22G00249
6. **MBOUOMBOUO HAMED MOUDALIF** - 24G01112
7. **MOMO FOUMTHIM GEORGE ANGELA NATACHA** - 22G00264
8. **NGLITANG RUBEN** - 22G00500
9. **SIGNING TSANGO MARYLINE** - 22G00368
10. **TAMBOU NOUMSI CELIANE** - 22G00378

### Academic Supervision

**Supervisor**: Dr. NOULAPEU

**Institution**: École Nationale Supérieure Polytechnique de Douala (ENSPD)

**Program**: Génie Informatique - Génie Logiciel (Software Engineering)

**Academic Year**: 2024-2025

### Task Distribution

**Team A** (MBOUMELA):
- Java backend development
- Business logic implementation
- User manual creation

**Team B** (MBOUOMBOUO):
- Frontend development (HTML, CSS, JavaScript)
- User interface design

**Team C** (SIGNING):
- Database design and implementation
- SQLite configuration

**Team D** (TAMBOU, KOUTA, MOMO):
- UML diagram creation
- System modeling

**Team E** (MBOUMA, MINKO, MOMO):
- Documentation writing
- Project reporting

**Team F** (KAMGANG, NGLITANG):
- Support and coordination

---

## Troubleshooting

### Common Issues and Solutions

#### Issue 1: 404 Error in Browser

**Symptom**: Browser shows "HTTP Status 404 - Not Found"

**Causes**:
- Tomcat server not started
- Project not deployed to server
- Incorrect URL

**Solutions**:
1. Verify Tomcat is running in Eclipse Servers tab
2. Check project is added to server (right-click server → Add and Remove)
3. Verify URL: `http://localhost:8080/projetBIBLIOTHEQUE(POO)`
4. Check server port in Tomcat configuration (default: 8080)

#### Issue 2: Database Not Found

**Symptom**: Application starts but cannot connect to database

**Error Message**: "Unable to open database file" or similar

**Solutions**:
1. Verify `bibliotheque.db` exists in project
2. Check file location (should be in project root or WEB-INF)
3. Verify database file permissions (read/write access)
4. Ensure database path in code matches actual location

#### Issue 3: Display Issues

**Symptom**: Pages load but formatting is incorrect

**Solutions**:
1. Clear browser cache (Ctrl+F5 or Cmd+Shift+R)
2. Verify CSS files are in correct location (`webapp/css/`)
3. Check web.xml configuration
4. Ensure static resources are properly deployed

#### Issue 4: Missing JAR Files

**Symptom**: Compilation errors or NoClassDefFoundError

**Solutions**:
1. Verify all JARs in `WEB-INF/lib` folder:
   - JSTL JAR
   - SQLite JDBC driver
   - Any other required libraries
2. Right-click project → Build Path → Configure Build Path
3. Add missing JARs to build path
4. Clean and rebuild project

#### Issue 5: Port Already in Use

**Symptom**: Cannot start Tomcat - "Port 8080 already in use"

**Solutions**:

**Windows**:
```cmd
netstat -ano | findstr :8080
taskkill /PID <process_id> /F
```

**macOS/Linux**:
```bash
lsof -ti:8080 | xargs kill -9
```

**OR** change Tomcat port:
1. Double-click server in Servers tab
2. Change HTTP port from 8080 to 8081 (or other)
3. Save and restart server

#### Issue 6: Login Fails

**Symptom**: Correct credentials rejected

**Solutions**:
1. Verify password format: Matricule + Full Name (NO SPACES)
2. Check database for user record
3. Verify password hashing implementation
4. Check authentication servlet logic
5. Review session management

#### Issue 7: Project Not Recognized as Web Project

**Symptom**: Cannot run on server, missing web project structure

**Solutions**:
1. Right-click project → Properties
2. Project Facets
3. Enable "Dynamic Web Module" (version 5.0)
4. Enable "Java" (version 17)
5. Apply and close
6. Refresh project

#### Issue 8: Compilation Errors

**Symptom**: Red X marks, cannot compile

**Solutions**:
1. Verify JDK installed and configured
2. Check Java version compatibility (JDK 17+)
3. Update Eclipse to latest version
4. Clean project: Project → Clean
5. Update Maven dependencies (if using Maven)

#### Issue 9: Slow Performance

**Symptom**: Pages load slowly, operations take long time

**Solutions**:
1. Increase JVM heap size in Tomcat configuration
2. Optimize database queries
3. Add indexes to frequently queried columns
4. Clear Eclipse workspace
5. Close unnecessary Eclipse projects

#### Issue 10: Session Timeout

**Symptom**: Frequently logged out

**Solutions**:
1. Increase session timeout in web.xml:
```xml
<session-config>
    <session-timeout>30</session-timeout>
</session-config>
```
2. Modify Tomcat's session timeout
3. Implement "remember me" functionality

---

## Future Enhancements

### Planned Improvements

#### Advanced Features
- **Reservations**: Allow readers to reserve books currently borrowed
- **Email Notifications**: Automated reminders for due dates and overdue books
- **Fine Management**: Calculate and track late return penalties
- **Barcode Scanning**: Quick book and reader identification
- **Report Generation**: Exportable reports (PDF, Excel) for statistics

#### User Experience
- **Public Portal**: Online catalog browsing for non-members
- **Reader Self-Service**: Readers can view their account and history
- **Mobile Application**: iOS and Android apps for mobile access
- **Book Recommendations**: Suggest books based on borrowing history
- **Advanced Search**: Full-text search, filters, faceted navigation

#### Integration
- **API Development**: RESTful API for external system integration
- **LDAP Authentication**: Integration with institutional directory services
- **Digital Resources**: Management of e-books and online journals
- **Library Consortium**: Inter-library loan system

#### Technical Improvements
- **Migration to MySQL/PostgreSQL**: More robust database for production
- **Caching**: Implement Redis or Memcached for performance
- **Microservices**: Split into independent services
- **Cloud Deployment**: Deploy on AWS, Azure, or Google Cloud
- **Containerization**: Docker deployment for easier scaling

#### Analytics
- **Usage Statistics**: Detailed analytics on borrowing patterns
- **Popular Books Dashboard**: Most borrowed books, trending categories
- **Reader Analytics**: Active vs inactive readers, borrowing frequency
- **Inventory Optimization**: Recommendations for book purchases

---

## Maintenance and Support

### Backup Procedures

**Database Backup**:
- Daily automated backup of `bibliotheque.db`
- Backup retention: 30 days
- Location: Designated backup directory

**Backup Script** (scheduled task):
```bash
#!/bin/bash
DATE=$(date +%Y%m%d)
cp /path/to/bibliotheque.db /backup/bibliotheque_$DATE.db
```

**Restoration**:
1. Stop Tomcat server
2. Replace `bibliotheque.db` with backup file
3. Restart Tomcat
4. Verify data integrity

### Activity Logs

- All critical operations logged
- Log retention: 6 months
- Log location: `logs/` directory

### Updates and Patches

**Process**:
1. Test in development environment
2. Create database backup
3. Deploy update
4. Verify functionality
5. Monitor for issues

---

## Deployment to Production

### Production Environment Requirements

**Server**:
- Apache Tomcat 10.0+ or compatible application server
- Java JDK 17+
- Operating System: Linux (recommended), Windows Server, or macOS Server

**Database**:
- Migrate from SQLite to MySQL or PostgreSQL
- Proper backup and replication strategy

**Network**:
- Static IP address or domain name
- SSL/TLS certificate for HTTPS
- Firewall configuration

### Deployment Steps

1. **Prepare WAR File**:
   - Right-click project → Export → WAR file
   - Save to deployment location

2. **Configure Production Server**:
   - Install Tomcat on server
   - Configure SSL certificates
   - Set up firewall rules

3. **Deploy Application**:
   - Copy WAR to Tomcat `webapps/` directory
   - OR use Tomcat Manager application
   - Tomcat auto-deploys WAR

4. **Configure Database**:
   - Set up MySQL/PostgreSQL
   - Import schema
   - Migrate data from SQLite
   - Update database connection settings

5. **Environment Configuration**:
   - Set production database credentials
   - Configure logging
   - Set session timeout
   - Enable security features

6. **Testing**:
   - Verify all functionality
   - Load testing
   - Security testing
   - User acceptance testing

7. **Go Live**:
   - Switch DNS to production server
   - Monitor logs and performance
   - Have rollback plan ready

---

## Documentation References

### Official Documentation

- **Java Documentation**: https://docs.oracle.com/en/java/
- **Apache Tomcat**: https://tomcat.apache.org/tomcat-10.0-doc/
- **Jakarta EE**: https://jakarta.ee/specifications/
- **SQLite**: https://www.sqlite.org/docs.html

### Learning Resources

- **UML Modeling**: https://www.uml-diagrams.org/
- **JPA Tutorial**: https://www.tutorialspoint.com/jpa/
- **Servlet Programming**: https://www.oracle.com/java/technologies/servlet-technology.html
- **JSP Guide**: https://www.oracle.com/java/technologies/jspt.html

### Project-Specific Documentation

- **Technical Documentation**: See `documentation_technique.pdf`
- **Project Report**: See `Rapport_de_projet.pdf`
- **User Manual**: See `Manuel_d_utilisation.pdf`

---

## License

### Educational Use

This project was developed for educational purposes as part of the Object-Oriented Programming curriculum at ENSPD.

**Permitted Uses**:
- Educational study and learning
- Academic reference
- Personal experimentation
- Portfolio demonstration

**Restrictions**:
- Not for commercial use without permission
- Attribution to original team required
- Modifications should be documented

**Academic Integrity**:
- Students using this as reference must cite properly
- Direct copying for academic submissions is prohibited
- Use as learning resource encouraged

---

## Contact and Support

### Project Team Contact

For questions or issues related to this project:

**Institution**: École Nationale Supérieure Polytechnique de Douala (ENSPD)

**Address**: B.P 2701 Douala, Cameroon

**Phone**: +237 697 542 240

**Email**: contact@enspd-udo.cm

**Website**: www.enspdudo.cm

### Technical Support

For technical assistance:
1. Review this README documentation
2. Check Troubleshooting section
3. Consult project documentation (PDF files)
4. Contact development team members
5. Reach out to academic supervisor

---

## Acknowledgments

### Special Thanks

The development team expresses gratitude to:

- **Dr. NOULAPEU** for academic supervision and guidance
- **ENSPD Faculty** for providing the learning environment
- **Fellow Students** for collaboration and support
- **Open Source Community** for tools and frameworks used

### Technologies Acknowledgment

This project was made possible by:
- **Oracle** for Java platform and tools
- **Apache Software Foundation** for Tomcat server
- **Eclipse Foundation** for IDE
- **SQLite** development team
- **Jakarta EE** community

---

## Revision History

| Version | Date | Description | Author |
|---------|------|-------------|--------|
| 1.0 | January 2025 | Initial release | Development Team |

---

**Document Version**: 1.0  
**Last Updated**: January 2025  
**Status**: Production Ready (Educational)  
**Project Type**: Academic - Object-Oriented Programming Project

---

Built with dedication by ENSPD Software Engineering students for educational excellence.
