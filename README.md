# 🚀 `upvuln` - System Update & Cleanup Script

[![License](https://img.shields.io/badge/License-MIT-blue.svg)](https://github.com/vulnquest58/upvuln/blob/main/LICENSE)

`upvuln` is a robust Bash script designed to automate system updates, upgrades, and cleanup tasks on Linux-based systems. With advanced features like **retry logic** , **color-coded output** , and **dependency fixes** , it ensures your system stays secure, clean, and up-to-date with minimal effort.

---

## 📋 Features

- **System Updates** : Automatically updates package lists (`apt update --fix-missing`) with retry logic for resilience.
- **Package Upgrades** : Upgrades all installed packages (`apt full-upgrade -y`) with retry logic to handle intermittent failures.
- **Cleanup** :
    - Removes unused packages (`apt autoremove -y`).
    - Cleans cached package files (`apt autoclean`).
- **Dependency Fixes** : Configures pending packages and fixes broken dependencies using `dpkg --configure -a` and `apt install -f`.
- **Retry Logic** : Retries failed operations up to 100 times with a 1-minute delay between attempts.
- **Color-Coded Output** : Provides clear, visually distinct messages for success (`GREEN`), failure (`RED`), and informational updates (`PURPLE`).
- **Self-Installation** : Moves itself to `/usr/local/bin/` for global accessibility after execution.

---

## 🛠️ Requirements

- A Linux-based system using `APT` (e.g., Ubuntu, Debian).
- Root privileges (script must be run with `sudo`).
- Bash shell installed (default on most Linux distributions).

---

## 📥 Installation

1. **Download the Script** : Clone the repository or download the `upvuln` script directly:
    
```
 wget https://raw.githubusercontent.com/vulnquest58/upvuln/main/upvuln
```
    
2. **Make the Script Executable** : Give the script executable permissions:
    
```
  chmod +x upvuln
```
    
3. **Run the Script** : Execute the script with root privileges:
    
```
  sudo ./upvuln
```
    
4. **Global Accessibility** : After the first run, the script will move itself to `/usr/local/bin/`. You can now run it globally:
    
```
 sudo upvuln
```
    

---

## 🚀 Usage

Simply run the script with root privileges:

```
sudo upvuln
```
![upvuln](https://github.com/user-attachments/assets/ab5edf14-abcb-4398-81a9-0a6f4af7ec7a)

The script will:

1. Update package lists with retry logic (`apt update --fix-missing`).
2. Upgrade installed packages with retry logic (`apt full-upgrade -y`).
3. Remove unused packages (`apt autoremove -y`).
4. Clean cached package files (`apt autoclean`).
5. Fix broken dependencies and configure pending packages.
6. Move itself to `/usr/local/bin/` for global access.

---

## 🔧 Advanced Features

### Retry Logic

If an operation fails (e.g., due to network issues or temporary errors), the script will retry up to **100 times** with a **1-minute delay** between attempts. This ensures resilience and minimizes manual intervention.

### Color-Coded Output

The script uses color-coded messages for better readability:

- **Purple** : Informational messages (e.g., "RUNNING: ...").
- **Green** : Success messages (e.g., "SUCCESS: ...").
- **Red** : Failure messages (e.g., "FAILED: ...").

Example:

```
RUNNING: sudo apt update --fix-missing

SUCCESS: sudo apt update --fix-missing

```
---

## 📜 License

This project is licensed under the **MIT License** . See the [LICENSE](https://chat.qwen.ai/c/LICENSE) file for details.

---
## ⭐ Support

If you find this script useful, please give it a star! Your support helps encourage further development and maintenance.

---
## 📞 Contact

For questions or feedback, feel free to reach out:

- GitHub: [@vulnquest58](https://github.com/vulnquest58)

---

## 📚 Acknowledgments

- Inspired by the need for simple, automated system maintenance tools.
- Thanks to the open-source community for their contributions and support.

---

✨ Thank you for using `upvuln`! ✨
