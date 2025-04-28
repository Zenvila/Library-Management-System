# Library Management System

This project connects Python with MongoDB and processes images using the Pillow library. It features a graphical user interface built with Tkinter.

## Requirements

Before running the project, you need to install Python, necessary packages, and set up MongoDB on Arch Linux.

## Installation and Setup

### 1. Install Python on Arch Linux

```bash
sudo pacman -S python python-pip
```

Verify the installation:
```bash
python --version
```

### 2. Install Required Python Packages

```bash
pip install pymongo pillow
```

### 3. Install Tkinter on Arch Linux

```bash
sudo pacman -S tk
```

### 4. Set Up MongoDB on Arch Linux

Install MongoDB:
```bash
sudo pacman -S mongodb
```

Enable and start the MongoDB service:
```bash
sudo systemctl enable mongodb
sudo systemctl start mongodb
```

### 5. Run the Project

```bash
# Create and activate virtual environment (recommended)
python -m venv venv
source venv/bin/activate

# Run the application
python task1.py
```

## Project Structure

The project uses the following components:
* **Tkinter**: For the graphical user interface (included with tk package)
* **PIL (Pillow)**: For image processing
* **PyMongo**: For connecting to MongoDB database

## Arch Linux Specific Notes

- If you encounter permissions issues with MongoDB, you may need to adjust the data directory permissions:
  ```bash
  sudo chown -R mongodb:mongodb /var/lib/mongodb
  ```

- For package management, you can also use an AUR helper like `yay` to install packages from the Arch User Repository if needed:
  ```bash
  yay -S python-pymongo
  ```
