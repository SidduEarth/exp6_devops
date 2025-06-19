
## 🔧 How to Create a Dockerfile in VS Code (Windows)

---

### 🧰 Step 1: Set Up Folder

Create a new folder on your Desktop:

```plaintext
hello-html-docker
```

Inside this folder, you will place:

* `index.html` (your HTML file)
* `Dockerfile` (your Docker build script)

---

### 📥 Step 2: Open the Folder in VS Code

1. Open **Visual Studio Code**
2. Click on `File` → `Open Folder...` → select your `hello-html-docker` folder

---

### 📝 Step 3: Create Files in VS Code

#### 1. Create a new file:

**File Name:** `index.html`
**Right-click** on the folder → `New File` → name it `index.html`

🔽 Paste this code:

```html
<!DOCTYPE html>
<html>
<head>
    <title>Hello from Docker</title>
</head>
<body>
    <h1>Hello World from HTML in Docker!</h1>
</body>
</html>
```

---

#### 2. Create the Dockerfile:

**File Name:** `Dockerfile`
Right-click → `New File` → name it exactly `Dockerfile` (no extension)

🔽 Paste this code:

```Dockerfile
# Use official Nginx web server image
FROM nginx:alpine

# Copy our HTML file into the default nginx folder
COPY index.html /usr/share/nginx/html/index.html
```

---

### ✅ Step 4: Save and Close VS Code

Use **Ctrl + S** to save all files. Now you're ready to build the Docker image!

---

## 🚀 Step 5: Run Docker Commands from Command Prompt (Windows)

1. Open Command Prompt (Windows + R → `cmd`)
2. Go to your project folder:

```bash
cd Desktop\hello-html-docker
```

3. Build the Docker image:

```bash
docker build -t html-hello .
```

✅ This creates an image named `html-hello`

4. Run the container:

```bash
docker run -d -p 8080:80 html-hello
```

✅ Now open your browser and go to:

```
http://localhost:8080
```

You’ll see your **Hello World from HTML in Docker!** message 🎉

---

## 💡 Tips

* Always **name your file exactly**: `Dockerfile` (no `.txt` or `.docker`)

* You can view the running container:

  ```bash
  docker ps
  ```

* You can stop the container using:

  ```bash
  docker stop <container_id>
  ```

---

## ✅ Summary

| Task                     | How to Do It                               |
| ------------------------ | ------------------------------------------ |
| Create Dockerfile        | Use VS Code in your project folder         |
| Write Dockerfile content | Paste code based on app (HTML/Flask)       |
| Build image              | `docker build -t image-name .`             |
| Run container            | `docker run -d -p 8080:80 image-name`      |
| View in browser          | `http://localhost:8080` or `:5000` (Flask) |

---
