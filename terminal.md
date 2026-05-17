# ⚡ Terminal Cheat Sheet

> The terminal (command line) lets you control your computer with text commands instead of clicking. Faster and more powerful.

---

## 🪟 Windows vs Mac/Linux

| Concept | Windows (PowerShell) | Mac/Linux (Bash) |
|---------|---------------------|-----------------|
| Open terminal | Right-click folder → "Open in Terminal" | Right-click → "Open in Terminal" |
| Home folder | `C:\Users\YourName` | `/Users/YourName` |
| Separator | `\` (backslash) | `/` (forward slash) |

---

## 📂 Navigating

```bash
# Show where you are
pwd               # Print working directory

# List files
ls                # List files (Mac/Linux)
dir               # List files (Windows)
ls -la            # List ALL files including hidden ones
ls -la | less     # List with scrolling

# Change directory
cd folder-name    # Go into a folder
cd ..             # Go up one folder
cd ~              # Go to home folder
cd /              # Go to root (Mac/Linux)
cd C:\            # Go to C: drive (Windows)
cd -              # Go to previous folder
```

---

## 📁 File Operations

```bash
# Create
mkdir new-folder          # Create a folder
touch file.txt            # Create a file (Mac/Linux)
New-Item file.txt         # Create a file (Windows)

# Copy
cp file.txt copy.txt      # Copy file (Mac/Linux)
Copy-Item file.txt copy.txt  # Copy file (Windows)
cp -r folder new-folder   # Copy entire folder

# Move / Rename
mv file.txt new-name.txt  # Rename (or move) a file
mv file.txt folder/       # Move file into folder

# Delete
rm file.txt               # Delete file (Mac/Linux)
Remove-Item file.txt      # Delete file (Windows)
rm -rf folder             # Delete folder and everything inside (BE CAREFUL!)
```

---

## 👀 Viewing Files

```bash
# See file content
cat file.txt              # Print entire file (Mac/Linux)
Get-Content file.txt      # Print entire file (Windows)
head file.txt             # First 10 lines
tail file.txt             # Last 10 lines
less file.txt             # Scroll through file (q to quit)

# Count lines, words, characters
wc file.txt               # Mac/Linux
Measure-Object file.txt   # Windows
```

---

## 🔍 Searching

```bash
# Find text in files (GREP)
grep "search-term" file.txt           # Mac/Linux
Select-String "search-term" file.txt  # Windows
grep -r "search-term" folder/         # Search entire folder

# Find files by name
find . -name "*.js"                   # Find all .js files (Mac/Linux)
Get-ChildItem -Recurse *.js           # Find all .js files (Windows)
```

---

## 🔧 Useful Tricks

```bash
# Clear the screen
clear           # Mac/Linux
cls             # Windows

# Show command history
history         # Mac/Linux
Get-History     # Windows

# Stop a running command
Ctrl + C        # Cancel whatever is running

# Auto-complete
Tab             # Press Tab to auto-complete folder/file names

# Previous commands
Up Arrow        # Go to previous command (saves typing)

# Run multiple commands one after another
command1 && command2    # Run command2 only if command1 succeeds
command1 ; command2     # Run command2 no matter what
command1 | command2     # Send output of command1 into command2 (pipe)
```

---

## 🌐 Network

```bash
# Check if a website is reachable
ping google.com

# See your IP address
curl ifconfig.me          # Mac/Linux
(Invoke-WebRequest ifconfig.me).Content  # Windows

# Download a file
curl -O https://example.com/file.zip    # Mac/Linux
wget https://example.com/file.zip       # If wget is installed
```

---

## 💡 Pro Tips

- Press **Tab** to auto-complete — saves tons of time
- Press **Up Arrow** to reuse previous commands
- Use `Ctrl+C` to stop anything that's stuck
- Use `Ctrl+L` to clear the terminal without losing scroll history
- Put reusable commands in a `.sh` (Mac/Linux) or `.ps1` (Windows) file
- When in doubt, type `--help` after a command (e.g., `git --help`)
