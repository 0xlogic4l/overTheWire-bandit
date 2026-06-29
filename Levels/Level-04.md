# Bandit Level 1 → Level 02

> **Date:** 2026-06-29

> **Difficulty:** ⭐☆☆☆☆

> **Status:** ✅ Completed

---

# Level Goal

The password for the next level is stored in the only human-readable file in the inhere directory.

> info

---

# Enumeration

```bash
# Commands used for reconnaissance

bandit3@bandit:~$ ls
bandit3@bandit:~$ file ./*

```

### Output

```text
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09

./-file00: data
./-file01: data
./-file02: data
./-file03: data
./-file04: data
./-file05: data
./-file06: OpenPGP Public Key
./-file07: ASCII text
./-file08: data
./-file09: Motorola S-Record; binary data in text format
```

---

# Analysis

* This level serves as an introduction to the Bandit wargame.
* The objective is to connect to the Bandit1 server using SSH.
* The provided username and password are used for authentication.
* After logging in, the password for the next level can be found in the `-file07` file located in the home directory.

---

# Solution

```bash
# Final commands used to solve the level

bandit3@bandit:~$ cat ./-file07
```

### Output

```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

---

# 🚩 Flag

```text
6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
```

---

# Explanation

This challenge about files named with special charachter and learn how i read it `-file07` and how i know file type using `file` command.

---

# Commands Learned

| Command  | Purpose               |
| -------- | --------------------- |
| `cd`     | Change Directory       |
| `ls`    |Listing files         |
| `cat`    | Display file contents |
| `file`    | Determine file type |
| `ssh`    | Connect to connect remotly server    |

---

# Notes

> 💡 Add anything worth remembering for future levels.
* The `file` command determine file type.

---

# Common Mistakes

* Using the wrong username or password when connecting via SSH.
* Forgetting to specify the correct port (`-p 2220`).
* Attempting to use command before logging in to the Bandit server.
* Typing the SSH command with incorrect syntax.
* Looking for the password in the wrong directory instead of the home directory.


---

# Takeaways

* Learned how to connect to a remote Linux server using SSH.
* Understood the importance of specifying a custom SSH port when required.
* Practiced reading the contents of a files named with special charachter using the `cat` command.
* Learned that the password from each level is used to authenticate to the next level.
* Gained familiarity with the basic workflow of the OverTheWire Bandit wargame.


---

# References

* https://overthewire.org/wargames/bandit/
* `man <command>`
* Linux documentation
