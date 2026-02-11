# 🐍 Creating a New Python Project with a Virtual Environment

## ✅ 1️⃣ Using the Terminal

### **Step 1:** Create a project folder.

```bash
mkdir my_project
cd my_project
```

### **Step 2:** Create a virtual environment

```bash
python -m venv venv_name
```

### **Step 3:** Activate the environment

```bash
  cd "path/to/new_project"
```

```bash
   .\venv_name\Scripts\Activate.ps1
```

**Mac/Linux**
```bash
source venv_name/bin/activate
```

### **Step 4:** Install packages

```bash
pip install requests
```

### **Step 5:** Save dependencies

```bash
pip freeze > requirements.txt
```

### **Step 6:** Deactivate

```bash
deactivate
```

## ✅ 2️⃣ Using VS Code

1. Create a new folder

2. Open it in VS Code:

3. Open terminal inside VS Code:

```
Ctrl + `
```

4. Create environment:

```bash
python -m venv venv
```

5. Activate it

Press:
```
Ctrl + Shift + P
```

6. Select:

```
Python: Select Interpreter
```

7. Choose the interpreter inside `venv`

## ✅ 3️⃣ Using PyCharm

1. Open PyCharm
2. Click **New Project**
3. Choose location
4. Select **New Virtualenv Environment**
5. Click **Create**

To install packages:
- File → Settings → Python Interpreter
- Click ➕ to install packages

## 🎯 Best Practice Structure:

```
my_project/
│
├── venv/
├── main.py
├── requirements.txt
└── README.md
```

# 🐍 Setting Up a Virtual Environment for an Existing Python Project

## ✅ 1️⃣ Using Terminal (Existing Project)

### **Step 1:** Navigate to your existing project folder

```bash
  cd path/to/existing_project
```

### **Step 2:** Create a virtual environment inside the project

```bash
python -m venv venv
```

### **Step 3:** Activate the environment

**Windows**
```bash
cd "path/to/existing_project"
```

```bash
   .\venv_name\Scripts\Activate.ps1
```

**Mac/Linux**
```bash
source venv/bin/activate
```

### **Step 4:** Install dependencies

If the project already contains a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

If not, manually install needed packages:
```bash
pip install package_name
```

### **Step 5:** Verify installation

```bash
pip list
```

### **Step 6:** Deactivate when finished

```bash
deactivate
```

## ✅ 2️⃣ Using VS Code (Existing Project)

### **Step 1:** Open the existing project folder

```bash
code path/to/existing_project
```

### **Step 2:** Open terminal inside VS Code

Press:
```
Ctrl + `
```

### **Step 3:** Create virtual environment

```bash
python -m venv venv
```

### **Step 4:** Activate environment

(Use same activation commands as above)

### **Step 5:** Select interpreter

```
Ctrl + Shift + P
```

Search:
```
Python: Select Interpreter
```
Choose the interpreter inside the `venv` folder.

### **Step 6:** Install dependencies

```bash
pip install -r requirements.txt
```

## ✅ 3️⃣ Using PyCharm (Existing Project)

### **Option A:** Open Existing Project

1. Open PyCharm
2. Click **Open**
3. Select your existing project folder

### **Step 2:** Configure Virtual Environment

1. Go to:
   File → Settings → Project → Python Interpreter
2. Click ⚙ → Add Interpreter
3. Choose **New Virtualenv Environment**
4. Select location inside the project
5. Click OK

PyCharm will create and attach the environment.

### **Step 3:** Install dependencies

If `requirements.txt` exists:
- Right-click file → Install requirements

Or manually install via Python Interpreter settings.

## 🎯 Recommended Structure for Existing Project:

```
existing_project/
│
├── venv/
├── src/
├── requirements.txt
├── README.md
└── main.py
```

## ✅ Best Practice Tips:

- Always create the virtual environment inside the project folder.
- Never upload the `venv/` folder to GitHub (add it to `.gitignore`).
- Always use `requirements.txt` for reproducibility.
