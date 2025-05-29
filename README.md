Sure! Here's a complete, ready-to-copy `README.md` for your project **UsageMonitorNodeJS** in English, including `pm2` usage and instructions on how to set the API URL in the frontend (`this.apiUrl = 'https://YOUR-BACKEND.de/api';`).

---

````markdown
# UsageMonitorNodeJS

**UsageMonitorNodeJS** is a lightweight Node.js application that collects system usage information (CPU, RAM, etc.) and exposes it via an API. A simple HTML frontend is included to visualize the data.

---

## 📦 Installation

1. **Clone the repository**

```bash
git clone https://github.com/JJBanana13/UsageMonitorNodeJS.git
cd UsageMonitorNodeJS
````

2. **Install dependencies**

```bash
npm install
```

---

## 🚀 Run the Server

You can start the server manually using:

```bash
node server.js
```

By default, the server runs on port `3000`. The system usage data will be available at:

```
http://localhost:3000/api
```

---

## ⚙️ Run with PM2 (for production use)

If you want the server to keep running in the background and restart on crash or reboot, use [PM2](https://pm2.keymetrics.io/):

1. **Install PM2 globally**

```bash
npm install -g pm2
```

2. **Start the server with PM2**

```bash
pm2 start server.js --name usage-monitor
```

3. **Save the process list and set up startup script**

```bash
pm2 save
pm2 startup
```

---

## 🌐 Configure the Frontend

The `index.html` file is a simple frontend that displays system usage stats.

📌 **IMPORTANT:** You need to set the correct API URL in the HTML file.

Open `index.html` and look for the following line:

```js
this.apiUrl = 'https://YOUR-BACKEND.de/api';
```

Replace `'https://YOUR-BACKEND.de/api'` with the actual URL of your backend, for example:

```js
this.apiUrl = 'http://localhost:3000/api';
```

Make sure this URL matches where your backend is hosted.

---

## 🛠️ Technologies Used

* Node.js
* Express.js
* HTML / CSS / JavaScript (Vanilla)
* PM2 (optional for process management)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 💡 Author

Made by [JJBanana13](https://github.com/JJBanana13)

```

---

Let me know if you'd also like a `LICENSE` file, a `.pm2.config.js`, or anything else to go with it.
```
