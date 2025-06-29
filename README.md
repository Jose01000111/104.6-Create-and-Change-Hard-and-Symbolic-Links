# 📁 104.6: Create and Change Hard and Symbolic Links

## ✅ What I Did in This Lab
I used common Linux commands to create, verify, and understand how links behave differently from copies. I explored how links are used to manage files efficiently and reduce redundancy.

[EXAM OBJECTIVE 104.6](https://www.lpi.org/our-certifications/exam-101-102-objectives/#104.6_Create_and_change_hard_and_symbolic_links)

[OBJ.104.6 NOTES](https://1drv.ms/w/c/354f1c8d534fbced/EWELnEweb3lCs_fWI_qeU-gBxafGWZxg2Y2ex4vdN3rr7w?e=aM0XQ4)

[OBJ.104.6 LAB](https://1drv.ms/w/c/354f1c8d534fbced/EebFPuWMmvVBq3kvNm9WYggBe8uwQZ6b2pqGn_fO990GGw?e=iJvWbg)

---

## 1️⃣ Create a Test File

### 🔹Create a simple file to use as our target

### 🔹View its contents and inode number

![Bnq3NDw](https://github.com/user-attachments/assets/4038e871-77a8-46ad-9e27-a8fd7a424507)

## 2️⃣ 🔗 Create a Hard Link

### 🔹Create a hard link to the original file

### 🔹Check inode numbers (they should be the same)

### 🔹Modify one file and observe changes in the other

![uSzphDt](https://github.com/user-attachments/assets/b7fbdfbb-3d8c-464d-965a-a3711fda09c3)

## 3️⃣ 🔗 Create a Symbolic (Soft) Link

### 🔹Create a symbolic link to the original file

### 🔹Check symbolic link details

### 🔹Read the contents of the symbolic link

![GapzPyO](https://github.com/user-attachments/assets/add9af02-9f6f-40cd-9449-1333feadb50d)

## 4️⃣ 🔍 Delete the Original File

### 🔹Remove the original file and observe behavior

### 🔹Check what happens to each link

![34a5Cte](https://github.com/user-attachments/assets/66b9934a-dcff-4f5d-92b3-4759afa8376e)

## 5️⃣ 🆚 Copy vs Link

### 🔹Copy the hard link to a new file

### 🔹Check inode numbers to see the difference

![u2N3fs0](https://github.com/user-attachments/assets/7fdf4cd9-3fca-46ef-a151-ea69130b3e66)

## 6️⃣ ⚙️ System Administration Use

### 🔹Use symbolic links for version management

![7uF1YWy](https://github.com/user-attachments/assets/29800df5-aa24-4b05-9beb-9e4e0daeb8ca)

### 🔹Update the link to a new version

![0hsSR5P](https://github.com/user-attachments/assets/3026aae4-b3ce-4dcc-95ee-f41a1051b57a)

---

## 🎓 What I Learned
I learned the difference between hard links and symbolic links, including how each behaves when the original file is modified or deleted. Hard links point to the same inode, while symbolic links point to the pathname. This lab helped me understand how linking supports system administration, version control, and efficient file handling. 🧠
