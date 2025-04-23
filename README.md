To install the [`face_recognition`](https://github.com/ageitgey/face_recognition) library on **Windows**, you need a few dependencies set up **before** running `pip install face_recognition`, because it relies on native code (C/C++) and libraries like `dlib`.

### **🧰 1\. Install Python (Recommended: Python 3.7–3.13)**

* Use the official [Python installer](https://www.python.org/downloads/windows/)

* During install: ✅ *Check the box that says* **"Add Python to PATH"**

---

### **⚙️ 2\. Install CMake**

`dlib` needs CMake to build native binaries.

* Download and install from https://cmake.org/download/

* ✅ During install: Select **“Add CMake to system PATH for all users”**

---

### **🛠️ 3\. Install Visual Studio Build Tools**

You **must** install the C++ build tools for Windows:

1. Go to: [https://visualstudio.microsoft.com/visual-cpp-build-tools/](https://visualstudio.microsoft.com/visual-cpp-build-tools/)

2. Install: **Build Tools for Visual Studio**

3. During installation, select:

   * ✅ **C++ build tools**

   * ✅ **Windows 10 SDK** (or 11 if you're on Win11)

---

### **🧪 4\. (Optional but Recommended) Create a Virtual Environment**

`python -m venv face-env`  
`face-env\Scripts\activate`

---

### **📦 5\. Upgrade pip, setuptools, wheel**

`pip install --upgrade pip setuptools wheel`

---

### **📥 6\. Now Install `face_recognition`**

`pip install face_recognition`

If it fails at building `dlib`, try:

`pip install cmake`  
`pip install dlib`  
`pip install face_recognition`

---

## **🧪 To Test If It Worked:**

`python -c "import face_recognition; print('face_recognition installed successfully')"`

---

## **🛑 Common Issues**

| Problem | Solution |
| ----- | ----- |
| `CMake not found` | Make sure it's in the PATH |
| `Build tools not found` | Ensure you installed C++ tools & SDK |
| `dlib build fails` | Try installing dlib first: `pip install dlib` |
| `wheel build fails` | Ensure `wheel`, `setuptools`, `pip` are upgraded |

---

Want me to generate a `.bat` script that automates this? Or are you on WSL instead of native Windows?

