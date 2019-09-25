## README: LT Microbiome and MDRB

### Instructions for utilizing Source Data and R Markdown files for the citation below:

### Title:
Colonizing multidrug-resistant bacteria and the longitudinal evolution of the intestinal microbiome after liver transplantation

#### Running Title:
Liver transplant microbiome and MDRB

#### Authors:
Medini K. Annavajhala, Angela Gomez-Simmonds, Nenad Macesic, Sean B. Sullivan, Anna Kress, Sabrina D. Khan, Marla J. Giddins, Stephania Stump, Grace I. Kim, Ryan Narain, Elizabeth C. Verna, Anne-Catrin Uhlemann

#### Journal:
*Nature Communications*, 2019

***

#### Instructions:
This collection includes R Markdown documents and source data needed to reproduce data analysis and generation of figures for the citation above. All metadata or source files required to reproduce our results, which are shown in the knitr output files (html, pdf), are provided. These files are publicly available at the following Github repository: https://github.com/mka2136/lt_microbiome and as Source Data associated with the citation above.

Importing all .Rmd files into RStudio and running the scripts in the following order will generate all output data reported in our manuscript:

* Step 1: Generating Phyloseq Objects and alpha-Diversity Metrics after QIIME1 OTU-calling (**Phyloseq_Objects.Rmd**)
    + input files
        - inputs/merged.biom
        - inputs/tree.tre 
        - inputs/dups.txt
    + output files: 	
        - inputs/phylo_filtered.RDS
        - inputs/phylo_relabun_filtered.RDS
        - inputs/LT_alpha_div.txt
							
* Step 2: Generating Figure 1: Liver transplant microbiome community (beta-diversity) and MDRB (**Figure1_MDRB_UF.Rmd**)
    + input files: 	
        - inputs/Fig1_metadata.txt
        - inputs/phylo_relabun_filtered.RDS
    + output files: 	
        - Figure1/panelA-1.png
        - Figure1/panelB-1.png
        - Figure1/panelC-1.png
        - Figure1/panelD-1.png
        - Figure1/fig1-1.png
        - Figure1/fig1-1.eps
							
* Step 3: Generating Figure 2: Pre-transplant alpha- and beta-diversity (**Figure2_PreLT_Diversity.Rmd**)
    + input files:
        - inputs/Fig2_metadata.txt
        - inputs/phylo_relabun_filtered.RDS
    + output files: 	
        - Figure2/panelA_stats-1.png
        - Figure2/panelB-1.png
        - Figure2/panelC-1.png
        - Figure2/panelD-1.png
        - Figure2/panelE-1.png
        - Figure2/panelF-1.png
        - Figure2/fig2-1.png
        - Figure2/fig2-1.eps
							
* Step 4: Generating Figure 3: Post-LT microbiome diversity (**Figure3_PostLT_Diversity.Rmd**)
    + input files: 	
        - inputs/Fig3_metadata.txt
        - inputs/phylo_relabun_filtered.RDS
    + output files: 	
        - Figure3/panelA-1.png
        - Figure3/panelA-clme-1.png
        - Figure3/panelB-1.png
        - Figure3/panelB-clme-1.png
        - Figure3/panelC-1.png
        - Figure3/fig3-1.png
        - Figure3/fig3-1.eps							

* Step 5: Differential abundance testing using DESeq2 and Analysis of Composition of Microbiomes (ANCOM) (**Differential_Abundance.Rmd**)
    + input files: 	
        - inputs/differential_abundance_metadata.txt
        - inputs/phylo_filtered.RDS
        - (*Note: this analysis also requires the ANCOM_updated_code.R script located in the "inputs" folder, which is sourced in the R Markdown file*) 
    + output files:	
        - differential_abundance/Supp_Data3.DESEq2_ARLD_preLT.txt
        - differential_abundance/Supp_Data5.DESeq2_MELD_preLT.txt
        - differential_abundance/Supp_Data7.DESeq2_CTP_CvA_preLT.txt
        - differential_abundance/Supp_Data11.DESeq2_peri_v_preLT.txt
        - differential_abundance/Supp_Data12.DESeq2_earlypost_v_periLT.txt
        - differential_abundance/Supp_Data13.DESeq2_late_v_earlypostLT.txt
        - differential_abundance/Supp_Data15.DESeq2_preLT_MDRB_1yr.txt
        - differential_abundance/Supp_Data17.DESeq2_CRE.txt
        - differential_abundance/Supp_Data19.DESeq2_CephRE.txt
        - differential_abundance/Supp_Data21.DESeq2_VRE.txt
        - differential_abundance/Supp_Data23.DESeq2_MDRB.txt
        - differential_abundance/Supp_Data4.ANCOM_ARLD_preLT.txt
        - differential_abundance/Supp_Data6.ANCOM_MELD_preLT.txt
        - differential_abundance/Supp_Data8.ANCOM_CTP_preLT.txt
        - differential_abundance/Supp_Data14.ANCOM_timecategory.txt
        - differential_abundance/Supp_Data16.ANCOM_MDRB_1yr_preLT.txt
        - differential_abundance/Supp_Data18.ANCOM_CRE.txt
        - differential_abundance/Supp_Data20.ANCOM_CephRE.txt
        - differential_abundance/Supp_Data22.ANCOM_VRE.txt
        - differential_abundance/Supp_Data24.ANCOM_MDRB.txt
						
* Step 6: Generating Figure 4: Overview of findings from multivariate models (**Figure4_Hypotheses.Rmd**)
    + input files: 	
        - inputs/Fig4_metadata.txt
    + output files:	
        - Figure4/fig4-1.png

* Step 7: Generating Supplementary Figure 2: Relative abundance of key taxa in patients who did vs. did not develop MDRB (**Supp_Figure2_Key_Taxa_Abundance.Rmd**)
    + input files:	
        - inputs/Supp_Fig2_metadata.txt
        - inputs/phylo_relabun_filtered.RDS
    + output files:	
        - Supp_Figure2/supp_fig2-1.png
