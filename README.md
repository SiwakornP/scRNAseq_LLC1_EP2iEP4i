# scRNAseq_LLC1_EP2iEP4i
This repository contains code for scRNA-seq analysis in "PGE2-EP2/EP4 signaling elicits immunosuppression by driving the mregDC-Treg axis in inflammatory tumor microenvironment"

## Alignment

FASTQ files were aligned using Cell Ranger (v.3.6) and reference genome mm10 (https://support.10xgenomics.com/single-cell-gene-expression/software/release-notes/build#GRCh38mm10_3.1.0).
```bash
cellranger count  --id=sample_no1 
                  --fastqs=//home/siwakorn/llc1/no1 
                  --sample=no1-control 
                  --transcriptome=//home/siwakorn/ref_genome/10x_ref_3.1.0_July_2018/GRCh38_and_mm10 
                  --r1-length 28 
                  --expect-cells=10000
```

## Analysis in R (v.3.6)
Part1: LLC1.Day6.Rmd

  To elucidate mechanism of EP2 antagonist and EP4 antagonist in LLC1 tumor growth suppression, LLC1-transplated mice were treated with Vechicle (n=2), EP2 antagonist alone (n=1), EP4 antagonist alone (n=1), and EP2 antagonist + EP4 antagonist (n=2) for 6 days and were subjected to scRNA-seq study.
  
Part2: LLC1.TregDepletion.Rmd

   To evaluate contribution of Treg in LLC1 tumor growth, scRNA-seq of Treg Depletion (n=2) and vechicle treated mice (n=2) were performed.

Part3: LLC1.Day1.5.Rmd

   To evaluate temporal effect of  EP2 antagonist and EP4 antagonist, scRNA-seq of EP2 antagonist + EP4 antagonist treated mice (n=3) and vehicle treated mices (n=3) at day 1.5 was performed.
   
## Dependencies
- R v.3.6
- seurat v.3.2.2
- celda v.1.2.4
- clusterProfiler v.3.14.3

## Resource 
Computation time was provided by the Supercomputing services, Human Genome Center, the Institute of Medical Science, the University of Tokyo.
(https://supcom.hgc.jp/english/)

## Feedback
Feedback is always welcome.

You can also reach me by 
- siwakorn.punya@gmail.com
- punyawatthananukool.siwakorn.78a@st.kyoto-u.ac.jp
- siwakorn.pun@mahidol.ac.th
