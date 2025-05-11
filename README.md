# 🪪 ID Card Auto-Crop API (FastAPI)

This FastAPI-based service accepts a scanned image of an ID card (with a white background) and returns a **cropped and straightened version** of the ID card.

---

## 📦 Features

- Upload scanned ID card image
- Automatically detects and crops the ID card
- Returns the result as a binary image file
- Works well with scanned images on A4 sheets

---

## 🔧 Requirements

Install dependencies:

```bash
pip install fastapi uvicorn python-multipart opencv-python

```
🚀 Run the API
uvicorn main:app --reload
This starts the server at: http://127.0.0.1:8000

📤 Upload via Postman
Method: POST

URL: http://127.0.0.1:8000/crop-id/

Body → form-data:

Key: file (type = File)

Value: Upload your image (e.g., scanned_id.jpg)

📥 Response
If successful: Returns a JPEG image (cropped_id.jpg) directly in Postman preview or as a file download.

If failed: Returns a JSON error like:

json
Copy
Edit
{ "error": "Could not detect ID card" }


