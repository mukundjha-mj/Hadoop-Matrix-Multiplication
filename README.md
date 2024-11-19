# 🚀 Hadoop Matrix Multiplication

> 🧮 A powerful distributed matrix multiplication implementation using Hadoop MapReduce framework.

## 📋 Overview

This repository provides a robust implementation of matrix multiplication using Hadoop's MapReduce paradigm. It efficiently handles large matrices by leveraging distributed computing capabilities.

## ⚙️ Prerequisites

Before you begin, ensure you have the following installed:

- 🐘 Hadoop (HDFS and YARN) properly configured
- ☕ Java Development Kit (JDK)
- 📊 Input matrix files (Matrix_A.txt and Matrix_B.txt)

## 📁 Directory Structure

```plaintext
Matrix_Multiplication/
├── 📦 MatrixMultiplication.jar
├── 📂 input/
│   ├── 📄 Matrix_A.txt
│   └── 📄 Matrix_B.txt
└── 📂 output/
```

## 🚀 Usage Instructions

### 1️⃣ Start Hadoop Services

Launch the Distributed File System:
```bash
$ start-dfs
```

Initialize the Resource Manager:
```bash
$ start-yarn
```

### 2️⃣ Prepare Input Data

Create HDFS input directory:
```bash
$ hdfs dfs -mkdir /input
```

Upload your matrix files:
```bash
$ hdfs dfs -put D:\Matrix_A.txt /input
$ hdfs dfs -put D:\Matrix_B.txt /input
```

### 3️⃣ Run Matrix Multiplication

Execute the MapReduce job:
```bash
$ hadoop jar D:\Matrix_Multiplication\MatrixMultiplication.jar com.mapreduce.wc/MatrixMultiply /input/* /output
```

### 4️⃣ View Results

Check output directory contents:
```bash
$ hdfs dfs -ls /output
```

Display multiplication results:
```bash
$ hdfs dfs -cat /output/part-r-00000
```

Alternative viewing command:
```bash
$ hadoop dfs -cat /output/*
```

### 5️⃣ Cleanup (Optional)

Remove input files:
```bash
$ hdfs dfs -rm /input/*
```

Clean output files:
```bash
$ hdfs dfs -rm /output/*
```

Delete output directory:
```bash
$ hdfs dfs -rmdir /output
```

## 🤝 Contributing

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

Created by Mukund. See `LICENSE` for more information.

## 📬 Contact

Mukund - [@mukundjha-mj](https://www.linkedin.com/in/mukundjha-mj/)

Project Link: [https://github.com/Mukund/hadoop-matrix-multiplication](https://github.com/YourUsername/hadoop-matrix-multiplication)

---
⭐ Star this repository if you find it helpful!
