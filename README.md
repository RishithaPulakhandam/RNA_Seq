### README: De Novo Transcriptome Reconstruction and Differential Gene Expression Analysis

---

#### **Project Title**:  
De Novo Transcriptome Reconstruction and Differential Gene Expression Analysis in G1E and Megakaryocyte Cellular States

---

#### **Project Description**:  
This project aims to analyze RNA-Seq data from G1E cells and megakaryocytes to identify transcript structures and determine differential gene expression. By employing a de novo transcriptome reconstruction approach, the project identifies novel transcripts and isoforms without relying on an annotated reference transcriptome.

---

#### **Data Sources**:  
- **RNA-Seq Data**: Preprocessed reads from G1E and megakaryocyte libraries (GEO Accession: GSE51338).  
- **Annotation File**: RefSeq GTF file (Mouse genome mm10).  
- **Reads**: Downsampled reads specific to chromosome 19 and key genomic loci.  

**Data Files Used**:  
1. Forward and reverse paired-end reads for G1E and megakaryocyte samples.  
2. RefSeq annotation GTF file.  

---

#### **Software and Tools**:  
The following tools were used for analysis:  

1. **Quality Control**:  
   - FastQC: Quality assessment of raw reads.  
   - Trimmomatic: Trimming low-quality bases.  

2. **Mapping**:  
   - HISAT2: Aligning RNA-Seq reads to the reference genome.  

3. **Transcriptome Reconstruction**:  
   - StringTie: Reconstructing transcript structures.  
   - StringTie-Merge: Merging transcript structures across samples.  
   - GFFCompare: Annotating and classifying transcripts.  

4. **Differential Gene Expression Analysis**:  
   - FeatureCounts: Counting reads per transcript.  
   - DESeq2: Statistical analysis for differential expression.  

5. **Visualization**:   
   - Plots: PCA, MA plots, and heatmaps for data interpretation.
     
     <img width="371" alt="image" src="https://github.com/user-attachments/assets/9cbdaf50-392e-4613-8938-7e65df178a68">  <br>
     
     <img width="241" alt="image" src="https://github.com/user-attachments/assets/fcd0367e-6bd8-4ce9-9900-a43448c6a4e7"> <br>
     
     <img width="250" alt="image" src="https://github.com/user-attachments/assets/b7a9469e-fbde-48ce-bd66-1fee3711a9bd"><br>

---

#### **Output Files**:  
1. Transcriptome GTF file with annotated and novel transcripts.  
2. Tabular file with differential expression results, including p-values and fold changes.  
3. Visualization plots (PCA, heatmaps, MA plots).  

---

#### **Key Findings**:  
- Differentially expressed genes between G1E and megakaryocytes were identified.<br>
  230 for adjusted pvalue<0.05<br>
  45 for adjusted pvalue<0.01 - 22 upregulated and 23 Downregulated.<br>
  <img width="509" alt="image" src="https://github.com/user-attachments/assets/0e46817f-ead5-4e3e-a358-87aa9019246d"><br>
- Novel transcripts and isoforms were reconstructed using de novo methods.
  
**Differentially Expressed Transcript Analysis**:  
- **Transcript Selected**: MSTRG.52.1  
- **Criteria Met**: Differential expression with a log2 fold change of 11.231453, surpassing the threshold of ±2.  
- **Corresponding Gene**: Hoxb13  

**Biological Function**:  
- Hoxb13 belongs to the HOX transcription factor family, essential for vertebrate embryonic development, body plan determination, and cell-type differentiation.  
- It plays a significant role in cell proliferation, differentiation, and apoptosis, with particular importance in tissues like the prostate and skin.  
- In hematopoietic systems, Hoxb13 may regulate lineage commitment.

**Expression Details**:  
- **Cell Type**: Higher expression in G1E cells compared to megakaryocyte cells.  
- **Expression Difference**: A log2 fold change of 11.23 corresponds to approximately 2,300 times higher expression in G1E cells.

**Hypothesized Role**:  
- Hoxb13 may contribute to epithelial and hematopoietic cell maturation and differentiation. Its higher expression in G1E cells could indicate a regulatory function specific to this cell type.  

**Epigenetic Regulation**:  
- The gene is known to bind methyl-CpG regions, suggesting its role in epigenetic gene expression regulation.  

**Clinical Relevance**:  
- In humans, orthologs of Hoxb13 are linked to diseases like ductal carcinoma in situ and renal cell carcinoma.  


#### **Dependencies**:  
- Galaxy platform (https://galaxyproject.org/)  
- Datasets from Zenodo (https://zenodo.org/record/583140)  
- Mouse genome assembly (mm10).  

---

#### **Acknowledgments**:  
This analysis is based on the Galaxy Training Network tutorial:  
**Mallory Freeberg, Mo Heydarian**  
“De novo transcriptome reconstruction with RNA-Seq”  
(https://training.galaxyproject.org/training-material/topics/transcriptomics/tutorials/de-novo/tutorial.html)
