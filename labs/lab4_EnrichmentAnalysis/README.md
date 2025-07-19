# 💻 Lab 4: Pathway Enrichment Analysis

## 📋 Objective
In this lab, you'll learn how to:
- Perform Gene Ontology (GO) enrichment analysis
- Conduct KEGG pathway over-representation analysis
- Visualize enrichment results with bar plots
- Create pathway diagrams with gene expression overlays
- Interpret biological significance of enriched pathways

---

## 📂 What to Do
> 🧠 You will complete this lab using the provided R Markdown template: `lab4_Enrichment_analysis_TEMPLATE.Rmd`

---

## 🚀 Output
You should produce a knitted **HTML report** that includes:
- GO enrichment bar plots for all three domains
- KEGG pathway results and visualizations
- Pathway diagrams with gene expression color overlays
- Biological interpretation of enriched terms

---

## 📦 Files Provided
- `lab4_Enrichment_analysis_TEMPLATE.Rmd` – Starter file for your report. Create your own copy and name it `lab4_Enrichment_analysis.Rmd`
- Differential expression results from Lab 3: `*_all_genes_results.tsv`

---

## 📊 Expected Results
- Results folder with organized output files:
 - `GO_analysis/` directory containing:
   - GO enrichment tables (MF, CC, BP) in TSV format
   - GO bar plots saved as PDF
 - `KEGG_analysis/` directory containing:
   - KEGG pathway enrichment table
   - Pathway diagrams as PNG files
- Summary of enriched biological processes 

---

## 🧠 Reflection Questions

**Answer these questions in your report:**

1. **GO Analysis Results:** Which GO domain (MF, CC, BP) provided the most informative results for understanding biology of your dataset?

2. **Biological Interpretation:** Look at your top enriched biological processes - do they align with known biology? Research 3 or more processes.

3. **KEGG vs GO:** How do KEGG pathway results complement your GO analysis? What different insights do they provide?

4. **Pathway Visualization:** In your pathview diagrams, what patterns do you observe? Are mostly upregulated or downregulated genes involved?

5. **Statistical Considerations:** Why do we use adjusted p-values and a background universe? What would happen without these?

---

## ⚠️ Common Issues

**Troubleshooting Tips:**

1. **Missing gene IDs:** Some genes may lack Entrez IDs - this is normal, just proceed with available genes

2. **Empty results:** No pathways are enriched, this is also normal, just procceed with other types of the analysis 

3. **Pathway visualization errors:** Check that pathway ID exists and is correctly formatted (e.g., "hsa04820")

4. **File path errors:** Make sure directory structure matches your setup from Lab 3

---

💡 Let your instructor or TA know if you encounter issues.