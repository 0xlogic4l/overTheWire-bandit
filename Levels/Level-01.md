 # Bandit Level 1 → Level 02

> **Date:** 2026-06-29

> **Difficulty:** ☆☆☆☆☆

> **Status:** ✅ Completed

---

# Level Goal

The password for the next level is stored in a file called `-` located in the home directory

---

# Enumeration

```bash
# Commands used for reconnaissance
bandit1@bandit:~$ ls
```

### Output

```text
# The current directory contains on file named "-"
```

---

# Analysis

* This level serves as an introduction to the Bandit wargame.
* The objective is to connect to the Bandit1 server using SSH.
* The provided username and password are used for authentication.
* After logging in, the password for the next level can be found in the `-` file located in the home directory.

---

# Solution

```bash
# Final commands used to solve the level
bandit1@bandit:~$ cat ./-
```

### Output

```text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

---

# 🚩 Flag

```text
PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
```

---

# Explanation

This challenge about files named with special charachter like `-`

---

# Commands Learned

| Command  | Purpose               |
| -------- | --------------------- |
| `ls -l`  | Listing files     |
| `cat`    | Display file contents |
| `ssh`    | Connect to connect remotly server    |

---

# Notes

> 💡 Add anything worth remembering for future levels.

* SSH is used to securely connect to a remote Linux server.
* The default SSH port is **22**, but Bandit uses port **2220**.
* The `cat` command displays the contents of a file.
* Always read the challenge description carefully, as it usually contains important connection details.
* The password obtained in each level is used to log in to the next level.


---

# Common Mistakes

* Using the wrong username or password when connecting via SSH.
* Forgetting to specify the correct port (`-p 2220`).
* Attempting to use `cat readme` before logging in to the Bandit server.
* Typing the SSH command with incorrect syntax.
* Looking for the password in the wrong directory instead of the home directory.

---

# Takeaways

* Learned how to connect to a remote Linux server using SSH.
* Understood the importance of specifying a custom SSH port when required.
* Practiced reading the contents of a file using the `cat` command.
* Learned that the password from each level is used to authenticate to the next level.
* Gained familiarity with the basic workflow of the OverTheWire Bandit wargame.


---

# References

* https://overthewire.org/wargames/bandit/
* `man <command>`
* Linux documentation
