# 📁 104.6: Create and Change Hard and Symbolic Links

## ✅ What I Did in This Lab
I used common Linux commands to create, verify, and understand how links behave differently from copies. I explored how links are used to manage files efficiently and reduce redundancy.

[EXAM OBJECTIVE 104.6](https://www.lpi.org/our-certifications/exam-101-102-objectives/#104.6_Create_and_change_hard_and_symbolic_links)

[OBJ.104.6 NOTES](https://1drv.ms/w/c/354f1c8d534fbced/EWELnEweb3lCs_fWI_qeU-gBxafGWZxg2Y2ex4vdN3rr7w?e=aM0XQ4)

[OBJ.104.6 LAB](https://1drv.ms/w/c/354f1c8d534fbced/EebFPuWMmvVBq3kvNm9WYggBe8uwQZ6b2pqGn_fO990GGw?e=iJvWbg)

---

## 1️⃣ Create a Test File

### 🔹Create a simple file to use as our target

bash
Copy
Edit
echo "Hello, LPIC-1!" > original.txt

### 🔹View its contents and inode number

bash
Copy
Edit
cat original.txt  
ls -li original.txt

## 2️⃣ 🔗 Create a Hard Link

### 🔹Create a hard link to the original file

bash
Copy
Edit
ln original.txt hardlink.txt

### 🔹Check inode numbers (they should be the same)

bash
Copy
Edit
ls -li original.txt hardlink.txt

### 🔹Modify one file and observe changes in the other

bash
Copy
Edit
echo "Hard links share data." >> hardlink.txt  
cat original.txt
## 3️⃣ 🔗 Create a Symbolic (Soft) Link

### 🔹Create a symbolic link to the original file

bash
Copy
Edit
ln -s original.txt symlink.txt

### 🔹Check symbolic link details

bash
Copy
Edit
ls -l symlink.txt

### 🔹Read the contents of the symbolic link

bash
Copy
Edit
cat symlink.txt

## 4️⃣ 🔍 Delete the Original File

### 🔹Remove the original file and observe behavior

bash
Copy
Edit
rm original.txt

### 🔹Check what happens to each link

bash
Copy
Edit
cat hardlink.txt    # Still works  
cat symlink.txt     # Will fail
## 5️⃣ 🆚 Copy vs Link

### 🔹Copy the hard link to a new file

bash
Copy
Edit
cp hardlink.txt copied.txt

### 🔹Check inode numbers to see the difference

bash
Copy
Edit
ls -li hardlink.txt copied.txt

## 6️⃣ ⚙️ System Administration Use

### 🔹Use symbolic links for version management

bash
Copy
Edit
mkdir -p /opt/tool-v1  
touch /opt/tool-v1/run.sh  
ln -s /opt/tool-v1 /opt/tool
ls -l /opt/tool

### 🔹Update the link to a new version

bash
Copy
Edit
mkdir -p /opt/tool-v2  
ln -sfn /opt/tool-v2 /opt/tool
ls -l /opt/tool

## 🎓 What I Learned
I learned the difference between hard links and symbolic links, including how each behaves when the original file is modified or deleted. Hard links point to the same inode, while symbolic links point to the pathname. This lab helped me understand how linking supports system administration, version control, and efficient file handling. 🧠
