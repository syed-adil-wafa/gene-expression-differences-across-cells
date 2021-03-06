## Characterization of differential cellular expression in human iPSCs and iPSC-derived GABAergic neurons using AmpliSeq

### Summary
This pilot experiment was conducted to characterize the gene expression profiles of human induced pluripotent stem cells (iPSCs) and iPSC-derived GABAergic inhibitory neurons. iPSCs were generated from fibroblasts collected from a patient with Tuberous Sclerosis Complex and a familial control. Whole transcriptome analyses confirmed stem cell identity of iPSCs based on expression of pluripotency genes (*OCT4* (*POU5F1*), *NANOG*, *SOX2*, *FUT4*) and neuronal identity of GABAergic neurons based on expression of neuronal genes (*TUBB3*, *MAP2*, *NCAM1*) and down-regulation of the aforementioned pluripotency genes. Pairwise correlation analysis demonstrated strong positive correlations between all pairs with stronger correlations between cell types than between genotypes indicating successful generation of iPSCs from somatic cells and differentiation of neurons from iPSCs.

### Methods
All experiments were conducted after receiving institutional review board approval. iPSCs were generated from patient fibroblasts and embryoid body GABAergic inhibitory neuron differentiations were performed as described in [Liu *et al.* (2013)](https://www.ncbi.nlm.nih.gov/pubmed/23928500). Neurons were re-plated on poly-D-lysine/laminin coated 12-well plates and allowed to mature for a week prior to RNA isolation. Gene expression was measured using ThermoFisher Scientific Ion AmpliSeq targeted whole transcriptome sequencing. 
#### Filtering and pre-processing genes
For hierarchical cluster analysis, genes with absolute expression values in the bottom 10<sup>th</sup> percentile across samples were filtered out from the dataset. Absolute expression values &le;1.0 rpm were replaced with 1.0 rpm and the entire dataset was then log<sub>10</sub> transformed. Genes with variablility in the bottom 10<sup>th</sup> percentile across samples were then filtered out from the dataset. Finally, genes with &le;log<sub>10</sub>(10.0 rpm) across samples were filtered out from the dataset. For cell identity and correlation analysis, genes were not filtered out as described above.
#### Data and statistical analysis
Downstream data analysis was performed using in-house scripts written in MATLAB 2016a (The MathWorks, Inc.). Hierarchical clustering of gene expression data was performed using the `clustergram` function with `correlation` as the distance metric.

### Results and discussion
Hierarchical clustering segregated the data into two distinctive clusters - one comprising of the iPSC lines and the other comprising of the neuronal lines.
![alt text](https://github.com/syed-adil-wafa/ampliSeq-gene-expression-characterization/blob/master/figures/clustergram.jpg)
Gene expression analyses confirmed stem cell identity of iPSCs based on expression of pluripotency genes (*OCT4*, *NANOG*, *SOX2*, *FUT4*) and neuronal identity of GABAergic neurons based on expression of neuronal genes (*TUBB3*, *MAP2*, *NCAM1*) and down-regulation of the aforementioned pluripotency genes. *NESTIN* (*NES*), a neural progenitor gene, was expressed in both iPSC and neuronal lines. *GFAP*, a glial marker, was not expressed in both iPSC and neuronal lines.
![alt text](https://github.com/syed-adil-wafa/ampliSeq-gene-expression-characterization/blob/master/figures/markers.jpg)
Correlation analysis demonstrated strong positive correlations between (1) control and patient iPSCs, (2) control and patient neurons, (3) control iPSCs and control neurons, and (4) patient iPSCs and patient neurons. 
![alt text](https://github.com/syed-adil-wafa/ampliSeq-gene-expression-characterization/blob/master/figures/scatter%20plots.jpg)
#### Limitations and future directions
Performing more differentiations will increase the number of biological replicates for each cell type and genotype allowing for replicability and statistical analyses to be conducted.

### Acknowledgements
Human Neuron Core: http://www.childrenshospital.org/research/labs/human-neuron-core
<br/> Laboratory of Mustafa Sahin: http://sahin-lab.org/
<br/> Harvard Stem Cell Institute: https://hsci.harvard.edu/

### References
Liu, Y., Liu, H., Sauvey, C., Yao, L., Zarnowska, E.D., & Zhang, S.C. (2013). Directed differentiation of forebrain GABA interneurons from human pluripotent stem cells. *Nature Protocols*, *8*(9), 1670-9. DOI: [10.1038/nprot.2013.106](https://www.ncbi.nlm.nih.gov/pubmed/23928500)
