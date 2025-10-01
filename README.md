# 🍔 Restaurant QR Menu Generator

A modern web application built with Django that allows users to instantly generate QR codes for their restaurant's digital menu. This project provides a simple and efficient backend foundation to create and download QR codes from any menu URL, making the shift to digital menus seamless for restaurant owners.

---

## ✨ Features

* **Restaurant Management**
    * Generate a unique QR code for any restaurant menu by providing a name and a URL.
    * Download the generated QR code directly as a high-quality `.png` image, ready for printing.

* **Simple User Interface**
    * Clean and intuitive form to input restaurant details.
    * A dedicated results page to preview the QR code before downloading.

* **Dynamic Generation**
    * The backend is powered by Python to dynamically create QR code images based on user input.

---

## 🛠️ Tech Stack

| Layer             | Technology / Library                    |
| :---------------- | :-------------------------------------- |
| **Backend** | Python, Django                          |
| **Frontend** | HTML, CSS, Bootstrap                    |
| **QR Generation** | `qrcode` (Python library)               |
| **Data Exchange** | HTTP Methods (GET, POST)                |
| **Database** | SQLite3 (Default for Development)       |

---

## 🚀 Getting Started

### Prerequisites

Make sure the following are installed on your system:
* Python 3.8+
* pip
* Git

### Local Setup (Linux/macOS/Windows)

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/sachink8n/menu-qr-generator.git](https://github.com/sachink8n/menu-qr-generator.git)
    cd menu-qr-generator
    ```

2.  **Create and activate the virtual environment**
    ```bash
    # Create the venv
    python -m venv venv

    # Activate the venv (on macOS/Linux)
    source venv/bin/activate

    # Activate the venv (on Windows)
    .\venv\Scripts\activate
    ```

3.  **Install project dependencies**
    ```bash
    pip install -r requirements.txt
    ```
    *(Note: If `requirements.txt` does not exist, create it with `pip freeze > requirements.txt`)*

4.  **Run the Django application**
    ```bash
    python manage.py runserver
    ```
    The application will be live at `http://12.0.0.1:8000/`.

---

## Application Endpoints

The application currently has one main endpoint for generating the QR code.

| Method   | Endpoint           | Description                                       |
| :------- | :----------------- | :------------------------------------------------ |
| `GET`    | `/`                | Displays the main form to enter restaurant details. |
| `POST`   | `/`                | Submits the form data to generate the QR code.    |

### Form Parameters (POST)

| Param              | Description                               |
| :----------------- | :---------------------------------------- |
| `restaurant_name`  | The name of the restaurant (e.g., "Ammu Restaurant"). |
| `menu_url`         | The full URL to the restaurant's menu.     |

---

## 🔮 Future Enhancements

* **User Authentication:** A complete login/signup system for restaurant owners.
* **Dashboard:** A user-specific dashboard to manage and view all created QR codes.
* **QR Code Customization:** Add options to change colors and embed a logo.
* **Scan Analytics:** A feature to track the number of scans for each QR code.

