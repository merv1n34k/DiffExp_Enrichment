# 💻  Lab 2: Load Data and Perform Exploratory Data Analysis

## 📋 Objective

In this lab, you'll learn how to:

- Download and organize RNA-seq quantification data
- Create an experimental design table
- Load transcript-level quantifications using `tximport`
- Perform basic exploratory steps on count data

---

## 📂 What to Do

> 🧠 You will complete this lab using the provided R Markdown template: `lab2_TEMPLATE.Rmd`

### ✅ Steps to follow:

1. **Set up your R Markdown file**
   - Fill in the YAML header (title, author, date).
   - Ensure code chunks are configured correctly.

2. **Describe the project**
   - Briefly explain the goal of the lab and the type of data being used.

3. **Download the data specific for your project (if not provided by course instructors)**
   - Use the provided `bash` code chunks (marked with `eval = FALSE`) to:
     - Create the appropriate folder
     - Download the ZIP archive
     - Unzip the contents in the RStudio Terminal

4. **Create a design table**
   - Construct a `data.frame` linking each sample ID to its experimental condition.

5. **Explore the directory structure**
   - Use `list.files()` to inspect the location of the `quant.sf` files.

6. **Build file paths**
   - Construct the relative paths to your quantification files and name them using sample IDs and conditions.

7. **Load transcript-gene mapping**
   - Load the `tx2gene` CSV file provided (this maps transcripts to genes).

8. **Import data with `tximport`**
   - Use `tximport()` to summarize transcript-level data into gene-level counts.

9. **Preview and explore the result**
   - Examine the structure of the resulting object (`txi`)
   - Look at the count matrix and access specific sample columns

---

## 📝 Notes

- Code chunks that use `bash` should **not be evaluated** when knitting. Make sure `eval = FALSE` is set.
- Perform file operations like unzipping in the **Terminal panel**, not in the R console.
- Use **clear comments** to explain your code logic.
- You'll be using `tidyverse`, `tximport`, and basic data handling functions.

---

## 🚀 Output

You should produce a knitted **HTML report** that includes:

- Short introduction
- Code for all steps above
- Output previews (tables, counts, etc.)
- Comments explaining each step

---

## 📦 Files Provided

- `lab2_TEMPLATE.Rmd` – Starter file for your report. Create your own copy and named it `lab2_data.Rmd`
- `tx2gene.ensembl_custom.v102.csv` – Transcript-to-gene mapping file

---

💡 Let your instructor or TA know if you encounter issues.
