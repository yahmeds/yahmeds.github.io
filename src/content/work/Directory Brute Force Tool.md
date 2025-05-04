---
title: Directory Brute Force Tool
publishDate: 2024-05-03 00:00:00
img: /assets/pentest.png
img_alt: A developer analyzing network requests on a dark terminal screen
description: |
  A simple but effective brute force directory discovery tool written in Java, built to scan and detect accessible paths on a given web server.
tags:
  - Java
  - Cybersecurity
  - Dev
---

[🔗 View the GitHub repository](https://github.com/yahmeds/Directory-Brute-Force-)

## Overview

This project is a custom directory brute-force scanner developed in Java. It was built as part of a personal initiative to deepen my skills in web application security and network programming.

The tool is designed to help identify exposed or hidden paths on a target server by appending common directory names from a wordlist and checking for valid HTTP responses.

## Key Features

- Wordlist-based directory enumeration
- Real-time status code filtering (ignores 404s)
- CLI-based tool built with simplicity and performance in mind
- Useful for basic reconnaissance or testing web server exposure

## How It Works

The tool takes two inputs:
1. A **base URL**
2. A **wordlist file** (.txt) with potential paths

It then appends each entry from the wordlist to the base URL and performs an HTTP GET request. If the response code is anything other than 404 (Not Found), the result is printed to the console.

Example:
[200] http://example.com/admin
[403] http://example.com/hidden
[301] http://example.com/login

## Usage

Compile the Java code:
```bash
javac Brut.java
```

## Why I Built It

I wanted to understand how tools like **DirBuster** or **Gobuster** work under the hood, and this project allowed me to practice:

- Low-level HTTP handling in Java  
- File I/O and CLI parsing  
- Cybersecurity principles in action  
- Continuous testing with Docker integration

It was also an opportunity to build a small yet functional tool from scratch that could simulate real-world reconnaissance logic.

---

## Final Thoughts

This tool was developed as part of my ongoing self-learning in **cybersecurity**. While it’s intentionally minimalistic, it reflects a strong grasp of **HTTP logic**, **automation**, and **network programming fundamentals**.

> ⚠️ *This tool is for educational and authorized testing only. Do not use it on systems you don't own or have explicit permission to test.*

