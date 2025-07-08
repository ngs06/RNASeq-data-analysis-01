# RNASeq-data-analysis-01
RNA-Seq analysis of GSE96870
This repository contains the full RNA-Seq analysis pipeline for the GEO dataset GSE96870, which investigates transcriptomic changes in the mouse cerbellum under different timepoints post-upper respiratory infection. 
---- 
**Dataset summary
GEO accession : [GSE96870] (https://www.ncbi.nlm.nih.gov/geo/query/acc.cgi?acc=GSE96870)
DOI : [10.1073/pnas.1620415114] (https://doi.org/10.1073/pnas.1620415114)
Citation : **Blackmore, Stephen, et al. "Influenza Infection Triggers Disease in a Genetic Model of Experimental Autoimmune Encephalomyelitis." Proceedings of the National Academy of Sciences, vol. 114, no. 30, 2017, pp. E6107-E6116,  https://doi.org/10.1073/pnas.1620415114. Accessed 8 Jul. 2025.**
Organism : *Mus musculus*
Tissues studied : Cerebellum and Spinal cord
Goal : To study tissue-specific transcriptomic changes in the CNS due to Influenza virus infection that leads to altered immune trafficking in the brain. 

**Analysis overview 
1. Raw data processing
   - Conversion of compressed files into *.csv format
   - Cleaning of sample names
   - Creating sample metadata
  
2. Data analysis
   - Construction of DESeqDataset with design *~condition*
   - Performing differential expression analysis
   - Filtering

3. Data visualization
   - PCA plots using plotPCA()
   - Volcano plot suign ggplot2()

4. Gene annotation
   - Conversion of ENSEMBL gene IDs to Gene symbols ad Entrez ID using biomaRT + org.MM.eg.db
  
5. GO analysis
   - Usage of clusterProfiler to run enrichGO() for biological processes
   - Plotting of results
  
**Session info
R version 4.4.1 (2024-06-14 ucrt)
Platform: x86_64-w64-mingw32/x64
Running under: Windows 11 x64 (build 26100)
**Key packages**
- `DESeq2` v1.42.0
- `biomaRt` v2.56.0
- `clusterProfiler` v4.10.0
- `org.Mm.eg.db` v3.18.0
- `ggplot2` v3.5.1
- `tidyverse` v2.0.0
- `pathview` v1.44.0 
  






