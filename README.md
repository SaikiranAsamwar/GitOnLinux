# Git & Python on AWS Linux  – Adding Files to Repository

This repository demonstrates how to set up **Git**, configure it, create a file, and push it to GitHub.  
It also explains how to launch a Linux instance on AWS EC2.  


## 🚀 Launching a Linux Instance on AWS Console

Follow these steps to launch an EC2 Linux instance on AWS:

1. **Login to AWS Management Console**  
   - Go to [AWS Console](https://aws.amazon.com/console/).  
   - Sign in with your credentials.

2. **Navigate to EC2 Service**  
   - In the search bar, type **EC2** and open the EC2 Dashboard.

3. **Launch Instance**  
   - Click on **Launch Instance** button.  
   - Provide a **Name** for your instance (e.g., `gitlnx`).

4. **Choose Amazon Machine Image (AMI)**  
   - Select **Amazon Linux 2 AMI** (or Ubuntu if preferred).

5. **Select Instance Type**  
   - Choose **t2.micro** (Free Tier eligible).

6. **Key Pair Configuration**  
   - Select an existing key pair or create a new one.  
   - Download the `.pem` key file safely (used for SSH login).

7. **Configure Network**  
   - Default VPC and subnet are fine.  
   - Allow SSH (Port 22) and HTTP (Port 80) if needed.

8. **Storage**  
   - Default storage (8GB) is enough for testing.  

9. **Review and Launch**  
   - Click **Launch Instance**.  
   - Wait until status shows **Running**.

10. **Connect to Instance**  
    - Select your instance → Click **Connect**.  
    - Copy the SSH command and run in terminal:  
      ```bash
      ssh -i /path/to/key.pem ec2-user@<public-ip>
      ```

---

## 🔹 System Setup
```bash
sudo hostnamectl set-hostname gitlnx   # Set hostname
clear                                  # Clear the terminal
sudo yum update                        # Update system packages
```

---

## 🔹 Git Installation & Configuration
```bash
sudo yum install git -y                # Install Git
git --version                          # Check Git version
git config --global user.name "Saikiran Asamwar"     # Set username
git config --global user.email "saikiranasaamwar@gmail.com"  # Set email
git config --list                      # Verify Git configurations
```

---

## 🔹 Python Installation
```bash
sudo yum install python3 -y            # Install Python3
python3 --version                      # Check Python version
```

---

## 🔹 Clone Repository
```bash
git clone https://github.com/SaikiranAsamwar/Demorepo.git   # Clone repo
ls                                                          # List files
cd Demorepo/                                                # Enter repo
ls                                                          # Verify repo files
```

---

## 🔹 File Creation
```bash
touch helloworld.py                   # Create a new file
nano helloworld.py                    # Edit the file and add code
cat helloworld.py                     # View file content
python3 helloworld.py                 # Run the Python script
```

**Example Code in `helloworld.py`:**
```python
print("Saikiran Asamwar")
```

---

## 🔹 Staging & Committing
```bash
git add helloworld.py                 # Stage file
git commit -m "New file is added to the repo"   # Commit changes
git status                            # Check repo status
```

---

## 🔹 Pushing to GitHub
```bash
git push origin main                  # Push commit to GitHub
git pull                              # Pull updates from GitHub
```

---

## 🔹 Verification
```bash
ls                                    # Check repo files
cat helloworld.py                     # Display file content
history                               # Show command history
```

---

## ✅ Final Result
- Launched Linux instance on AWS EC2  
- Installed **Git & Python**  
- Configured Git username & email  
- Cloned repository from GitHub  
- Created `helloworld.py`  
- Added → Committed → Pushed changes to GitHub  

🎉 Your file is now live in the repository!


---

## 👤 Author
**Saikiran Asamwar**  
_A Cloud Enthusiast_  

---
