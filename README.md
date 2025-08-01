# GEMINI-INTEGRATED-BACKEND

A lightweight and practical RESTful API powered by [Gemini 2.5 Flash](https://ai.google.dev/gemini-api/docs/models/gemini), built with Node.js and Express.  
This backend supports **multimodal input** — generate content or analysis from **text, image, document, and audio**.

## 🔥 Features

| Endpoint                  | Method | Description                              |
|--------------------------|--------|------------------------------------------|
| `/generate-text`         | POST   | Generate text from a plain prompt        |
| `/generate-from-image`   | POST   | Analyze uploaded image + optional prompt |
| `/generate-from-document`| POST   | Summarize or analyze a document file     |
| `/generate-from-audio`   | POST   | Transcribe or analyze uploaded audio     |

## ⚙️ Tech Stack

- **Node.js** with **Express**
- **Google Generative AI SDK** (@google/generative-ai)
- **Multer** for file upload handling
- **dotenv** for environment configuration
- **fs** for file cleanup

## 🧪 How to Use

### 1. Clone this repo

```
git clone https://github.com/adammarchelino/adam-genai-backend.git
cd adam-genai-backend
````

### 2. Install dependencies

```
npm install
```

### 3. Configure environment

Buat file `.env` berdasarkan template berikut:

```env
# .env
GEMINI_API_KEY=your-google-api-key-here
```

### 4. Run the server

```
node index.js
```

Server akan berjalan di `http://localhost:3000`

## 🔌 Testing the API

Gunakan Postman / ThunderClient untuk testing.

### ➤ `/generate-text`

* **Method:** `POST`
* **Body (raw - JSON):**

```json
{
  "prompt": "Tuliskan artikel tentang dampak teknologi AI"
}
```

---

### ➤ `/generate-from-image`

* **Method:** `POST`
* **Body (form-data):**

  * `image`: *(type: File)*
  * `prompt`: *(type: Text)* (opsional)

---

### ➤ `/generate-from-document`

* **Method:** `POST`
* **Body (form-data):**

  * `document`: *(type: File - PDF/TXT/etc)*

---

### ➤ `/generate-from-audio`

* **Method:** `POST`
* **Body (form-data):**

  * `audio`: *(type: File - MP3/WAV)*
  * `prompt`: *(type: Text)* (opsional)

## 📁 File Structure

```
├── index.js               # Main server logic
├── .env.example           # Env variable template
├── .gitignore             # Git ignore rules
├── package.json           # Dependencies and scripts
├── uploads/               # Temp file storage (auto-created by multer)
```

## 👨‍💻 Author

Built with focus & fire by
**[Adam Marchelino](https://github.com/adammarchelino)** 🚀
*A young BEGINNER walking against the current.*
