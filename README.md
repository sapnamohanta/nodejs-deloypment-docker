# nodejs-deloypment-docker



---


## 🚀 Deployment Steps

### 🔹 1. Launch EC2 Instance

* Ubuntu 22.04 recommended
* Allow ports `22`, `80`, and `5000` in the security group

### 🔹 2. SSH into EC2

```bash
ssh -i "your-key.pem" ubuntu@your-ec2-public-ip
```

### 🔹 3. Install Docker

```bash
sudo apt update
sudo apt install docker.io -y
sudo systemctl start docker
sudo usermod -aG docker $USER
```

### 🔹 4. Clone Your Repository

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### 🔹 5. Build and Run Container

```bash
docker build -t myapp .
docker run -d -p 5000:5000 myapp
```

Now your app should be accessible at:
`http://<your-ec2-public-ip>:5000`

---

---

## ✅ Expected Outcome

* A containerized application successfully deployed and running on an AWS EC2 instance.
* Scalable and consistent environment via Docker.

---



```

---
