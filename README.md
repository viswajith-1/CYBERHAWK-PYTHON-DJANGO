# 🦅 CYBERHAWK: A Cyber Awareness & Crime Reporting Portal

**CYBERHAWK** is a comprehensive web platform designed to combat the rising threat of cybercrime. It serves as a centralized hub for users to report cybercrimes, access vital educational resources, and stay informed with real-time cybersecurity news.

[cite_start]This project was submitted in 2024 in partial fulfillment of the requirements for the award of the BSc Degree in Computer Science from the University of Kerala, by students of Naipunnya School of Management, Cherthala[cite: 1, 14, 16].

*Screenshots*

<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/563db8cf-2870-42fa-b125-fba294a93d1a" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/b2755be1-f64b-40a2-a6a5-796f9dbc13c2" />
<img width="940" height="529" alt="image" src="https://github.com/user-attachments/assets/661dd300-146e-441c-97df-db22802d50d4" />



---

## 📍 Table of Contents

- [About The Project](#about-the-project)
- [✨ Key Features](#-key-features)
- [🔐 Role-Based Access Control](#-role-based-access-control)
- [💻 Tech Stack](#-tech-stack)
- [🗃️ Database Schema](#️-database-schema)
- [🚀 Getting Started](#-getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [📈 Future Enhancements](#-future-enhancements)

---

## 🎯 About The Project

Cybercrime is a growing global threat. [cite_start]Cyberhawk aims to empower users to be aware of and fight back against these threats through a user-friendly platform[cite: 57, 104].

The primary objectives are:
* [cite_start]**Empower Users:** Provide a platform to report cybercrimes easily and conveniently[cite: 109].
* [cite_start]**Educate & Inform:** Offer educational resources, practical tips, and real-time cybersecurity news to help users protect themselves[cite: 58, 59, 105, 106, 110].
* [cite_start]**Report & Track:** Allow users to file cybercrime reports, track the investigation's progress, receive updates, and access final case results[cite: 60, 107].
* [cite_start]**Analyze Trends:** Collect and analyze reported cybercrimes to identify emerging threats and share prevention strategies[cite: 111].

## ✨ Key Features

* [cite_start]**Cybercrime Complaint Filing:** A streamlined process for users to report various cybercrimes[cite: 115].
* [cite_start]**Case Tracking System:** A secure portal for users to monitor the progress of their reported cases and access final reports[cite: 115].
* [cite_start]**Cybersecurity News & Updates:** A real-time feed of relevant news articles to keep users informed about emerging threats[cite: 115].
* [cite_start]**Educational Resources:** A library of articles, videos, and tutorials on practical online safety and self-defense[cite: 115].
* [cite_start]**User-Centric Design:** A simple and intuitive interface accessible to users of all technical backgrounds[cite: 115].
* [cite_start]**Multi-Role Functionality:** A comprehensive system with separate modules for Users, Admins, Managers, and Employees[cite: 116, 117].

## 🔐 Role-Based Access Control

The platform features a multi-layered access system to manage operations effectively:

* **👤 User:** The primary citizen-facing module. [cite_start]Users can file reports, access educational content, read news, and track their case status[cite: 345, 346, 347, 348, 352, 353, 354].
* [cite_start]**🛡️ Admin:** Has a comprehensive administrator module to view all reported crimes, identify emerging trends, and manage user accounts[cite: 270, 277, 279, 281, 286, 289].
* [cite_start]**👨‍💼 Manager:** Uses the manager module to view and assign cases to investigators (Employees) and manage employee accounts[cite: 294, 302, 304, 305, 306].
* [cite_start]**🕵️ Employee (Investigator):** Equipped with an employee module to investigate assigned cybercrimes, view reports, and update case status[cite: 325, 328, 331, 335].

## 💻 Tech Stack

[cite_start]This project was built using the following technologies[cite: 170]:

* **Technology:** Python Django
* **Database:** Sqlite3
* **Frontend:** HTML5, CSS3, JavaScript, Bootstrap
* **Development Tools:** Visual Studio Code
* **Platform:** Windows/Linux

## 🗃️ Database Schema

The system utilizes four main tables to manage data:

1.  [cite_start]**RegistrationTBL:** Stores user information including `NAME`, `MOBILE NO.`, `EMAIL_ID` (Primary Key), `PASSWORD`, and `USER_TYPE`[cite: 361].
2.  [cite_start]**LoginTBL:** Manages login credentials, with `EMAIL_ID` as a Foreign Key linked to `RegistrationTBL`[cite: 363].
3.  **CaseTBL:** Contains all details of a reported crime, such as `CASE_ID` (Primary Key), victim information, `INCIDENT_TYPE`, `DESCRIPTION`, and `CASE_PROGRESS`. [cite_start]It includes `ASSIGNED_TO` as a Foreign Key to link to an investigator[cite: 365].
4.  [cite_start]**ContentTBL:** Stores content for the news and educational sections, linking to the creator via `EMAIL_ID` as a Foreign Key[cite: 367].

## 🚀 Getting Started

Follow these instructions to get a local copy of the project up and running for development and testing.

### Prerequisites

You will need to have the following software installed on your machine:
* [Python 3.x](https://www.python.org/downloads/)
* [pip](https://pip.pypa.io/en/stable/installation/) (Python package installer)
* [Git](https://git-scm.com/downloads)

### Installation

1.  **Clone the repository**
    ```sh
    git clone [https://github.com/](https://github.com/)[YOUR-USERNAME]/[YOUR-REPO-NAME].git
    cd [YOUR-REPO-NAME]
    ```

2.  **Create and activate a virtual environment** (Recommended)
    ```sh
    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install dependencies**
    (This project uses Django and its default Sqlite3. If you have other packages, create a `requirements.txt` file and run `pip install -r requirements.txt`)
    ```sh
    pip install django
    ```

4.  **Apply database migrations**
    This will create the `db.sqlite3` file and set up the tables.
    ```sh
    python manage.py migrate
    ```

5.  **Create a superuser (Admin)**
    This will give you access to the Django admin panel, which corresponds to the "Admin" role.
    ```sh
    python manage.py createsuperuser
    ```
    Enter a username, email, and password when prompted.

6.  **Run the development server**
    ```sh
    python manage.py runserver
    ```

7.  Open your browser and navigate to `http://127.0.0.1:8000/` to view the application.
    * **Admin Panel:** `http://127.0.0.1:8000/admin`

## 📈 Future Enhancements

[cite_start]The project report identifies several exciting avenues for future development[cite: 507]:

* [cite_start]**Law Enforcement Integration:** Streamline case reporting by integrating with official law enforcement databases (subject to legal and privacy regulations)[cite: 508, 509].
* [cite_start]**AI-Powered Chatbots:** Implement 24/7 AI-powered chatbots to provide basic guidance and support to users[cite: 510].
* [cite_start]**Interactive Learning Modules:** Expand the educational library with interactive modules to better engage users and solidify their understanding of cybersecurity best practices[cite: 510, 511].
