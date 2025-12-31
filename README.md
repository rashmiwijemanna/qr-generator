# 📱 Product QR Code Generator

A lightweight, efficient tool designed for retail and inventory management systems to generate scannable QR codes instantly. This application integrates with the GoQR API to dynamically render images based on user input, suitable for product labeling and URL sharing.

## 🚀 Key Features
* **Instant QR Generation:** Converts text, URLs, or Product IDs into high-quality QR codes in milliseconds.
* **Input Validation:** Prevents API misuse by detecting empty inputs and triggering user alerts.
* **API Integration:** Fetches dynamic images using the RESTful `api.qrserver.com` endpoint.
* **Interactive UI:** Smooth reveal animations and a clean, card-based interface using CSS3.

## 🛠️ Technologies Used
* **Frontend:** HTML5, CSS3
* **Logic:** JavaScript (ES6+)
* **API:** [QR Server API](https://goqr.me/api/)
* **Tools:** VS Code, Git

## 📸 Usage
1. Open `index.html` in any modern web browser.
2. Enter a text string, URL, or Product ID (e.g., `Product-5501`).
3. Click **"Generate QR Code"**.
4. The system validates the input and renders the QR code instantly.

## ⚙️ How it Works (Code Snippet)
The application uses DOM manipulation to fetch user input and construct a dynamic API request:

```javascript
function generateQR(){
    if(qrText.value.length > 0){
        qrImage.src = "[https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=](https://api.qrserver.com/v1/create-qr-code/?size=150x150&data=)" + qrText.value;
        imgBox.classList.add("show-img");
    } else {
        alert("Please enter a valid text or URL!");
    }
}
