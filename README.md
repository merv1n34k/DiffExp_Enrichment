# 🧬 Making Sense of RNA-seq Data: Differential Gene Expression and Pathway Analysis (UBDS3_2025 Edition)

Instructor: [Ian Kouzel](mailto:ian.kouzel@gmail.com)  
TAs: **Anastasiia Horlova** and **Oleksii Stroganov**  

UBDS<sup>3</sup> Ukrainian Biological Data Science Summer School  
Location: Uzhhorod, Ukraine

Dates: 27.07-1.08.2025

## Course Schedule

[Schedule](./docs/schedule.md)

## Purpose

This course guides you through differential gene expression analysis—from raw gene count data obtained via RNA-seq experiments to extracting meaningful biological insights. You'll work with real-world datasets to perform exploratory analysis, differential gene expression analysis, and enrichment analysis (including GO, KEGG, Reactome, DOSE, and WikiPathways).

You'll learn how to import and explore data in R/RStudio using the tidyverse, analyze RNA-seq count data with DESeq2, and get hands-on experience with the Bioconductor packages. By the end, you’ll turn your analysis into a fully reproducible R Markdown report.

## Projects

💡 Projects will be disctributed by instructor and TAs among the participants

### 1. Epithelial mesenchymal transition (EMT)

**Study:** Epithelial mesenchymal transition (EMT) in A549 NSCLC cells. TGFbeta was used to induce EMT, RNA isolated and subjected to RNAseq on Illumina HiSeq.  

> **From the authors**: 
> The capacity of cancer cells to undergo epithelial mesenchymal trans-differentiation has been implicated as a factor driving metastasis, through the acquisition of enhanced migratory/invasive cell programs and the engagement of anti-apoptotic mechanisms promoting drug and radiation resistance. Our aim was to define molecular signaling changes associated with mesenchymal trans-differentiation in two KRas mutant NSCLC models. We focused on central transcription and epigenetic regulators predicted to be important for mesenchymal cell survival. 

📄 **References**:  
1. Haley, J.A. et al. (2014). *Altered Transcriptional Control Networks with Trans-Differentiation of Isogenic Mutant KRas NSCLC Models.*  
[Frontiers in Oncology](https://doi.org/10.3389/fonc.2014.00344)  
BioProject: [PRJNA515936](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA515936)
2. Hao, Y., Baker, D., & ten Dijke, P. (2019). *TGF-β-mediated epithelial–mesenchymal transition and cancer metastasis*. *International Journal of Molecular Sciences, 20*(11), 2767. [https://doi.org/10.3390/ijms20112767](https://doi.org/10.3390/ijms20112767) [REVIEW, additional reading]

   
**🧪 Experimental Design for Project 1 (EMT)**

| Sample ID   | Condition   |
|-------------|-------------|
| SRR8460397  | TGFbeta3    |
| SRR8460398  | TGFbeta3    |
| SRR8460399  | Control     |
| SRR8460400  | Control     |

### 2. Glioblastoma [GSE147352, PRJNA798408]

**Study:** Phenotypic and molecular states of IDH1 mutation-induced CD24-positive glioma stem-like cells. 

> **From the authors**:
> Mutations in IDH1 and IDH2 drive the development of gliomas. These genetic alterations promote tumor cell renewal, disrupt differentiation states, and induce stem-like properties. Understanding how this phenotypic reprogramming occurs remains an area of high interest in glioma research. Our data demonstrate that induction of a CD24-positive population is one mechanism by which IDH-mutant tumors acquire stem-like properties. These findings have significant implications for our understanding of the molecular underpinnings of IDH-mutant gliomas.
vs. normal

📄 **References**:  
1. Haddock, S. et al. (2022). *Phenotypic and molecular states of IDH1 mutation-induced CD24-positive glioma stem-like cells.*
[Neoplasia, 28](https://doi.org/10.1016/j.neo.2022.100790)


### 3. Schizophrenia [GSE63738]

💡 General instructions for downloading: not required to do it right away. Will be discussed in detail in Lab 2.
```bash
# Download salmon quantification files for EMT dataset
wget "https://www.dropbox.com/scl/fo/i387hjzocw227bjllf069/AB0Y-Rt3DxCAXMCJKJVGppM?rlkey=4feunl032pfpbr69w9yfj4al4&st=l2deogkv&dl=1" -O TGFbeta_data.zip
# Decompress downloaded folder
unzip TGFbeta_data.zip -d TGFbeta_data

wget "https://www.dropbox.com/scl/fo/uogwkn77jmhvor1rqc8cz/AMER7_che3v0JfUEssh5p0Y?rlkey=55wklf7huqpplfuj08e6e2t80&st=artgap4o&dl=0" -O Glioblastoma_GSE147352.zip
# Decompress downloaded folder
unzip Glioblastoma_GSE147352.zip -d Glioblastoma_GSE147352

# Download salmon quantification files for schizophrenia_GSE63738 dataset
wget "https://www.dropbox.com/scl/fo/u9bbd2p4zub4zh1zz52q4/AHS29ectp5VKqNEgNNGAWMQ?rlkey=r4fey782143i1x7lt0t0jpuav&st=uj1har82&dl=0" -O schizophrenia_GSE63738.zip
# Decompress downloaded folder
unzip schizophrenia_GSE63738.zip -d schizophrenia_GSE63738
```

## 💻 Labs

All lab instructions and code are located in the **Labs** folder.

👉 [Go to Labs Folder to start with labs](labs/)

## ⚙️ Generate htmls or pdfs from md files (in case required)

```bash
# Option1: save manually as a page
# Option2: render with pandoc
# tested on MacOS
brew install pandoc
# html (better)
pandoc README.md -o README.html
# pdf (not everything will be rendered)
pandoc README.md -o README.pdf --pdf-engine=xelatex
```

---

## ✅ Required R packages

```r
# CRAN
tidyverse
DT
# Bioconductor
tximport
DESeq2
AnnotationDbi
org.Hs.eg.db
clusterProfiler
pathview
enrichplot
DOSE
ReactomePA
shiny
```

---

## 📚 Resources

- [DESeq2 Vignette](https://bioconductor.org/packages/devel/bioc/vignettes/DESeq2/inst/doc/DESeq2.html)  
- [clusterProfiler](https://bioconductor.org/packages/release/bioc/html/clusterProfiler.html)
- [GO analysis](https://yulab-smu.top/biomedical-knowledge-mining-book/clusterprofiler-go.html)
- [KEGG analysis](https://yulab-smu.top/biomedical-knowledge-mining-book/clusterprofiler-kegg.html)
- [Wikipathways analysis](https://yulab-smu.top/biomedical-knowledge-mining-book/wikipathways-analysis.html)
- [REACTOME](https://yulab-smu.top/biomedical-knowledge-mining-book/reactomepa.html)
- [DOSE](https://yulab-smu.top/biomedical-knowledge-mining-book/dose-enrichment.html)
- [R for Data Science](https://r4ds.hadley.nz/)
- [Mastering Shiny](https://mastering-shiny.org/)
