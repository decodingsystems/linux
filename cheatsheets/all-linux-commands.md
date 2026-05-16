# The Ultimate Linux Commands Cheatsheet

## 1. File and Directory Management
- `pwd`: Print Working Directory.
- `ls`: List directory contents (`ls -la`: Long format, all files including hidden).
- `cd [dir]`: Change directory (`cd ..` to go up one level, `cd ~` for home).
- `touch [file]`: Create an empty file or update access timestamp.
- `mkdir [dir]`: Create a new directory (`mkdir -p a/b/c` creates parents if needed).
- `cp [src] [dest]`: Copy file (`cp -r` for recursive directory copy).
- `mv [src] [dest]`: Move or rename file.
- `rm [file]`: Remove file (`rm -rf` forcefully and recursively removes directories).

## 2. Text Viewing and Manipulation
- `cat [file]`: Concatenate and print files on standard output.
- `less [file]`: View file contents one page at a time.
- `head -n 10 [file]`: View the first 10 lines.
- `tail -n 10 [file]`: View the last 10 lines (`tail -f` to follow file changes).
- `grep "pattern" [file]`: Search for a string within a file.
- `awk '{print $1}' [file]`: Pattern scanning and processing language.
- `sed 's/old/new/g' [file]`: Stream editor for text replacement.

## 3. Users and Groups
- `whoami`: Display current user.
- `id`: Display user identity and group affiliations.
- `su [user]`: Switch user.
- `sudo [command]`: Execute a command as superuser.
- `useradd [user]`: Create a new user.
- `passwd [user]`: Change user password.
- `usermod -aG [group] [user]`: Add user to a group.

## 4. File Permissions and Ownership
- `chmod 755 [file]`: Change file mode bits (Read=4, Write=2, Execute=1).
- `chown user:group [file]`: Change file owner and group.

## 5. Process Management
- `ps aux`: Display currently running processes.
- `top` / `htop`: Real-time process monitoring.
- `kill [PID]`: Terminate a process gracefully.
- `kill -9 [PID]`: Terminate a process forcefully.
- `bg`: Resume suspended job in background.
- `fg`: Bring background job to foreground.

## 6. Archiving and Compression
- `tar -cvf archive.tar [dir]`: Create a tar archive.
- `tar -xvf archive.tar`: Extract a tar archive.
- `tar -czvf archive.tar.gz [dir]`: Create a gzip compressed tar archive.
- `zip -r zipfile.zip [dir]`: Zip a folder.
- `unzip zipfile.zip`: Extract a zip file.

## 7. Networking
- `ping [ip/domain]`: Test reachability.
- `ip a`: Show IP addresses and network interfaces.
- `netstat -tulpen` / `ss -tulpen`: Show listening ports.
- `curl [url]`: Transfer data from or to a server.
- `wget [url]`: Download files from the web.
- `ssh user@host`: Connect to a remote machine.
