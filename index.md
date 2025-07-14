# Swaxnet Table & File CRUD API Guide

## ENGLISH

### Table CRUD (Create, Read, Update, Delete)
- **Create (Insert):**
```bash
POST /api/data/secure.php?swax=TABLE_ID
Headers: Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
Body: { "username": "john", "email": "john@example.com" }
```
- **Read (Get):**
```bash
GET /api/data/secure.php?swax=TABLE_ID
Headers: Authorization: Bearer YOUR_API_KEY
```
- **Update:**
```bash
PUT /api/data/secure.php?swax=TABLE_ID&id=RECORD_ID
Headers: Authorization: Bearer YOUR_API_KEY
Content-Type: application/json
Body: { "username": "john_updated" }
```
- **Delete:**
```bash
DELETE /api/data/secure.php?swax=TABLE_ID&id=RECORD_ID
Headers: Authorization: Bearer YOUR_API_KEY
```

#### Example Success Response
```json
{ "success": true, "message": "Record inserted successfully" }
```
#### Example Error Response
```json
{ "error": "Table not found" }
```

### File Storage CRUD
- **Upload File:**
```bash
POST /api/storage/upload.php
Headers: Authorization: Bearer YOUR_API_KEY
Content-Type: multipart/form-data
Form Data: folder=FOLDER_NAME, file=(select file)
```

#### Example Success Response
```json
{ "success": true, "message": "File uploaded successfully" }
```
#### Example Error Response
```json
{ "error": "File extension not allowed" }
```
### you need help contact us 255657779003 whatsapp
