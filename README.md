# LeetCode Solutions - DSA

A comprehensive collection of LeetCode problems solved in multiple programming languages, organized by topics and difficulty levels.

## 📁 Folder Structure

```
leetcode-solution-DSA/
├── README.md (this file)
├── .gitignore
├── CONTRIBUTING.md (optional)
│
├── Easy/
│   ├── 0001-two-sum/
│   │   ├── README.md
│   │   ├── Solution.java
│   │   ├── Solution.py
│   │   └── Solution.cpp
│   │
│   └── 0009-palindrome-number/
│       ├── README.md
│       └── Solution.java
│
├── Medium/
│   ├── 0011-container-with-most-water/
│   │   ├── README.md
│   │   ├── Solution.java
│   │   ├── Solution.py
│   │   └── notes.md
│   │
│   └── 0002-add-two-numbers/
│       ├── README.md
│       └── Solution.java
│
├── Hard/
│   └── 0025-reverse-nodes-in-k-group/
│       ├── README.md
│       └── Solution.java
│
└── Topics/
    ├── Array/
    ├── LinkedList/
    ├── Stack/
    ├── Queue/
    ├── Tree/
    ├── Graph/
    ├── Dynamic-Programming/
    ├── Greedy/
    ├── Two-Pointers/
    ├── Sliding-Window/
    ├── Hashing/
    └── Sorting/
```

## 📋 Problem Naming Convention

- **Format:** `NNNN-problem-name`
- **NNNN:** 4-digit LeetCode problem number (with leading zeros)
- **problem-name:** Hyphenated problem title

### Examples:
- `0001-two-sum` (Easy)
- `0011-container-with-most-water` (Medium)
- `0025-reverse-nodes-in-k-group` (Hard)

## 📄 File Format for Each Problem

Each problem folder should contain:

### 1. **README.md** - Problem Description
```markdown
# [Problem Number]. Problem Title

**Difficulty:** Easy/Medium/Hard  
**Topics:** Array, Two Pointers, Sliding Window, etc.  
**LeetCode Link:** https://leetcode.com/problems/problem-name

## Problem Statement
[Copy from LeetCode]

## Approach
- **Algorithm:** Brief explanation
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Solution

### Java
[Code snippet]

### Python
[Code snippet]

### C++
[Code snippet]
```

### 2. **Solution.java** (or .py, .cpp, etc.)
```java
class Solution {
    public int maxArea(int[] height) {
        // Solution code here
    }
}
```

### 3. **notes.md** (Optional - for additional notes/approach)

## 🚀 How to Add a New Solution

### Method 1: Using GitHub Web UI

1. Go to your repository
2. Click **"Add file"** → **"Create new file"**
3. Create folder: `Easy/0001-two-sum/README.md`
4. Add problem details
5. Commit with message: `Add solution for 0001-two-sum`
6. Repeat for solution files

### Method 2: Using Git CLI

```bash
# Clone repository
git clone https://github.com/mahammadsahil2005/leetcode-solution-DSA.git
cd leetcode-solution-DSA

# Create problem folder
mkdir -p Easy/0001-two-sum

# Add README
cat > Easy/0001-two-sum/README.md << 'EOF'
# 1. Two Sum
[Add content here]
EOF

# Add solution
cat > Easy/0001-two-sum/Solution.java << 'EOF'
class Solution {
    public int[] twoSum(int[] nums, int target) {
        // Your solution
    }
}
EOF

# Commit and push
git add .
git commit -m "Add solution for 0001-two-sum"
git push origin main
```

## 📊 Supported Languages

- ☕ **Java**
- 🐍 **Python**
- 🔧 **C++**
- 📜 **JavaScript**
- 🎯 **Go**
- 🦀 **Rust**

## 🏷️ Topics Covered

- Array
- LinkedList
- Stack & Queue
- Trees & Graphs
- Dynamic Programming
- Greedy Algorithms
- Two Pointers
- Sliding Window
- Hashing
- Sorting & Searching
- And more...

## 📈 Statistics

- **Total Problems:** 1
- **Easy:** 0
- **Medium:** 1
- **Hard:** 0

## 📝 Guidelines

✅ **Do:**
- Use clear, readable code with comments
- Follow language-specific naming conventions
- Provide time & space complexity analysis
- Test solutions on LeetCode before uploading
- Use the prescribed folder structure

❌ **Don't:**
- Copy solutions without understanding them
- Skip comments for complex logic
- Mix different solutions in one file
- Commit without testing

## 📞 Contributing

Want to add your solutions? 
1. Fork the repository
2. Create a new branch
3. Add your solutions following the structure
4. Submit a pull request

---

**Last Updated:** September 2026  
**Maintained by:** mahammadsahil2005
