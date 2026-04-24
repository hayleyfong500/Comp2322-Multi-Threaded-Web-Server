# Comp2322-Multi-Threaded-Web-Server
Multi-thread Web Server
- Name: Fong Po Hei
- Student ID: 24095734d
- Course: Comp 2322 Computer Networking

Requirements:
- Python 3.6+

How to Run:
python server.py

How to Test:
Visit: http://127.0.0.1:8080/

Command Line (curl):
# GET text file
curl http://127.0.0.1:8080/test.txt

# GET image
curl http://127.0.0.1:8080/test.png -o test.png

# HEAD request
curl -I http://127.0.0.1:8080/

# 404 test
curl http://127.0.0.1:8080/missing.html

# 403 test (path traversal)
curl http://127.0.0.1:8080/../secret

# 304 test (cache)
curl -H "If-Modified-Since: Sat, 01 Jan 2000 00:00:00 GMT" http://127.0.0.1:8080/

PowerShell (Windows):
# GET request
Invoke-WebRequest -Uri http://127.0.0.1:8080/index.html

# HEAD request
Invoke-WebRequest -Uri http://127.0.0.1:8080/index.html -Method HEAD

# POST request (400 test)
Invoke-WebRequest -Uri http://127.0.0.1:8080/index.html -Method POST

# Path traversal (403 test)
Invoke-WebRequest -Uri "http://127.0.0.1:8080/../secret.txt"

Files:
- `server.py` - Main server code
- `web_root/` - Web files directory
- `request.log` - Access log (auto-generated)

Features:
- Multi-threaded concurrent processing
- GET and HEAD methods
- 5 HTTP status codes (200, 304, 400, 403, 404)
- Cache control (Last-Modified / If-Modified-Since)
- Persistent connections (keep-alive)
- Access logging
- Path traversal protection
<img width="468" height="648" alt="image" src="https://github.com/user-attachments/assets/a1f8ae8f-0d86-448b-b27c-8600e7e2dc77" />
