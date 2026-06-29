# Bandit Level 0

> **Date:** 2026-06-29

> **Difficulty:** ☆☆☆☆☆

> **Status:** ✅ Completed

---

# Level Goal

Connect to the Bandit server using the provided SSH credentials and retrieve the password for the next level by reading the contents of the `readme` file in the home directory.

---

# Enumeration

```bash
# Commands used for reconnaissance
bandit0@bandit:~$ ls
```

### Output

```text
# The current directory contains on file named "readme"
```

---

# Analysis

* This level serves as an introduction to the Bandit wargame.
* The objective is to connect to the Bandit server using SSH.
* The provided username and password are used for authentication.
* After logging in, the password for the next level can be found in the `readme` file located in the home directory.

---

# Solution

```bash
# Final commands used to solve the level
bandit0@bandit:~$ cat readme
```

### Output

```text
Congratulations on your first steps into the bandit game!!
Please make sure you have read the rules at https://overthewire.org/rules/
If you are following a course, workshop, walkthrough or other educational activity,
please inform the instructor about the rules as well and encourage them to
contribute to the OverTheWire community so we can keep these games free!

The password you are looking for is: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

```

---

# 🚩 Flag

```text
6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR
```

---

# Explanation

The challenge introduces the Bandit wargame and demonstrates how to connect to a remote Linux server using SSH. After successfully logging in with the provided credentials, the `readme` file in the home directory contains the password required to access the next level. This level focuses on basic SSH authentication and reading the contents of a file using the `cat` command.


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
