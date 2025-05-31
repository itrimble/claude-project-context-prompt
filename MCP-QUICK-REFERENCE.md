# MCP Permission Rules Quick Reference

Copy and paste these permission rules into your Claude configuration. Adjust paths and commands based on your specific development environment.

## File System Access

```bash
# Main development directory (adjust path as needed)
FileSystem(/Users/[username]/Scripts/*)

# Broader home directory access (use with caution)
FileSystem(/Users/[username]/*)

# Specific project directories
FileSystem(/Users/[username]/Developer/*)
FileSystem(/Users/[username]/Projects/*)
```

## Version Control & GitHub

```bash
# Core Git operations
Bash(git *)

# GitHub CLI
Bash(gh repo *)
Bash(gh pr *)
Bash(gh issue *)
Bash(gh auth *)
Bash(gh workflow *)
```

## Development Languages & Runtimes

### Node.js Ecosystem
```bash
Bash(npm *)
Bash(yarn *)
Bash(node *)
Bash(npx *)
```

### Python Development
```bash
Bash(python *)
Bash(pip *)
Bash(pipx *)
Bash(python3 *)
Bash(pip3 *)
```

### iOS/Swift Development
```bash
Bash(xcode-select *)
Bash(swift *)
Bash(swiftc *)
Bash(xcrun *)
Bash(xcodebuild *)
```

### Ruby Development
```bash
Bash(ruby *)
Bash(gem *)
Bash(bundle *)
```

### Java Development
```bash
Bash(java *)
Bash(javac *)
Bash(mvn *)
Bash(gradle *)
```

## Code Editors & IDEs

```bash
# Visual Studio Code
Bash(code *)

# Sublime Text
Bash(subl *)

# Vim/Neovim
Bash(vim *)
Bash(nvim *)
```

## Container & Virtualization

```bash
# Docker
Bash(docker *)
Bash(docker-compose *)

# Kubernetes
Bash(kubectl *)

# Vagrant
Bash(vagrant *)
```

## Database Tools

```bash
# PostgreSQL
Bash(psql *)
Bash(pg_dump *)
Bash(pg_restore *)

# MySQL
Bash(mysql *)
Bash(mysqldump *)

# SQLite
Bash(sqlite3 *)

# MongoDB
Bash(mongo *)
Bash(mongodump *)
```

## Package Managers

```bash
# Homebrew (macOS)
Bash(brew *)

# APT (Ubuntu/Debian)
Bash(apt *)
Bash(apt-get *)

# Chocolatey (Windows)
Bash(choco *)
```

## Build Tools & Task Runners

```bash
# Make
Bash(make *)

# CMake
Bash(cmake *)

# Webpack
Bash(webpack *)

# Vite
Bash(vite *)

# Gulp
Bash(gulp *)
```

## System Utilities

```bash
# Process monitoring
Bash(htop *)
Bash(ps *)
Bash(top *)

# Network tools
Bash(nmap *)
Bash(curl *)
Bash(wget *)

# File operations
Bash(find *)
Bash(grep *)
Bash(sed *)
Bash(awk *)

# Archive tools
Bash(tar *)
Bash(zip *)
Bash(unzip *)
```

## Automation & Configuration

```bash
# Ansible
Bash(ansible *)
Bash(ansible-playbook *)

# Terraform
Bash(terraform *)

# SSH
Bash(ssh *)
Bash(scp *)
```

## Testing & Quality Assurance

```bash
# Jest
Bash(jest *)

# Pytest
Bash(pytest *)

# ESLint
Bash(eslint *)

# Prettier
Bash(prettier *)
```

## Media & Documentation

```bash
# OBS Studio
Bash(obs *)

# FFmpeg
Bash(ffmpeg *)

# ImageMagick
Bash(convert *)
Bash(magick *)
```

## Quick Setup Instructions

1. **Open Claude Desktop** or use Claude Code CLI
2. **Navigate to Permission Settings**
3. **Add Rules One by One:**
   - Click "Add a new rule..."
   - Copy/paste rule from above
   - Set to "Allow"
   - Confirm

4. **Recommended Priority Order:**
   1. File system access to your main dev directory
   2. Git operations
   3. Your primary programming language tools
   4. Code editor commands
   5. Package managers
   6. Additional tools as needed

## Security Notes

- **Start Minimal:** Only add permissions you actually need
- **Review Regularly:** Audit your permission rules periodically  
- **Path Specificity:** Use specific paths rather than broad wildcards when possible
- **Testing:** Verify each rule works as expected after adding

## Environment-Specific Adjustments

### macOS
- Use `/Users/[username]/` for home directory
- Homebrew commands available via `brew *`
- Xcode tools available

### Linux
- Use `/home/[username]/` for home directory
- Package managers vary by distribution (apt, yum, pacman, etc.)

### Windows
- Use `C:\Users\[username]\` for home directory
- PowerShell commands may need `Bash(powershell *)` 
- WSL commands available if using Windows Subsystem for Linux

Remember to replace `[username]` with your actual username!
