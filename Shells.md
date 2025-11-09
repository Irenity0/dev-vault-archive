### 1. Command Prompt (cmd)
**Command Prompt** (or **cmd.exe**) is the default command-line interpreter for Windows. It allows users to execute commands to interact with the operating system, such as navigating directories, managing files, and running scripts.

- **OS**: Windows
- **Uses**: Basic file operations, system commands, batch scripting (`.bat` files) 
- **Example Command**:  

	```cmd
    dir  (Lists files in a directory)
    ```

---

### 2. PowerShell
**PowerShell** is an advanced command-line shell and scripting language developed by Microsoft, designed for automation and system administration. It is more powerful than Command Prompt because it supports object-oriented scripting.

- **OS**: Windows (but also available on Linux/macOS)    
- **Uses**: System administration, automation, task scheduling  
- **Example Command**:

    ```powershell
    Get-ChildItem  (Lists files in a directory, similar to "dir")
    ```

---

### 3. Bash (Bourne Again Shell)
**Bash** is the default shell for most Linux distributions and macOS. It is a command-line interpreter that allows users to execute commands, run scripts, and automate tasks using shell scripting.

- **OS**: Linux, macOS (Windows via WSL or Git Bash)  
- **Uses**: System administration, scripting, automation
- **Example Command**:

	```bash
    ls  (Lists files in a directory, similar to "dir" in cmd)
    ```

---

### Key Differences

| Feature              | **Command Prompt (cmd)** | **PowerShell**                       | **Bash**                    |
| -------------------- | ------------------------ | ------------------------------------ | --------------------------- |
| **Default OS**       | Windows                  | Windows (also on Linux/macOS)        | Linux/macOS                 |
| **Scripting**        | Batch (`.bat` files)     | PowerShell scripts (`.ps1` files)    | Shell scripts (`.sh` files) |
| **Object-Oriented?** | No                       | Yes (Works with objects)             | No                          |
| **Commands**         | Basic                    | Advanced (works with system objects) | Unix-like commands          |
| **Use Case**         | Simple tasks             | System automation                    | Linux/macOS scripting       |

