# IPSREF
IPSREF - Management and Scheduling System


This repository contains the source code for **IPSREF**, an integrated full-stack application that combines a web platform for users and administrators, a complementary desktop application, and a robust relational database. The system is designed to manage dishes, menus, schedules, extras, and customer support (including real-time chat).

---

## 📁 Project Structure

The project is divided into three main modules:

### 1. 🗄️ Database (`/BD`)
Contains all the necessary files for modeling and populating the relational database.
* **`create.sql`**: SQL script containing the structure of tables, primary keys, and foreign keys.
* **`inserts.sql`**: SQL script to populate the database with initial test data.
* **`esquema.png`**: Physical/relational diagram for database architecture documentation.

### 2. 🖥️ Desktop Application (`/PythonApp`)
A desktop application developed in Python, designed for local administration or a kiosk/totem system.
* **`ipsref.py`**: The main application file.
* **Visual Assets**: Includes UI elements such as `logo.png`, `alert.png`, and `lock.png`.

### 3. 🌐 Web Platform & Dashboard (`/Website`)
The core of the system, developed in PHP, CSS, and JavaScript, featuring both a public/user area and a comprehensive admin panel.

* **Infrastructure & API:**
  * `conexao.php`: Database connection configuration.
  * `api.php`: Endpoints for data communication and API requests.
* **User Area:**
  * `login.php` and `perfil.php`: Authentication and user profile management.
  * `faq.php` and `suporte.php`: User help center and support.
* **Administrative Dashboard:**
  * `index.php`: Main control panel featuring metrics and charts.
  * `pratos.php` and `agendarPratos.php`: Menu management and meal scheduling.
  * `extras.php`: Management of complements and extra items.
  * `chat.php` and `chats.php`: Real-time support and chat system.
* **Assets & Libraries:**
  * Modular styling organized within the `/css` folder (e.g., `historico.css`, `dashboard.css`).
  * `Inputmask` JavaScript library integration for automatic field formatting (IPs, dates, phone numbers, VAT/NIF).

---

## 🚀 Technologies Used

* **Backend:** PHP
* **Frontend:** HTML5, CSS3, JavaScript
* **Desktop:** Python
* **Database:** SQL (MySQL/PostgreSQL)
* **Libraries:** JavaScript

---

## 🛠️ Getting Started

1. **Database Setup:**
   * Import the `BD/create.sql` file into your preferred DBMS.
   * (Optional) Run `BD/inserts.sql` to load the mock data for testing.
   * Configure your database credentials inside `Website/conexao.php`.

2. **Running the Web Server:**
   * Host the `Website/` folder on a local server (such as Apache via XAMPP, Laragon, or Docker).
   * Open your browser and navigate to the local address (e.g., `http://localhost/IPSREF`).

3. **Running the Python Application:**
   * Python needs to be installed.
   * Run the following command in your terminal: `python PythonApp/ipsref.py`.
