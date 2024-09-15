# Dataset - Code Quality Issues in AI-generated Code

## Overview
This dataset contains AI-generated code samples labeled with specific code quality issues. It is designed to help researchers and developers detect and analyze common quality problems in AI-generated code. The dataset is particularly useful for training machine learning models aimed at detecting issues like parameter reassignment, inefficient loops, and multiple variable declarations.

## Dataset Structure
The dataset is stored in CSV format with the following columns:

- **generated_code**: The AI-generated code snippet.
- **is_quality_issue**: A binary value (`1` for true, `0` for false) indicating whether the code snippet contains a quality issue.
- **quality_info**: A description or label for the specific quality issue found in the code.
- **MultipleVariableDeclarations**: A binary value (`1` for true, `0` for false) indicating if the snippet contains multiple variable declarations in one statement.
- **AvoidReassigningParameters**: A binary value (`1` for true, `0` for false) indicating whether the snippet reassigns function parameters, a poor coding practice.
- **ForLoopCanBeForeach**: A binary value (`1` for true, `0` for false) indicating whether a `for` loop could be optimized by using a `foreach` construct.

### Sample Data
| generated_code               | is_quality_issue | quality_info             | MultipleVariableDeclarations | AvoidReassigningParameters | ForLoopCanBeForeach |
|------------------------------|------------------|--------------------------|------------------------------|----------------------------|---------------------|
| `def foo(x): x = 5`           | 1                | AvoidReassigningParameters| 0                            | 1                          | 0                   |
| `for (int i=0; i<n; i++) {...}`| 1                | ForLoopCanBeForeach       | 0                            | 0                          | 1                   |
| `var a, b = 10;`              | 1                | MultipleVariableDeclarations| 1                          | 0                          | 0                   |

## Usage
This dataset can be used for:
- **Machine Learning**: Train models to automatically detect code quality issues in AI-generated code.
- **Tool Benchmarking**: Evaluate the performance of static analysis tools on AI-generated code.
- **Research**: Analyze the prevalence and types of code quality issues in AI-generated code from tools like ChatGPT and GitHub Copilot.

## File Details
- **File Format**: CSV
- **Programming Languages**: Python

## Citation
If you use this dataset in your research, please cite:
[QualityCheck AI: Detecting Code Quality Issues in AI-
generated code using deep learning](https://drive.google.com/drive/folders/1LrWKvqTs5y52P9OpnsvI044Gvlbpjp9n)
---
