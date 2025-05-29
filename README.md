# UsageMonitorNodeJS

**UsageMonitorNodeJS** is a lightweight Node.js application that collects system usage information (CPU, RAM, etc.) and provides it via an API. A simple HTML frontend is included to visualize the data.

---

## 📦 Installation

1. **Clone the repository**

```bash
git clone https://github.com/JJBanana13/UsageMonitorNodeJS.git
cd UsageMonitorNodeJS
```

2. **Install dependencies**

```bash
npm install
```

---

## 🚀 Run the Server (Development)

You can start the server manually using:

```bash
node server.js
```

The API will be available at:

```
http://localhost:3000/api
```

---

## ⚙️ Run with PM2 (Production)

To keep the server running in the background and restart it automatically on system boot or crash, use [PM2](https://pm2.keymetrics.io/).

1. **Install PM2 globally**

```bash
npm install -g pm2
```

2. **Start the server with PM2**

```bash
pm2 start server.js --name usage-monitor
```

3. **Enable auto-start on boot**

```bash
pm2 save
pm2 startup
```

---

## 🌐 Configure the Frontend

The `index.html` file is used to visualize the system usage data.

> 🔧 **IMPORTANT:** You must set the correct API URL manually in the `index.html` file.

Look for the following line:

```js
this.apiUrl = 'https://YOUR-BACKEND.de/api';
```

Replace it with the actual URL of your backend. For example:

```js
this.apiUrl = 'http://localhost:3000/api';
```

Make sure this URL matches the address where your Node.js server is running.

---

## 🛠️ Technologies Used

- Node.js
- Express.js
- HTML / CSS / JavaScript (Vanilla)
- PM2 (for process management, optional)

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

Created by [JJBanana13](https://github.com/JJBanana13)
