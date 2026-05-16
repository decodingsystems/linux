# 50 Linux Interview Questions (Basic to Advanced)

## Beginner Level
1. **What is Linux?** It is an open-source, Unix-like OS kernel created by Linus Torvalds.
2. **What is the root account?** It is the system administrator account with absolute privileges.
3. **What is the difference between Linux and Unix?** Unix is proprietary; Linux is open-source and based on Unix.
4. **How do you find your current working directory?** Using the `pwd` command.
5. **How can you view hidden files?** `ls -a` or `ls -la`.
6. **What is a "hidden" file in Linux?** Any file starting with a dot (`.`).
7. **What does the `cd` command do?** Changes the current directory.
8. **What does `cd ~` do?** Takes you to the current user's home directory.
9. **How do you create an empty file?** `touch filename`.
10. **How do you read a file's contents?** `cat filename` or `less filename`.
11. **How do you delete a file?** `rm filename`.
12. **How to delete a directory and its contents?** `rm -rf directory_name`.
13. **How do you copy a file?** `cp source target`.
14. **How do you move a file?** `mv source target`.
15. **What is `chmod`?** Used to change file/directory permissions.

## Intermediate Level
16. **Explain file permissions (e.g., 777).** 777 means read (4), write (2), and execute (1) for owner, group, and others.
17. **What is the difference between `su` and `sudo`?** `su` switches the entire user session, while `sudo` runs a single command as another user (usually root).
18. **How do you search for a pattern in a file?** `grep "pattern" filename`.
19. **What is the difference between `> ` and `>>`?** `>` overwrites a file; `>>` appends to a file.
20. **What is the purpose of piping (`|`)?** It sends the standard output of one command as standard input to the next.
21. **How do you view running processes?** `ps aux` or `top`.
22. **What is a daemon?** A background process operating without direct user interaction (like `sshd`).
23. **How do you forcefully kill a process?** `kill -9 PID`.
24. **Difference between `kill` and `killall`?** `kill` terminates by PID; `killall` terminates by process name.
25. **How do you compress a file into a tarball?** `tar -czvf name.tar.gz /folder`.
26. **What is an inode?** A data structure holding metadata about a file (except its name and data).
27. **What is a soft link vs a hard link?** Soft link points to the filename; hard link points to the inode.
28. **How do you create a symlink?** `ln -s target link_name`.
29. **What does `/etc` directory hold?** System-wide configuration files.
30. **What is `crontab`?** A table used to schedule cron jobs (automated tasks).
31. **What command schedules a job?** `crontab -e`.
32. **How do you find a file by name anywhere in system?** `find / -name filename`.
33. **What is the `/dev` folder?** Contains device files (like `/dev/sda` for disks).

## Advanced Level
34. **What happens during the Linux boot process?** BIOS -> MBR -> GRUB -> Kernel -> Init (or Systemd) -> Runlevel programs.
35. **What is `systemd`?** A system and service manager used to bootstrap user space and manage processes.
36. **Difference between TCP and UDP in `/etc/services`?** TCP is reliable/connection-oriented; UDP is fast/connectionless.
37. **How do you troubleshoot network connectivity in Linux?** `ping`, `traceroute`, `netstat`, `ip a`.
38. **What is the `umask`?** It sets default permissions for newly created files and directories.
39. **Explain `awk` vs `sed`.** `awk` is a data extraction/reporting tool; `sed` is a stream editor for text transformations.
40. **How do you mount a USB drive?** `mount /dev/sdb1 /mnt/usb`.
41. **What is LVM (Logical Volume Manager)?** A method of allocating space on mass-storage devices that is more flexible than conventional partitioning.
42. **What's the difference between a zombie and an orphan process?** Zombie has finished but has entry in process table; Orphan's parent has died, adopted by `init`.
43. **How do you kill a zombie process?** You can't kill a zombie directly (it's already dead). Kill its parent process.
44. **What is swapping and thrashing?** Swapping pushes idle memory pages to disk. Thrashing is excessive disk I/O due to constant swapping.
45. **What is a Load Average (e.g., in `top`)?** The average number of processes in a runnable or uninterruptable state over 1, 5, and 15 minutes.
46. **How do you check open ports?** `netstat -tulnp` or `ss -tulnp`.
47. **What is SSH port forwarding?** Tunnelling application ports from the client machine to the server machine over SSH.
48. **Explain the `setuid` bit.** When set on an executable, a user executes it with the privileges of the file owner.
49. **What is a sticky bit?** Placed on directories (like `/tmp`) so only the file owner can delete their files within it.
50. **How do you change your open file descriptor limit?** Edit `/etc/security/limits.conf` and use `ulimit -n`.
