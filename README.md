
# Virus-Overwrite

**Virus-Overwrite** is an educational example of an overwrite virus, written in C. The virus demonstrates how malicious software can overwrite executable files in a directory with its own code, causing data corruption and file loss. This project is meant for educational purposes only and should never be used in production environments.

**Warning**: This project is for educational use only. It should not be run on any system you do not own or control, and should be executed with caution in isolated environments (e.g., virtual machines).

## Table of Contents

1. [Overview](#overview)
2. [How to Build and Run](#how-to-build-and-run)
3. [Program Explanation](#program-explanation)
4. [License](#license)

## Overview

An **Overwrite Virus** is a type of malware that works by overwriting the content of files on an infected system. This virus targets executable files (`.out` files) in the current directory and replaces their contents with the virus's own code, effectively rendering the target files unusable.

Once the virus is executed, it searches for all `.out` files in the directory and overwrites them with its binary content. This makes the files non-functional, and they will no longer execute as intended. The virus also displays a message indicating that the system has been compromised.

### Key Features:
- **Self-replication**: The virus reads its own binary code and injects itself into other `.out` files.
- **File corruption**: Overwrites the contents of the target files, causing them to become unusable.
- **Command-line output**: Displays a message indicating the system has been infected.

## How to Build and Run

### Step 1: Build the Target Program

The target program is a simple executable file that will be overwritten by the virus. To create the target files, run the following commands:

```bash
gcc target.c -o target1.out
gcc target.c -o target2.out
gcc target.c -o target3.out
```

### Step 2: Build the Virus Program

Next, compile the virus program with the following command:

```bash
gcc overwrite.c -o overwrite.out
```

### Step 3: Run the Target Programs

To simulate an infection, first run the target programs:

```bash
./target1.out
./target2.out
./target3.out
```

### Step 4: Run the Virus Program

After running the target programs, execute the virus program to infect the target files:

```bash
./overwrite.out
```

Once the virus has run, you can check the status of the target files by running them again:

```bash
./target1.out
./target2.out
./target3.out
```

The target programs will no longer function as they have been overwritten by the virus.

## Program Explanation

- **Self-Reading Functionality**: The virus reads its own binary code and stores it in a buffer. This allows the virus to replicate itself into other files.
- **Directory Scanning**: The virus scans the current directory for files with the `.out` extension and overwrites them with its own content.
- **Infection Process**: For each matching `.out` file, the virus opens the file in write mode and overwrites its contents, effectively infecting the target file.
- **Message Display**: After completing the infection process, the virus will print a message to the terminal indicating that the system has been compromised. The message will be followed by some ASCII art as a form of demonstration.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

**Note**: This virus is for educational purposes only. Please run this project only in a safe, controlled environment (e.g., a virtual machine) and never on a production system or systems with important data.
```

This version of the `README.md` provides clear documentation on how to use and understand the project, but it omits the actual source code, as per your request. Let me know if you need further modifications!
