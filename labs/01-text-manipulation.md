# Lab 1: Text Manipulation Masterclass

## Objective
Learn how to chain basic Linux text processing commands (`grep`, `awk`, `sed`, `sort`, `uniq`) to analyze data efficiently.

## Prerequisites
- A Linux shell.

## Setup
First, create an imaginary server log file named `access.log` to work with:
```bash
cat << EOF > access.log
192.168.1.10 - - [10/Oct/2023:13:55:36] "GET /index.html HTTP/1.1" 200
10.0.0.5 - - [10/Oct/2023:13:56:01] "GET /login HTTP/1.1" 401
192.168.1.10 - - [10/Oct/2023:13:58:12] "POST /login HTTP/1.1" 200
172.16.0.4 - - [10/Oct/2023:14:01:03] "GET /admin HTTP/1.1" 403
192.168.1.10 - - [10/Oct/2023:14:05:00] "GET /dashboard HTTP/1.1" 200
10.0.0.5 - - [10/Oct/2023:14:10:11] "GET /api/data HTTP/1.1" 500
EOF
```

## Exercise 1: Finding specific entries with grep
Find all `403` or `401` unauthorized requests.
```bash
grep "401\|403" access.log
```
*Expected Output:* Shows the `/login` and `/admin` failed requests.

## Exercise 2: Extracting IPs with awk
Extract only the IP addresses (the first column) from the log file.
```bash
awk '{print $1}' access.log
```

## Exercise 3: Counting unique IP occurrences
Chain `awk`, `sort`, and `uniq -c` to find the most active IPs.
```bash
awk '{print $1}' access.log | sort | uniq -c | sort -nr
```
*Expected Output:*
```
      3 192.168.1.10
      2 10.0.0.5
      1 172.16.0.4
```

## Exercise 4: Data Masking with sed
Replace all IP addresses starting with `192.168` with `[REDACTED]` for data privacy.
```bash
sed 's/192.168.[0-9]\+.[0-9]\+/[REDACTED]/g' access.log
```

## Cleanup
```bash
rm access.log
```
