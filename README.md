# OB53 JWT API

A lightweight Flask-based API for generating and processing authentication tokens for **Free Fire OB53**.

The project provides simple HTTP endpoints for obtaining an access token using guest credentials and processing the authentication flow to return JWT-related account information.

## ✨ Features

* 🚀 Flask REST API
* 🔐 Guest OAuth token generation
* 🔑 JWT token processing
* 🌐 Free Fire OB53 authentication flow
* 📦 Protocol Buffers support
* ⚡ Lightweight and easy to deploy
* ☁️ Vercel deployment configuration included
* 🐍 Python based

## 📁 Project Structure

```text
OB53-JWT-API-SRC/
├── app.py
├── my_pb2.py
├── output_pb2.py
├── requirements.txt
├── vercel.json
└── README.md
```

## 🛠️ Requirements

* Python 3.9+
* pip
* Internet connection

## 📥 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/OB53-JWT-API-SRC.git
cd OB53-JWT-API-SRC
```

Install the dependencies:

```bash
pip install -r requirements.txt
```

## ▶️ Run Locally

Start the API:

```bash
python app.py
```

The server will run on:

```text
http://127.0.0.1:1080
```

For a VPS/server, the application listens on:

```text
0.0.0.0:1080
```

## 🔗 API Endpoints

### `/token`

Generates an authentication flow using a UID and password.

**Method:**

```http
GET
```

**Parameters:**

```text
uid
password
```

**Example:**

```text
http://YOUR-IP:1080/token?uid=YOUR_UID&password=YOUR_PASSWORD
```

### `/access-jwt`

Processes an access token and returns account/JWT information.

**Method:**

```http
GET
```

**Parameters:**

```text
access_token
open_id
```

`open_id` can be omitted when the API is able to retrieve it automatically.

**Example:**

```text
http://YOUR-IP:1080/access-jwt?access_token=YOUR_ACCESS_TOKEN&open_id=YOUR_OPEN_ID
```

## 📦 Dependencies

The project uses:

* Flask
* PyCryptodome
* Requests
* Protocol Buffers
* PyJWT
* Flask-Caching

Install everything with:

```bash
pip install -r requirements.txt
```

## ☁️ Vercel Deployment

This repository includes a `vercel.json` configuration.

Install and configure the Vercel CLI:

```bash
npm install -g vercel
```

Then deploy:

```bash
vercel
```

Follow the Vercel prompts to complete deployment.

## ⚠️ Security Notice

Do **not** expose real account credentials, access tokens, cookies, private keys, or other sensitive authentication information in a public GitHub repository.

If sensitive credentials have accidentally been committed, rotate/revoke them immediately.

This project is provided for educational and development purposes. Use it responsibly and only with accounts and services you are authorized to access.

## 👨‍💻 Credits

**Developed by Mahendra**

© 2026 Mahendra. All rights reserved.

## ⭐ Support

If this project was useful to you, consider giving the repository a ⭐ on GitHub.

---

### Made ❤️ by Mahendra
