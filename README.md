# 🗂️ File Permission Flowchart & chmod Demo

### 🎓 Specialization:
> Artificial Intelligence & ROS Systems

## 🧑‍🎨 Designer: Abeer Alasmri

---

## 💻 Used Tools

| Tool          | Description                                      |
|---------------|--------------------------------------------------|
| 🐍 Python      | For scripting chmod logic and demo               |
| 🐧 Ubuntu      | Linux environment to manage permissions          |
| 🖥️ VirtualBox  | Virtualization platform to run Ubuntu safely     |

---

## 💡 Project Idea

This mini project visualizes how Linux file permissions work  
and demonstrates changing them using a Python script with chmod.  
It combines both logic + practice in a fun and secure way. 🎯🔐

---

## 🎯 Project Objectives

- Understand file permission structure in Linux.
- Visualize permission flow via a flowchart.
- Use chmod command correctly via Python.
- Learn the importance of applying the right permission levels.

---

## ✅ Requirements

- [ ] Create a flowchart that explains Linux file permissions.
- [ ] Demonstrate chmod in a Python file.
- [ ] Final file permission: rwxrwxr-x
- [ ] Explain the developer joke: "chmod 777 fixed it" 😄

---

## 🧠 Task Description

> Understand Linux file permission rules  
> → Create a flowchart to explain them  
> → Write a Python script to apply chmod  
> → Demonstrate changing to rwxrwxr-x

---

## 📁 Files Table

| 📸 Image/File Name         | 📄 Description                                          |
|---------------------------|---------------------------------------------------------|
|`terminal_output_example_py.png` | Terminal screenshot showing all executed commands       |
|`linux-file-permissions-flowchart.jpg`| Flowchart image explaining the project workflow         |

---

# Understanding File Permissions in Linux💻✨

In Linux, file permissions are divided into three main categories:

## 1. User (Owner)
- The user is the owner of the file or directory.
- Typical permissions include:
  - Read (r): Permission to view the file contents.
  - Write (w): Permission to modify or delete the file.
  - Execute (x): Permission to run the file if it is executable.

## 2. Group
- The group consists of users sharing specific permissions.
- Permissions can be:
  - Read (r): View the file contents.
  - Write (w): Modify the file (if allowed).
  - Execute (x): Execute the file.

## 3. Others
- Others include all users not in the user or group categories.
- Usually:
  - Write (w): Permission is denied to prevent unauthorized changes.
  - Read (r): Allowed if file should be publicly readable.
  - Execute (x): Allowed if executable by all.

## Summary:

| Permission | User (Owner) | Group | Others   |
|------------|--------------|-------|----------|
| Read (r)   | ✔ Allowed    | ✔ Allowed | ✔ Allowed  |
| Write (w)  | ✔ Allowed    | ✔ Allowed | ✘ Denied   |
| Execute (x)| ✔ Allowed    | ✔ Allowed | ✔ Allowed  |

> Write permission is denied to others to protect the system and prevent unauthorized modifications.

---

# 🛠️ How to Run the File and Change Its Permissions

## 🧩 Step 1: Open the Virtual Machine:
Open VirtualBox and run your Ubuntu virtual machine.

---

## 🌐 Step 2: Set the System Language to English (UK):
Before opening the terminal:

1. Go to Settings > Region & Language
2. Choose English (United Kingdom)
3. Click the ✅ green button to apply
4. Log out and back in to activate the setting

---

## 💻 Step 3: Open the Terminal:
Make sure the terminal prompt looks like this:

```bash
yourname@yourname-pc:~$
```
---

## step 4:Create a Python file using nano:
```bash
nano change_permissions.py
```

---

## 🧾step 5: Write the following code inside the file:

After you open the file using the nano command, paste the following Python code:

```python
print("Hello, World! This file will have custom permissions.")
```

---

## 💾step 6:Save and Exit:

To save and exit from the nano editor after writing your code:

- Press CTRL + X → to exit the editor  
- Then press Y → to confirm saving the changes  
- Then press ENTER → to save the file with the same name

✅ Now your Python file is saved and ready to run.

---

## ▶️step 7: Run the Python File to Make Sure It Works:

In the terminal, type the following command to run your file:

```bash
python3 change_permissions.py
```
## ✅ Output:

When you run the command, you should see this result in the terminal:

```bash
Hello, World! This file will have custom permissions.
```

---

### step 8 : 📂 List the file to confirm it exists:

```bash
ls
```

---

### step 9 : 🔐 Change the file permissions using chmod:

To give the file custom permissions, use the following command:

```bash
chmod 775 change_permissions.py
```

---

### step 10:✅ Verify the new permissions:

To check that the file’s permissions were successfully changed, run:

```bash
ls -l change_permissions.py
```
🔸 Note: That’s a lowercase l, *not* the number 1.

### Expected Output:
```bash
-rwxrwxr-x 1 abeer abeer 64 Aug 1 17:51 change_permissions.py
```


### ⚠️ Important Notes Before Running the Commands:

| Section                     | Is It Editable? | Notes / Example                                                                 |
|----------------------------|-----------------|----------------------------------------------------------------------------------|
| yourname@yourname-pc:~$  | ✅ Yes           | ✳️ This appears automatically based on your device username. Example: abeer@abeer-pc:~$ |
| change_permissions.py    | ✅ Yes           | ✳️ This is your file name — you can change it to any custom name, e.g. script.py |
| ls -l                    | ❌ No            | ✅ Note: The l here is a lowercase L, *not* the number 1. Be careful!    |

---
### 🔍 Explanation: How the Permission 775 Was Calculated in Detail

- ✅ Read (4)
- ✅ Write (2)
- ✅ Execute (1)
  
### 🔐 File Permission Calculation in Linux (775)

| 🧑 Group      | ✅ Permissions | ➕ Calculation | 🔢 Value |
|--------------|----------------|----------------|----------|
| Owner        | rwx          | 4 (read) + 2 (write) + 1 (execute) | 7 |
| Group        | rwx          | 4 (read) + 2 (write) + 1 (execute) | 7 |
| Others       | r-x          | 4 (read) + 0 (no write) + 1 (execute) | 5 |

🔚 Resulting Permission Code: `775`
  
---

## 🤡 Explanation of the Joke: 
“chmod 777 fixed it”

This joke is popular among developers because...

> It’s like: “Nothing works? Just give everyone all the permissions!”

Here's what happens:

- chmod 777 gives read + write + execute permission to:
  - The owner
  - The group
  - Others
- It “solves” the issue but opens security risks. 🫣  
It’s like saying:  
> “Oh, the door won’t open? Let’s remove the lock completely!”

✅ It works  
❌ But it’s not the right solution

chmod 777 =  
Give EVERYONE (owner, group, others) full access:
- ✅ Read (4)
- ✅ Write (2)
- ✅ Execute (1)

---

## 🖼️ Project Images & Description:

| 📸 Image                                | 📝 Description                                           |
|----------------------------------------|---------------------------------------------------------|
| ![Terminal Output](/terminal_output_example_py.png) | Terminal output showing chmod result with rwxrwxr-x   |
| ![Flowchart](/linux-file-permissions-flowchart.jpg)     | Visual diagram of Linux file permission structure       |

---

## ✨ What I Learned:

- File permission bits: r, w, x and their numerical values
- How to use chmod securely and effectively
- Risks of using chmod 777
- Visualizing concepts using flowcharts
- Working in a virtual Linux environment safely 🌐🐧

---

> 💡 *Good developers don’t just make things work—they make things secure.* 🔐
