# Lab 2: File Permissions and Ownership

## Objective
Understand the `chmod` and `chown` commands, and how Linux handles file security using octal and symbolic permissions.

## Prerequisites
- Linux shell.
- Root or `sudo` access for some commands (specifically for `chown`).

## Exercise 1: Creating a secure script
1. Create a simple bash script:
   ```bash
   echo "echo 'Hello Admin'" > secure_script.sh
   ```
2. Check its default permissions:
   ```bash
   ls -l secure_script.sh
   ```
   *Usually creates as `-rw-r--r--` (644).*
3. Try to execute it:
   ```bash
   ./secure_script.sh
   ```
   *Expected Output: Permission denied.*

## Exercise 2: Using Symbolic chmod
1. Add execute permissions for the user (owner) only:
   ```bash
   chmod u+x secure_script.sh
   ```
2. Verify with `ls -l` (Should be `-rwxr--r--`).
3. Execute it successfully: `./secure_script.sh`

## Exercise 3: Using Octal chmod
Change the permissions so that:
- Owner has full access (read, write, execute) = 4+2+1 = 7
- Group has read and execute = 4+1 = 5
- Others have zero access = 0

```bash
chmod 750 secure_script.sh
ls -l secure_script.sh
```
*Expected Output: `-rwxr-x---`*

## Exercise 4: Changing Ownership
*(Requires sudo privileges)*
1. Create a dummy test file.
   ```bash
   touch system_config.txt
   ```
2. Make it owned by the `root` user and `root` group.
   ```bash
   sudo chown root:root system_config.txt
   ```
3. Verify ownership:
   ```bash
   ls -l system_config.txt
   ```
   *Notice the output shows `root root` instead of your username.*

## Cleanup
```bash
rm secure_script.sh
sudo rm system_config.txt
```
