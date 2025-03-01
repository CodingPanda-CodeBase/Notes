# 🔥 **Sublime Text Setup for Competitive Programming**

Hi All,

Please follow step by step guide to setup sublime for competitive programming using C++.

Sublime Text is a lightweight yet powerful text editor.


## 🛠 **1. Install Sublime Text**
### **Windows**
1. Download **Sublime Text** from: [https://www.sublimetext.com/download](https://www.sublimetext.com/download)
2. Run the `.exe` file and follow the installation process.
3. Add Sublime to system PATH (Follow video: <LINK>).

### **Mac**
1. Download from [Sublime’s official site](https://www.sublimetext.com/download).
3. Open Sublime Text and pin it to the Dock.

### **Linux (Ubuntu/Debian)**
1. Follow: https://www.geeksforgeeks.org/setting-up-sublime-text-for-competitive-coding-in-cpp14-on-ubuntu/

## 🏗 **2. Set Up Build Systems for C++, Python & Java**
A **build system** allows you to compile and run your code directly inside Sublime.

### **C++ Build System**
1. Open **Sublime Text** and go to **Tools → Build System → New Build System**.
2. Create code.cpp, input.txt and output.txt in same folder
3. Follow video to adjust the code writing, input and output sections <LINK>
4. Replace the content with:
   ```json
    {
        "cmd": [
            "g++.exe", "-std=c++17", "${file}", 
            "-o", "${file_base_name}.exe", 
            "&&", "${file_base_name}.exe", "<", "input.txt", ">", "output.txt"
        ],
        "shell": true,
        "working_dir": "$file_path",
        "selector": "source.cpp",
        "file_regex": "^(.*?):(\\d+):(\\d+):\\s*(.*)$"
    }
   ```
5. Save it as **C++17 Build.sublime-build**.
6. Now, press **Ctrl + B** to compile & run C++ files

---

## 🚀 **4. Install Competitive Programming Plugins**
### **C++ Snippets**
- Install **C++ Competitive Programming Snippets** via **Package Control**.
- Provides templates for **fast I/O, modular exponentiation, etc.**.

---

## 🎯 **5. Useful Shortcuts for Competitive Programming**
| **Shortcut**  | **Action** |
|--------------|-----------|
| `Ctrl + B` | Build & Run Code |
| `Ctrl + Shift + P` | Open Command Palette |
| `Ctrl + P` | Quick Open Files |
| `Ctrl + D` | Select Next Occurrence |
| `Ctrl + /` | Toggle Comment |
| `Ctrl + Shift + ↑/↓` | Move Line Up/Down |

---

## 🔥 **6. Optimize Sublime for Fast Coding**
1. **Enable Auto Save:**  
   - Go to **Preferences → Settings** and add:  
     ```json
     "save_on_focus_lost": true
     ```
2. **Increase File Opening Speed:**  
   - Add this to **Settings**:
     ```json
     "index_files": false
     ```

🚀 **Happy Coding & Good Luck for Competitions!** 🎯

---

Let me know if you need any modifications! 🚀🔥
