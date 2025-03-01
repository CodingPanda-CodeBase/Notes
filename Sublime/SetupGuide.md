# Sublime Text Setup for Competitive Programming 👨‍💻

Hi All,

Here is a step by step guide to setup sublime for competitive programming using C++. Sublime Text is a lightweight yet powerful text editor and is best suitable for Competitive Programming.

## 🛠 1. Install Sublime Text
### Windows
1. Download **Sublime Text** from: [https://www.sublimetext.com/download](https://www.sublimetext.com/download)
2. Run the `.exe` file and follow the installation process.
3. Add Sublime to system PATH (Follow video: <LINK>).

### Mac
1. Download from [Sublime’s official site](https://www.sublimetext.com/download).
3. Open Sublime Text and pin it to the Dock.

### Linux (Ubuntu/Debian)
1. Run the following command:
   ```
   wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -
   echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list
   sudo apt update && sudo apt install sublime-text
   ```

## 2. Set Up Build Systems for C++
A **build system** allows you to compile and run your code directly inside Sublime.

### For Windows
1. Open Sublime Text
2. Create code.cpp, input.txt and output.txt in same folder
3. Follow video to adjust the code writing, input and output sections <LINK>
4. Go to **Tools → Build System → New Build System**.
5. Replace the content with:
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
6. Save it as **C++17 Build.sublime-build**.
7. Now, press **Ctrl + B** to compile & run C++ files

### For MacOS
1. To install compiler
   1. Install home brew: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)" ( official site: https://brew.sh/)`
   2. Add path: `export PATH=/opt/homebrew/bin:$PATH`    
   1. `brew install gcc`
   2. `brew install coreutils` (for adding timeout functionality)
3. Open **Sublime Text** and 
4. Create code.cpp, input.txt and output.txt in same folder
5. Follow video to adjust the code writing, input and output sections <LINK>
6. Go to **Tools → Build System → New Build System**.
7. Replace the content with:
  ```json
{
   "cmd" : ["/opt/homebrew/bin/g++-14 $file_name -o $file_base_name && /opt/homebrew/bin/gtimeout 2s ./$file_base_name<input.txt>output.txt"], 
   "selector" : "source.c",
   "shell": true,
   "working_dir" : "$file_path",
}
   ```
8. Save it as **C++17 Build.sublime-build**.
8. Note: We are setting the program timeout to 2 seconds means, program will be auto terminated after 2 secs. It will help to avoid forever execution of programs.

### For Linux
Same steps, just use following snippet:
```json
{
   "cmd" : ["g++ -std=c++14 $file_name -o $file_base_name && timeout 2s ./$file_base_name<input.txt>output.txt"], 
   "selector" : "source.c",
   "shell": true,
   "working_dir" : "$file_path"
}
```


## 5. Useful Shortcuts for Competitive Programming (Windows & Linux)
| **Shortcut**  | **Action** |
|--------------|-----------|
| `Ctrl + B` | Build & Run Code |
| `Ctrl + Shift + P` | Open Command Palette |
| `Ctrl + P` | Quick Open Files |
| `Ctrl + D` | Select Next Occurrence |
| `Ctrl + /` | Toggle Comment |
| `Ctrl + Shift + ↑/↓` | Move Line Up/Down |

## 6. Useful Shortcuts for Competitive Programming (Mac)  
| **Shortcut**  | **Action** |
|--------------|-----------|
| `Cmd + B` | Build & Run Code |
| `Cmd + Shift + P` | Open Command Palette |
| `Cmd + P` | Quick Open Files |
| `Cmd + D` | Select Next Occurrence |
| `Cmd + /` | Toggle Comment |
| `Cmd + Ctrl + ↑/↓` | Move Line Up/Down |

## **6. Optimize Sublime for Fast Coding**
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


Add your comments on youtube video if you are facing any issues: <LINK>

**Happy Coding & Good Luck for your Competitions!**

## ☕Support:
<p><a href="https://www.buymeacoffee.com/anshaj_sharma"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="anshaj_sharma" /></a></p>
