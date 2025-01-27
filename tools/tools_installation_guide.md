## Tool Installation Guide

### Installing Hydra and Related Tools

#### For Linux (Ubuntu):
```bash
# Update package list
sudo apt update

# Install Hydra
sudo apt install -y hydra

# Verify installation
hydra -h
```

#### For Windows:
---
1. Download the latest version of Hydra for Windows from [GitHub](https://github.com/vanhauser-thc/thc-hydra).  
2. Extract the ZIP file to a folder.  
3. Add the folder path to your system's environment variables under `PATH`.  
4. Open `cmd` or `PowerShell` and verify installation:
   ```
   hydra -h
   ```

### Using Browser (Firefox/Chrome) for XSS Testing
- Use the F12 key or fn+F12 key 
- Right-click on the page, and select Inspect from the options.
  
---

### Installing a Web Browser with Dev Tools (for XSS Testing)
---
#### For Linux (Ubuntu):
```bash
# Install Firefox
sudo apt install -y firefox

# Verify installation
firefox --version
```

#### For Windows:
1. Download Firefox from [Mozilla's official site](https://www.mozilla.org/firefox/).
2. Install the browser by following the on-screen instructions.
3. Open Firefox and use `Ctrl + Shift + I` to access Developer Tools.


---
