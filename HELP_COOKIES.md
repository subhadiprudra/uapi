# How to Fix "Sign in to confirm you’re not a bot" Error

This error happens when YouTube blocks the request because it looks automated or lacks authentication. To fix this, you need to provide valid cookies from a logged-in browser session.

## Option 1: Export `cookie.txt` (Recommended)

1.  **Install a Browser Extension**:
    - **Chrome/Brave/Edge**: Install [Get cookies.txt LOCALLY](https://chrome.google.com/webstore/detail/get-cookiestxt-locally/cclelndahbckbenkjhflccpebjtmnkjp).
    - **Firefox**: Install [cookies.txt](https://addons.mozilla.org/en-US/firefox/addon/cookies-txt/).

2.  **Log in to YouTube**:
    - Open your browser and go to [https://www.youtube.com](https://www.youtube.com).
    - Make sure you are logged in.

3.  **Export Cookies**:
    - Click the extension icon.
    - Click "Export" or "Download".
    - Save the file as `cookie.txt`.

4.  **Place the File**:
    - Move the `cookie.txt` file to this folder:
      `/Users/subhadiprudra/flutter_apps/misic_vdotube/uapi/`
    - **Important**: Overwrite the existing `cookie.txt` if it exists.

5.  **Restart the Server**:
    - Stop the server (Ctrl+C) and start it again.

## Option 2: Use Browser Cookies Directly (Local Only)

If you are running this locally and have Chrome installed, you can modify `app.py` to pull cookies directly from Chrome.

Change `ydl_opts` in `app.py`:

```python
ydl_opts = {
    'format': 'best',
    'quiet': True,
    'cookiesfrombrowser': ('chrome',),  # Uses cookies from Chrome
}
```
*Note: This requires Chrome to be closed (on some systems) or unlocked.*
