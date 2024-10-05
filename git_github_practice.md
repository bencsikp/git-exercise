
# Git and GitHub Practice and Explanation

### 1. **Setting up Git and GitHub**

#### Install Git
1. Download Git from the official site: [Git](https://git-scm.com)
2. Run the following commands to configure Git:
   ```bash
   git config --global user.name "Your Name"
   git config --global user.email "your-email@example.com"
   ```

#### Set up GitHub
- Create a GitHub account at [GitHub](https://github.com).
- Generate an SSH key to connect your local machine to GitHub:
  - Follow this [guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

---

### 2. **Basic Git Commands**

#### **Exercise 1: Create a Git Repository Locally**
1. Create a folder for your project:
   ```bash
   mkdir my-first-git-project
   cd my-first-git-project
   ```
2. Initialize a Git repository:
   ```bash
   git init
   ```
3. Create a new file and commit:
   ```bash
   echo "Hello, Git!" > readme.txt
   git add readme.txt
   git commit -m "Initial commit"
   ```

---

#### **Exercise 2: Making Changes and Checking History**
1. Modify the file:
   ```bash
   echo "This is my first change" >> readme.txt
   git add readme.txt
   git commit -m "Added a line to readme.txt"
   ```
2. View the commit history:
   ```bash
   git log
   ```

---

### 3. **Using GitHub**

#### **Exercise 3: Pushing to GitHub**
1. Create a new repository on GitHub.
2. Link your local repository:
   ```bash
   git remote add origin git@github.com:username/repo-name.git
   git push -u origin master
   ```

---

### 4. **Branching and Merging**

#### **Exercise 4: Creating and Working with Branches**
1. Create a new branch:
   ```bash
   git checkout -b feature-branch
   git add readme.txt
   git commit -m "Added a new feature"
   git checkout master
   git merge feature-branch
   git push origin master
   ```

---

### 5. **Collaborating with GitHub**

#### **Exercise 5: Forking and Pull Requests**
1. Fork a repository on GitHub.
2. Clone the repository and create a branch:
   ```bash
   git clone git@github.com:your-username/forked-repo.git
   git checkout -b fix-bug
   git commit -m "Fixed a bug"
   git push origin fix-bug
   ```

---

### 6. **Handling Merge Conflicts**

#### **Exercise 6: Simulating a Merge Conflict**
1. Create a conflicting branch and merge:
   ```bash
   git checkout -b conflicting-branch
   git add readme.txt
   git commit -m "Added conflicting line"
   git merge conflicting-branch
   ```

---

### 7. **Reverting Changes**

#### **Exercise 7: Undoing Changes**
1. Undo staged and committed changes:
   ```bash
   git reset readme.txt
   git revert HEAD
   ```

---

### **Why Use Branches?**
- **Isolate features or bug fixes**: Keep work separate until it's complete.
- **Collaboration**: Each developer can work on their own branch.
- **Experimentation**: Test changes without affecting the main codebase.

---

### **How to Merge Branches in Git**
1. **Fast-Forward Merge**:
   ```bash
   git merge feature-branch
   ```

2. **Three-Way Merge**:
   ```bash
   git merge feature-branch
   ```

3. **Resolve Merge Conflicts**:
   ```bash
   git add <filename>
   git commit
   ```

---

### **Check Your Git Configuration**
- Check the configured name:
   ```bash
   git config --global user.name
   ```
- Check the configured email:
   ```bash
   git config --global user.email
   ```
