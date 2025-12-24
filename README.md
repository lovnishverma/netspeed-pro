# 🚀 NetSpeed Pro

**Enterprise-Grade Network Diagnostics Tool**

NetSpeed Pro is a lightweight, professional network speed testing application built with vanilla JavaScript. Unlike heavy, ad-filled alternatives, this tool is designed for accuracy, privacy, and performance. It runs entirely in the browser and leverages Cloudflare's massive global edge network to provide low-latency, accurate connection metrics.

🔗 **Live Demo:** [https://www.lovnishverma.in/netspeed-pro/](https://www.lovnishverma.in/netspeed-pro/)

---

## ✨ Features

* **Real-Time Diagnostics:** Measures **Download**, **Upload**, **Ping**, and **Jitter** with millisecond precision.
* **Packet Loss Detection:** Tracks failed ping requests to calculate real packet loss percentage.
* **Enterprise UI:** Clean, glassmorphism-inspired interface with animated particles and smooth SVG graphs.
* **Gigabit Ready:** Optimized payload sizes (up to 50MB) to accurately test high-speed fiber connections.
* **No Backend Required:** Runs 100% client-side using public CORS-enabled APIs.
* **Export Data:** Built-in JSON export functionality to save test results for analysis.
* **Mobile Responsive:** Fully adaptive design that works on desktops, tablets, and phones.

---

## 🛠 How It Works

NetSpeed Pro performs a series of distinct tests to analyze your connection health:

1. **Ping & Jitter:** Sends rapid `HEAD` requests to the server to measure latency (Ping) and the variance in response times (Jitter). Any failed requests are counted as Packet Loss.
2. **Download Test:** Downloads binary blobs of increasing size (up to 50MB) from Cloudflare's edge servers (`speed.cloudflare.com`), calculating throughput in real-time.
3. **Upload Test:** Generates random binary data and POSTs it to the server to measure upstream bandwidth.

> **Note:** We use Cloudflare's public speed test endpoints because they offer massive bandwidth capacity and are physically located close to users worldwide.

---

## 💻 Tech Stack

* **Core:** HTML5, CSS3, Vanilla JavaScript (ES6+)
* **Network API:** `XMLHttpRequest` (for progress tracking) & `Fetch API`
* **Styling:** CSS Custom Properties (Variables), Flexbox/Grid, CSS Animations
* **Fonts:** JetBrains Mono (Data), Lexend (UI)

---

## 🚀 Getting Started

To run this project locally on your machine:

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/netspeed-pro.git
cd netspeed-pro

```


2. **Run a local server**
Because of browser security (CORS), speed tests may not work if you simply open the `index.html` file. You need a local server.
* **Using Python:**
```bash
python3 -m http.server 8000

```


* **Using VS Code:**
Install the "Live Server" extension and click "Go Live" at the bottom right.


3. **Open in Browser**
Visit `http://localhost:8000` to see the app running.

---

## ⚙️ Configuration

You can tweak the test parameters by editing the `CONFIG` object in `index.html`:

```javascript
const CONFIG = {
    testFileSizes: {
        download: 52428800, // 50 MB (Adjust for slower/faster connections)
        upload: 10485760,   // 10 MB
    },
    pingAttempts: 10,       // Increase for more accurate Packet Loss data
    requestTimeout: 30000,  // Timeout in milliseconds
};

```

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improvements (like historical data charts or theme switching), feel free to fork the repo and submit a pull request.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.

---

*Developed by [Lovnish Verma*](https://www.lovnishverma.in/)

Here is a video explaining how to build similar speed test applications in JavaScript. [Internet Speed Test App](https://www.youtube.com/watch?v=FMm60Mz20C4)
