# Video URL Extractor API

A simple Flask API that uses `yt-dlp` to extract direct download URLs from video services (like YouTube).

## Setup

1.  **Create a virtual environment (optional):**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

## Running the App

```bash
python app.py
```

The server will start at `http://0.0.0.0:5000`.

## Usage

**Endpoint:** `GET /extract`

**Query Parameter:** `url` (The URL of the video)

**Example:**

```bash
curl "http://127.0.0.1:5000/extract?url=https://www.youtube.com/watch?v=dQw4w9WgXcQ"
```

**Response:**

```json
{
  "download_url": "https://rr3---sn-...",
  "title": "Rick Astley - Never Gonna Give You Up (Official Music Video)",
  "thumbnail": "https://i.ytimg.com/vi/dQw4w9WgXcQ/maxresdefault.jpg",
  "duration": 212
}
```
