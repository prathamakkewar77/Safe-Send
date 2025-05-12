# 🔒 Safe-Send: Secure File Sharing System

Safe-Send is a secure file sharing platform that ensures confidential files are transferred with proper authentication and encryption measures. It uses file content verification, token-based authentication, and secure download links.

## 🚀 Features

- 🔐 **JWT-based Authentication** for users
- 🧠 **File Type Detection** using `python-magic` (not just by file extension)
- 🕵️ **Content Verification** before allowing uploads
- 🧩 **Encrypted, Expiring Download URLs**
- 🛡️ **Hashed Password Storage** using secure algorithms
- 👥 User Role: Operation Users can upload and share files

---

## 🧰 Technology Stack

| Component        | Technology           |
|------------------|----------------------|
| **Framework**    | Flask                |
| **Database**     | MongoDB              |
| **Auth**         | JWT (JSON Web Tokens)|
| **File Detection**| python-magic        |

---

## 🔐 Security Considerations

- ✅ File types verified by analyzing contents, not just extensions
- ✅ Passwords securely hashed before storage
- ✅ Download links are encrypted and expire after a short duration

---

## 📦 API Endpoints

### 🔑 Authentication

- `POST /signup` — Register a new user  
- `GET /verify-email/<token>` — Verify a user's email  
- `POST /login` — Authenticate a user and receive a token  

### 📁 File Operations

- `POST /upload` — Upload a file (**Operation Users** only)  
- `GET /files` — List all uploaded files  
- `GET /download/<file_id>` — Generate a secure download link  
- `GET /secure-download/<token>` — Download the file using the token  
