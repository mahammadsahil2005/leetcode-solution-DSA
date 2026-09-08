# Repository Structure Guide

## Quick Start

This repository is organized by **difficulty level** and **topics**.

```
leetcode-solution-DSA/
├── Easy/
│   ├── 0001-two-sum/
│   │   ├── README.md
│   │   ├── Solution.java
│   │   └── Solution.py
│   └── ...
│
├── Medium/
│   ├── 0002-add-two-numbers/
│   │   ├── README.md
│   │   ├── Solution.java
│   │   └── Solution.py
│   └── ...
│
├── Hard/
│   ├── 0025-reverse-nodes-in-k-group/
│   │   ├── README.md
│   │   ├── Solution.java
│   │   └── Solution.py
│   └── ...
│
└── README.md (Main index)
```

## How to Add a New Problem

### Step 1: Determine Difficulty
Choose: `Easy`, `Medium`, or `Hard`

### Step 2: Create Folder
```bash
mkdir -p Easy/0001-two-sum
```

### Step 3: Add README.md
```bash
cat > Easy/0001-two-sum/README.md << 'EOF'
# 1. Problem Title

**Difficulty:** Easy  
**Topics:** Topic1, Topic2  
**LeetCode Link:** https://leetcode.com/problems/...

## Problem Statement
[Copy from LeetCode]

## Approach
- **Algorithm:** Explanation
- **Time Complexity:** O(n)
- **Space Complexity:** O(1)

## Solution
### Java
[Your code]
EOF
```

### Step 4: Add Solution Files
```bash
cat > Easy/0001-two-sum/Solution.java << 'EOF'
class Solution {
    // Your solution
}
EOF
```

### Step 5: Commit and Push
```bash
git add .
git commit -m "Add solution for 0001-two-sum"
git push origin main
```

## File Naming Conventions

- **Folder:** `NNNN-problem-name` (e.g., `0001-two-sum`)
- **Solution:** `Solution.java`, `Solution.py`, `Solution.cpp`
- **Notes:** `notes.md` (optional for extra explanation)

## Supported Languages

- Java (`.java`)
- Python (`.py`)
- C++ (`.cpp`)
- JavaScript (`.js`)
- Go (`.go`)
- Rust (`.rs`)

## Best Practices

✅ Do:
- Add clear comments explaining logic
- Include time & space complexity analysis
- Test on LeetCode before uploading
- Follow the folder structure
- Use 4-digit problem numbers with leading zeros

❌ Don't:
- Copy solutions without understanding
- Forget complexity analysis
- Mix multiple problems in one file
- Use inconsistent naming

## Example Problem Structure

```
Easy/0001-two-sum/
├── README.md              # Problem description + solution
├── Solution.java          # Java implementation
├── Solution.py            # Python implementation
└── notes.md               # Optional: additional notes
```
