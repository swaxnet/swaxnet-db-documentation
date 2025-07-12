## If you already have a table like users and Forder like profile_pictures ready this doc


## Complete CRUD Examples

### Create (POST)
```bash
# Add a new user
curl -X POST "https://www.api.swaxnet.xyz/api/data/index.php?table=users" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "id": "2",
    "username": "jane_smith",
    "email": "jane@example.com",
    "age": 30,
    "is_active": true,
    "created_at": "2024-01-15"
  }'
```

### Read (GET)
```bash
# Get all users
curl -X GET "https://www.api.swaxnet.xyz/api/data/index.php?table=users" \
  -H "Authorization: Bearer YOUR_API_KEY"

# Get specific user by ID
curl -X GET "https://www.api.swaxnet.xyz/api/data/index.php?table=users&id=1" \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### Update (PUT)
```bash
# Update user with ID 1
curl -X PUT "https://www.api.swaxnet.xyz/api/data/index.php?table=users&id=1" \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -d '{
    "username": "john_doe_updated",
    "age": 26,
    "is_active": false
  }'
```

### Delete (DELETE)
```bash
# Delete user with ID 1
curl -X DELETE "https://www.api.swaxnet.xyz/api/data/index.php?table=users&id=1" \
  -H "Authorization: Bearer YOUR_API_KEY"
```

### Upload File
```bash
curl -X POST https://www.api.swaxnet.xyz/api/storage/upload.php \
  -H "Authorization: Bearer YOUR_API_KEY" \
  -F "folder=profile_pictures" \
  -F "file=@/path/to/your/image.jpg"
```
