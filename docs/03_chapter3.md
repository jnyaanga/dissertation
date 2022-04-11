# Multiple genetic loci underlie differences in *C. elegans* growth

\chaptermark{Genetics and growth}



## Preface

The Andersen lab is particularly adept at connecting phenotypic variation in a population to unique genetic variants. As a follow-up to the work described in the previous chapter, I was interested in leveraging this expertise to explore how natural genetic variation influenced growth in *C. elegans*. This meant running another long time course experiment (on my golden birthday no less!), digging into a treasure trove of "throw-away" data collected in 2014, and working with a few new strains other than our good pal N2. The following chapter is based off of my work on this project. It is currently in preparation for submission as a first-author manuscript to G3.

## Abstract

Growth rate and body size are complex traits that contribute to the fitness of organisms. The identification of loci that underlie differences in these traits provides insights into the genetic contributions to development. Leveraging *Caenorhabditis elegans* as a tractable metazoan model for quantitative genetics, we can identify genomic regions that underlie differences in growth. We measured post-embryonic growth of the laboratory-adapted wild-type strain (N2) and a wild strain from Hawaii (CB4856), and found differences in body size. Using linkage mapping, we identified three distinct quantitative trait loci (QTL) on chromosomes IV, V, and X that are associated with variation in body size. We further examined these size-associated QTL using chromosome substitution strains and near-isogenic lines, and validated the chromosome X QTL. Additionally, we generated a list of candidate genes for the chromosome X QTL. These genes could potentially contribute to differences in animal growth and should be evaluated in subsequent studies. Our work reveals the genetic architecture underlying animal growth variation and highlights the genetic complexity of body size in *C. elegans* natural populations.

## Introduction

Precise regulation of final body size is essential to the development and fitness of organisms. Although a larger body size can increase competitive advantages, it also requires added time and nutrients to develop @Hone2005-ex. For this reason, mechanisms that control developmental growth rate and ultimate body size are likely under strong natural selection.

The robustness and precision with which animal development is choreographed is still not well understood. Developing systems coordinate the organization and interaction among cells, tissues, and organs at high reproducibility even in the presence of genetic and environmental perturbations. The early developmental biologist C.H. Waddington coined the term "canalization" to describe this biological robustness @Waddington1942-ih. Developmental canalization has been widely studied in human growth [@Tanner1963-wa; @Cameron2012-fz; @Desmond2017-ek], and shown that to achieve an adult height within normal range, shorter individuals tend to undergo accelerated growth whereas taller individuals experience a decreased rate of growth @Hector2012-xi. In this way, the growth curves of individuals, though variable, converge on a narrow range.

To study the phenomenon of organismal size uniformity, considerable precision and throughput is needed, which can be a challenge when working with multicellular organisms. The nematode *Caenorhabditis elegans* presents a powerful model organism to study developmental growth. *C. elegans* has a quick generation time, produces large numbers of genetically identical offspring, and is easily cultured in controlled laboratory conditions (Wood 1988). Furthermore, *C. elegans* post-embryonic development is well characterized and marked by four larval-stage transitions (molts) that separate the *C. elegans* life cycle into five distinct stages: four larval stages (L1-L4) and adult @Singh1978-xi. The timing of these molts determines the completion of stage-specific development [@Zaidel-Bar2010-up; @Monsalve2011-vo], underscoring the importance of developmental growth regulation in *C. elegans.*

We can leverage *C. elegans* natural genetic diversity to connect phenotypic differences to genetic variants [@Evans2021-zr; @Andersen2022-su\]. Two particular strains of interest are the laboratory-adapted wild-type strain, N2, and a wild strain from Hawaii, CB4856. The genetic diversity between these two strains was shown to underlie multiple phenotypic differences, including aggregation behavior, life history traits, and gene expression @Evans2021-zr. Recombinant inbred lines constructed from crosses between the N2 and CB4856 strains each have unique variants derived from each parental background. Performed at a large scale, these populations of recombinant individuals are a powerful tool to identify genomic regions that are correlated with phenotypic variation. Mapping the natural variation underlying phenotypic differences allows for the dissection of genetic networks involved in important biological processes. Many others have taken this approach to study the genetic underpinnings of complex traits [@Evans2021-zr; @Andersen2022-su].

To characterize the genetic basis for variation in body size and growth in *C. elegans*, we first performed a longitudinal study of post-embryonic growth in N2 and CB4856 animals. Although we observed similar patterns in overall growth dynamics, we also noticed small differences in body size at individual time points across development. To study these differences in size, we used linkage mapping to identify three distinct QTL that influence animal size variation. We further assessed each QTL independently using chromosome substitution strains and near-isogenic lines. Doing so, we validated the chromosome X QTL and identified promising candidate genes that could contribute to the differences in size between the N2 and CB4856 strains. Our work provides a framework for future studies to investigate the genetic mechanisms controlling developmental growth and body size in natural populations of *C. elegans*.

## Materials and methods

### Strains

Animals were grown at $20^{\circ}C$ on 6 cm plates of modified nematode growth media (NGMA), containing 1% agar and 0.7% agarose seeded with E. coli OP50 bacteria. Recombinant inbred advanced intercross lines (RIAILs) used for linkage mapping were constructed previously @Andersen2015-uj. The construction of chromosome substitution strains (CSSs) and near isogenic lines (NILs) used for validation is detailed below. Strains are available upon request.

### High-throughput growth assay

Measurements of body size and fluorescence were measured as previously described @Nyaanga2022-zd. Briefly, the N2 and CB4856 strains were propagated for three generations, bleach-synchronized, and titered at a concentration of 1 embryo per $\mu L$ into six replicate 500 mL flasks for a final volume of 25 mL. The following day, arrested L1s were fed HB101 food at a final concentration of OD20 in a final flask volume of 100 mL K medium and HB101 food. Animals were then grown at $20^{\circ}C$ with constant shaking. Flasks were sampled each hour beginning one hour after feeding and continuing for 51 consecutive hours. At each hour, animals were sampled from each flask, treated with sodium azide, imaged with an ImageXpress Nano (Molecular Devices, SanJose, CA) and scored using a large-particle flow cytometer (COPAS BIOSORT, Union Biometrica, Holliston MA). The COPAS BIOSORT platform was used to collect measurements of animal length (TOF) and optical extinction (EXT). Normalized optical extinction (norm.EXT) was previously established as a proxy for animal width. The raw data collected were imported and processed using the easysorter R package @Shimko2014-eb. Processing removed non-animal objects such as bacterial clumps, shed cuticles, and next generation larval animals from the time-course data using the *mclust* R package @Scrucca2016-by.

### High-throughput fitness assay for linkage mapping

For RIAIL phenotyping, we used a high-throughput fitness assay previously described @Andersen2015-uj. In brief, populations of each strain were propagated on NGMA plates for four generations after which gravid adults were bleach-synchronized and embryos from each strain were aliquoted at a concentration of 25-50 embryos/$\mu L$ into 96-well microtiter plates for a final volume of 50 $\mu L$ K medium. The next day, arrested L1s were fed HB101 bacterial lysate (Pennsylvania State University Shared Fermentation Facility, State College, PA; @Garcia-Gonzalez2017-wl ) at a final concentration of 5 mg/mL in K medium and grown to the L4 larval stage for 48 hours at $20^{\circ}C$ with constant shaking. Animals were then sorted using a COPAS BIOSORT platform during which time animal length and width were collected. Measurements collected by the COPAS BIOSORT were processed and analyzed using the easysorter R package @Shimko2014-eb. Well populations of recombinant strains that contained more than 100 or fewer than three individuals were removed from further processing, resulting in an average of 25 independent replicate wells per strain. Differences among strains tested on different days were controlled using a linear model (animal_size \~ experiment_date). In this way, we address only the differences among strains caused by growth and the day-to-day experimental variance is controlled. These residual values are used for plotting.

### Linkage mapping

310 RIAILs (set 2 RIAILs) were phenotyped using the high-throughput assay described above. Linkage mapping was performed for body size traits using the R package linkagemapping (www.github.com/AndersenLab/linkagemapping) as previously described @Brady2019-qg. The genotypic data and residual phenotypic data were merged using the merge_pheno function with the argument set = 2. Quantitative trait loci (QTL) were detected using the fsearch function. This function calculates the logarithm of the odds (LOD) scores for each genetic marker and each trait as $-n(ln(1-R^2)/2ln(10))$ where R is the Pearson correlation coefficient between the RIAIL genotypes at the marker and trait values (Bloom et al. 2013). A significance threshold based on a 5% genome-wide error rate was calculated by permuting the phenotypic values of each RIAIL 1000 times. QTL were identified as the marker with the highest LOD score above the significance threshold. This marker was then integrated into the model as a cofactor and mapping was repeated iteratively until no further significant QTL were identified. Finally, the annotate_lods function was used to calculate the effect size of each QTL. 95% confidence intervals were defined by a 1.5-LOD drop from the peak marker.

### Generation of chromosome substitution strains (CSSs) and near-isogenic lines (NILs)

CSSs were generated from a cross of the N2 and CB4856 strains. These strains were crossed and heterozygous hermaphrodite progeny were mated to each parental genotype for four generations followed by three generations of selfing to ensure homozygosity of the genome. For each cross, PCR amplicons for insertion-deletions (indels) on the left and right sides of chromosomes IV and V were used to confirm progeny genotypes and select non-recombinants within the introgressed region (**S1 Text**). CSSs were whole-genome sequenced to confirm their genotypes. NILs were generated as previously described [@Zdraljevic2017-jd; @Zdraljevic2019-fr; @Evans2018-sj; @Brady2019-qg] by either backcrossing a selected RIAIL or NIL for six generations or de novo by crossing the parental strains N2 and CB4856 to create a heterozygous individual that was then backcrossed for six generations. PCR amplicons for indel variants were used to track the genomic interval (**S1 Text**). NILs were whole-genome sequenced to verify introgressions.

### Statistical analysis of CSS and NIL results

Growth dynamics for CSSs were tested using a modified version of the high-throughput fitness assay for linkage mapping. Animals were propagated on NGMA plates for two generations before gravid adults were bleach-synchronized and embryos from each strain were aliquoted at a concentration of 1 embryo/$\mu L$ into 12-well, flat bottom culture plates. After three days, gravid adults were bleach-synchronized and embryos were titered into 96-well microtiter plates at a concentration of 50 embryos/$\mu L$ for a final volume of 50 $\mu L$ K medium. The next day, arrested L1s were fed HB101 live bacterial food at a final concentration of OD20. Animals were grown for 48 hours at 20°C with constant shaking and then scored using the COPAS BIOSORT platform as before. The raw data collected were again imported and processed using the easysorter R package (Shimko and Andersen 2014). Processing removed non-animal objects such as bacterial clumps, shed cuticles, and next generation larval animals from the time-course data using the *mclust* R package @Scrucca2016-by. Complete pairwise strain comparisons were performed using the TukeyHSD function @Team2014-fu on an ANOVA model with the formula phenotype \~ strain. A *p*-value of *p* \< 0.05 was used as a threshold for statistical significance. Recapitulation was defined by the significance and direction of effect the CSS or NIL had compared to the parental strains.

## Results

### Growth dynamics of the N2 and CB4856 strains

To precisely evaluate *C. elegans* growth dynamics, we previously developed a high-throughput growth assay that integrates image-based and flow-based devices to quantify the growth of thousands of animals over developmental time @Nyaanga2022-zd. We used this assay to collect body size measurements of N2 and CB4856 animals over the course of larval development from the L1 stage through the L4 stage. Briefly, populations of 100,000 animals were cultured in flasks in triplicate for each strain. Every hour after feeding, we sampled the population from each flask (approximately 300 animals per flask), collected images, and measured length (TOF) and width (norm.EXT) of sampled animals using the COPAS BIOSORT platform (Figure S3-1). From these raw body size measurements, we removed non-animal objects using model-based clustering and generated summary statistics to study population changes (Figures S3-2, see Methods). Here, we report mean length and mean width of animals over 51 consecutive developmental time points (**Figure 3-1**). Overall, we observed little divergence in growth behavior between the two strains. As previously reported, we detected continuous growth punctuated by periods of discontinuous growth rate, resulting in visible shifts in length and width over time. Although growth behavior is consistent in both N2 and CB4856 animals, we capture significant differences in animal length and width at individual time points, particularly early in development (Figure S3-4). As animals age we identify fewer time points with significant differences likely due to increased population variance. We find that across all instances where there is a significant difference in animal length, N2 is consistently longer than CB4856. However, this is not the case in animal width as we observe time points where CB4856 is wider than N2 and others where it is thinner.

<img src="img/ch3/fig3-1.png" width="90%"  style="display: block; margin: auto;" />

**Figure 3-1. Quantitative measurements of growth for N2 and CB4856 animals.** Tukey boxplots of mean length **(A)** and mean width **(B)** for the N2 (orange) and CB4856 (blue) strains over developmental time. The horizontal line in the middle of the box is the median, and the box denotes the 25th to 75th quantiles of the data. The vertical line represents the 1.5 interquartile range. Inset plots magnify mean animal size measurements from hour 48. Each point corresponds to the means length or mean width of a population of animals in each well.

### Identification of QTL underlying variation in growth

As a complex trait, developmental growth is likely influenced by many genes as well as the interactions among them. To investigate the genetic basis of differences in growth, we assessed the development of a panel of 310 RIAILs derived from a cross between the N2 and CB4856 strains (set 2 RIAILs, see Methods). In lieu of collecting measurements throughout development, we used body size as a convenient proxy for developmental progression, where fast growth corresponds to large size and slow growth corresponds to small size. After 48 hours of growth, we collected measurements of length and width using a high-throughput fitness assay, and removed wells containing more than 100 or fewer than three animals from downstream processing (see Methods). Doing so, we observed a distribution of both length (**Figure 3-2A**) and width (**Figure 3-2D**) among the RIAILs, indicating that growth rate varies in the strain population. Next, we mapped body length and width separately and obtained three significant QTL (**Figure 3-2B**,**E**). The length-associated QTL, spanning the center of chromosome IV, and the width-associated QTL on the center of chromosome V independently explain approximately 5% of the phenotypic variation among the RIAILs. The third QTL on the right arm of chromosome X explains slightly more variation at 8.6% (**Table 3-1**). Notably, not only did we find distinct QTL for length and width, we also observed QTL with opposite effects on body shape. Strains with the N2 allele on chromosome IV were longer than strains with the CB4856 allele at this location (**Figure 3-2C**). By contrast, strains with the CB4856 alleles on chromosomes V and X were wider than strains with the N2 allele at these loci (**Figure 3-2F**). The identification of distinct QTL for length vs. width indicates that body shape is influenced by multiple genetic mechanisms. Additionally, we scanned the genome for interactions between pairs of genomic markers that could affect the phenotypic distribution of length or width in the RIAILs and identified no significant interactions (Figures S3-5 and S3-6). These data suggest that the three identified loci contain variants that uniquely influence growth rate along multiple axes, where each locus independently affects the longitudinal or circumferential growth of animals.

<img src="img/ch3/fig3-2.png" width="100%"  style="display: block; margin: auto;" />

**Figure 3-2. Linkage mapping identifies three QTL associated with body size.** Histogram of normalized mean body length **(A)** and mean body width **(D)** of the RIAIL population. **(B, E)** Linkage mapping results for mean body length or mean body width are shown with genomic position (x-axis) plotted against the logarithm of the odds (LOD) score (y-axis). X-axis tick marks denote every 5 Mb. Significant QTL are denoted by a red triangle at the peak marker, and blue shading shows the 95% confidence interval around the peak marker. The percentage of the total phenotypic variance in the RIAIL population that is explained by each QTL is shown above the peak marker. **(C, F)** Tukey box plots show the normalized mean length or width (y-axis) of RIAILs split by genotype at the marker with the maximum LOD score (x-axis). Populations of recombinant strains were grown in independent wells. Each point corresponds to the mean value of all well means. Boxes for data from strains with the N2 allele are colored orange, and boxes for data from strains with the CB4856 allele are shown in blue.

**Table 3-1. Body size QTL**

+-----------+----------------+-------------------------+------------+---------+----------------------------+-----------------+
| **Trait** | **Chromosome** | **Interval (bp)**       | **Peak**   | **LOD** | **Variance explained (%)** | **Effect size** |
+:=========:+:==============:+:=======================:+:==========:+:=======:+:==========================:+:===============:+
| Length    | IV             | 6,211,685 - 12,868,784  | 9,392,639  | 3.22    | 5.28                       | -0.229          |
+-----------+----------------+-------------------------+------------+---------+----------------------------+-----------------+
| Width     | V              | 5,371,124 - 12,112,105  | 11,806,498 | 4.54    | 5.59                       | 0.236           |
+-----------+----------------+-------------------------+------------+---------+----------------------------+-----------------+
| Width     | X              | 12,565,734 - 13,173,080 | 12,750,794 | 5.25    | 8.63                       | 0.293           |
+-----------+----------------+-------------------------+------------+---------+----------------------------+-----------------+

### Validation of loci associated with differences in animal size

To validate whether genetic variation between the N2 and CB4856 strains contributes to differences in animal size, we generated chromosome substitution strains (CSSs) for chromosomes IV and V in which the entire chromosome from the N2 strain was introgressed into the CB4856 genetic background and vice versa. We also constructed reciprocal near-isogenic lines (NILs) for chromosomes IV, V, and X. These NILs contain a small genomic segment derived from one parent strain introgressed into the genetic background of the other parent strain. We then measured the length and width of animals after 48 hours of growth and calculated statistical significance in a pairwise manner for each strain (see Methods). For the chromosomes IV and V QTL, we were unable to recapitulate the results observed in the linkage mapping (Figures S3-7** and S3-8). These two QTL each explain only 5% of the total phenotypic variation among the RIAILs and have the smallest effect sizes among the three detected QTL (**Table 3-1**). The inability to validate these QTL suggests a complex genetic architecture that cannot be explained by isolating these loci using CSSs and NILs, or a lack of power to detect differences driven by these QTL in the CSSs and NILs. By contrast, we successfully validated the chromosome X QTL by observing that genotype significantly contributed to differences in body width of NILs (**Figure 3-3**). The strain with the CB4856 allele on chromosome X crossed into the N2 genetic background was significantly wider than the N2 strain (Tukey's HSD, *p*-value = $1.29e^{-10}$). Similarly, the strain with the N2 chromosome X region introgressed into the CB4856 genetic background was significantly thinner than the CB4856 strain (Tukey's HSD, *p*-value = $1.29e^{-10}$). These results confirmed that genetic variation between the N2 and CB4856 strains on chromosome X contributes to the difference in body width between these strains.

<img src="img/ch3/fig3-3.png" width="100%"  style="display: block; margin: auto;" />

**Figure 3-3. NILs validated the chromosome X QTL.** **(A)** Strain genotypes are displayed as colored rectangles (N2: orange, CB4856: blue) for chromosome X (left) and in general for the rest of the chromosomes (right). The solid vertical line represents the peak marker of the QTL. The dashed vertical lines represent the confidence interval. **(B)** Residual mean animal width (x-axis) is plotted as Tukey box plots against strain (y-axis). Each point corresponds to the mean width of a population of animals from each well. The boxes for the parental strains are colored: N2, orange; CB4856, blue. Statistical significance was calculated by Tukey's HSD (\*\*\*\* = *p*-value \< 0.0001).

### Identification of candidate genes in the chromosome X QTL

To identify candidate genes that could underlie variation in body width, we investigated the genes in the chromosome X interval in the N2 strain. We found 151 genes present in this interval and eliminated 96 genes that had no genetic variation in the CB4856 strain (**Table 3-2**). Of the remaining 55 genes, 18 have genetic variation in the amino-acid sequence of a protein (protein-coding variation), and 34 have genetic variation that is not protein-coding (non-coding variation). However, protein-coding variation is just one way in which genetic variation can cause phenotypic variation. We also considered instances where genetic variation causes a change in gene expression. Using an expression QTL (eQTL) dataset that mapped expression differences in another panel of RIAILs (set 1) derived from N2 and CB4856 [@Rockman2009-qy; @Evans2020-db], we identified five genes with eQTL that map to our region of interest. Additionally, we found 17 other genes outside this genomic interval with eQTL that map to this interval, resulting in a total of 72 candidate genes, none of which are located within a hyper-divergent region @Lee2021-wx.

To further narrow our list of genes, we inspected the functional descriptions and gene ontology (GO) annotations for the remaining 72 candidate genes. When considering the 21 genes with protein-coding variation and/or eQTL, one candidate (*ppk-3*) stood out. *ppk-3*, or phosphatidylinositol phosphate kinase 3, is an ortholog of the mammalian PIKfyve. These kinases play important roles in cell communication and membrane trafficking @Gillooly2001-tu. Notably, mutations in *ppk-3* are responsible for a range of developmental defects, including embryonic lethality, developmental arrest, and larval growth delay @Nicot2006-rn. Investigating the sequence read alignments of the N2 and CB4856 strains at the *ppk-3* locus using the Variant Browser on CeNDR @Cook2017-zq, we observed a missense variant in the second exon predicted to encode a serine-to-threonine substitution (S43T). Although this variant is not in a predicted functional domain, it could alter protein function thereby contributing to the observed phenotypic difference. Aside from *ppk-3*, we identified two additional candidate genes when assessing the functional description for the 34 genes with non-coding genetic variation. The first, *nhr-25*, encodes a nuclear hormone receptor orthologous to Ftz-F1 in Drosophila and is required for proper molting and developmental control @Asahina2000-zz. We observed a splice-site variant in the *nhr-25* locus that could disrupt proper RNA splicing. Interestingly, disruption of *nhr-25* often causes embryonic arrest; however, mutants that survive hatching display a squat body stature (Dpy phenotype), suggesting that *nhr-25* could play a role in body size and shape @Gissendanner2000-hs. The second, *bcat-1*, encodes a branched-chain amino acid aminotransferase that, by RNAi screens, is shown to be required for embryonic and larval development @Maeda2001-eo. In the *bcat-1* locus we observe a variant in an intron and in the three prime untranslated region. Together, these results suggest that one or more genes on chromosome X are candidates that need additional study to explain the variation that we observe in animal growth.\

**Table 3-2. Genes in QTL interval for chromosome X**

+----------------------+-------------------------------------------+------------------------+--------------------+------------+
| **No variation**$^a$ | **Protein-coding var and/or eQTL**$^b$    | **Non-coding var**$^c$ | **Other eQTL**$^d$ | **Total**  |
+:====================:+:=========================================:+:======================:+:==================:+:==========:+
| 96                   | 21                                        | 34                     | 17                 | 168        |
+----------------------+-------------------------------------------+------------------------+--------------------+------------+

$^a$Genes within genomic interval with no genetic variation

$^b$Genes within genomic interval with protein-coding variation and/or an eQTL that maps to this interval

$^c$Genes within genomic interval with non-coding variation and no eQTL that maps to this interval

$^d$Genes outside genomic interval with eQTL that maps to this interval

## Discussion

Here, we investigated larval growth of N2 and CB4856 animals from the L1 stage to the L4 stage. Although we observed similarities in the dynamics of growth, we also saw differences in the size of animals across developmental time. We used linkage mapping to investigate these differences and identified three small-effect QTL associated with variation in body size. Two QTL underlie variation in animal width, and a single non-overlapping QTL contributes to differences in animal length. Using NILs, we validated the width-associated QTL on chromosome X and identified candidate genes that could underlie variation in width. Taken together, our results demonstrate the power of leveraging natural genetic variation to examine the genetic architecture of complex traits such as body size and shape.

### A complex genetic architecture underlies differences in body size

As a complex life history trait, developmental growth could be influenced by several loci @Houle1992-vs. In this study, we report three size-associated QTL. Strikingly, we find loci that decouple components of body size, revealing a complex genetic system that influences growth along different axes of the body. Evidence for genetically separate modules underlying distinct aspects of a single trait has been observed in studies of *C. elegans* behavioral patterns where linkage mapping studies using a panel of RIAILs (set 1, @Rockman2009-qy ) identified distinct loci underlying separate aspects of avoidance response to thermal stimuli @Ghosh2015-bw. Here, we identify distinct QTL for length and width, suggesting that different genetic mechanisms control animal growth along the length vs. width directions. This finding is particularly interesting given the differences in general growth dynamics of length compared to width that we found here (**Figure 3-1**) and previously @Nyaanga2022-zd where we observe a simultaneous increase in length and decrease in width at the transition between larval stages.

The results of the linkage mapping experiment identified two broad peaks on chromosomes IV and V associated with length and width respectively, as well as a narrow peak on chromosome X for width. Although we successfully validated the width-associated QTL on chromosome X (**Figure 3-3**), we were unable to validate the other two QTL (Figures S6 and S7). Our inability to recapitulate the results observed in the linkage mapping might be driven by several factors. First, many loci spread across the genome could underlie variation in body size. Under this polygenic model, any region can harbor variants driving our observed phenotypic difference through additive and/or non-additive effects. The contribution of polygenicity to phenotypic variance has previously been explored in *C. elegans*. Studies of fertility and body size in the *C. elegans* multiparental experimental evolution (CeMEE) panel found that a significant fraction of phenotypic variance, nearly 40% for fertility, can be explained by polygenicity @Noble2017-py. Second, the intervals could contain QTL of opposing effects, making it difficult to recapitulate the results observed in the mapping using NILs. Notably, researchers have observed patterns of polygeny and antagonistic-effect loci when investigating *C. elegans* growth and reproduction in nickel stress @Bernstein2019-pq. Third, it is possible that the QTL effects are smaller than 5% and we are underpowered to detect differences driven by these QTL in the CSSs and NILs.

### Candidate genes for variation in body size

Genetic variants underlying complex traits are often elusive [@Rockman2012-pu; @Evans2021-zr]. Ultimately, when searching for QTL, we aim to identify genes contributing to the variation in phenotypes among individuals. Here, we identified candidate genes located in the interval of the chromosome X QTL (**Table 2**). However, complex traits, such as body size, are likely affected by many genes. For example, recent studies of human genetic variation using data from 5.4 million individuals report finding over 12,000 independent loci associated with height @Yengo2022-yw. In the laboratory strain of *C. elegans*, we know many loci that quantitatively affect body size and shape. Mutations in these genes span various classes, including abnormal pharyngeal pumping (Eat), egg-laying defective (Egl), uncoordinated (Unc), abnormal dauer formation (Daf), and several cuticle and body shape classes (Dpy, Lon, Sma, Rol, Sqt) [@Morck2006-pl; @So2011-ls; @Cho2021-xa]. The polygenic nature of complex traits is a recognized barrier in identifying the genes contributing to phenotypic variation in a population [@Boyle2017-bb; @Bernstein2019-pq]. However, we believe that molecular analysis of loci that underlie variation in development-associated traits in natural populations of *C. elegans* is essential to deciphering the evolutionary significance of developmental canalization.

### Comparison with previous QTL studies of *C. elegans* growth

Our mapping results both recapitulate and expand upon previous QTL studies of growth in *C. elegans*. Previously, median body length of mixed-stage animals was mapped using the same panel of RIAILs (set 2) @Andersen2015-uj. A single small-effect (5.7%) QTL in the center of chromosome IV was found, consistent with our findings. Also in this study, the authors mapped median body width (norm.EXT) to three QTL on chromosomes III, IV, and X. We detected an overlapping genomic region on chromosome X in our current study. Discrepancy in the other QTL is likely caused by differences in the body size assay as the previous study measured mixed-stage animals and we focused on synchronized L4 animals. Additionally, others have mapped variation in animal length for a collection of introgression lines produced from the N2 and CB4856 strains at 48 hours after L1 arrest @Snoek2014-tv. Here, investigators found five separate QTL on chromosome IV affecting body size. This result suggests the presence of several independent loci on chromosome IV each contributing to variation in length. Further investigation is necessary to determine whether the overlapping genomic region detected in our current study is in fact separate loci that independently contribute to variation in animal length. Most recently, a group using a *C. elegans* RIL population identified 18 QTL influencing various body-size traits at a range of temperatures, with the majority clustering on chromosome X @Maulana2022-jy. This work not only demonstrates the genetic complexity underlying body-size phenotypes, but also suggests the presence of co-regulatory loci underlying plasticity. *C. elegans* gives investigators a powerful system to better our understanding of the genetic mechanisms that shape growth and environmental sensitivity in natural populations.

## Contributions

This work was supported by the NSF-Simons Center for Quantitative Biology at Northwestern University. Dr. Erik Andersen, Dr. Gaotian Zhang, and Sophia Gibson assisted with the high-throughput sampling.

## Supplement

<img src="img/ch3/supp/S1Fig.png" width="95%"  style="display: block; margin: auto;" />

**Figure S3-1. Raw measurements of animal size.** Raw COPAS BIOSORT of animal length (A) and width (B) for N2 and CB4856 objects are shown here. Each point represents an individual object that was measured.

<img src="img/ch3/supp/S2Fig.png" width="95%"  style="display: block; margin: auto;" />

**Figure S3-2. Mixture modeling of COPAS BIOSORT data was used to prune data.** Mixture models of Gaussian distributions were fit to log transformed animal length (x-axis) and log transformed optical extinction (y-axis). Data from each hour of the experiment was analyzed and processed to remove clusters that did not include animal objects. Panels indicate experimental hours from which data were taken.

<img src="img/ch3/supp/S3Fig.png" width="95%"  style="display: block; margin: auto;" />

**Figure S3-3. Pruned measurements of animal size.** COPAS BIOSORT data of animal length (A) and width (B) after the removal of non-animal objects using model-based clustering methods.

<img src="img/ch3/supp/S4Fig.png" width="100%"  style="display: block; margin: auto;" />

**Figure S3-4. Comparison of means across developmental time points.** Tukey boxplots of mean length **(A)** and mean width **(B)** for N2 (orange) and CB4856 (blue) over developmental time. The horizontal line in the middle of the box is the median, and the box denotes the 25th to 75th quantiles of the data. The vertical line represents the 1.5 interquartile range. Inset plots magnify mean animal size measurements from hour 48. Each point corresponds to the mean of a population from each well. Statistical significance was calculated using a Wilcoxon test (ns = non-significant (*p*-value \> 0.05); \*, \*\*, \*\*\*, and \*\*\*\* = significant (*p*-value \< 0.05, 0.01, 0.001, or 0.0001, respectively).\
\

<img src="img/ch3/supp/S5Fig.png" width="75%"  style="display: block; margin: auto;" />

**Figure S3-5. Two dimensional genome scan for mean animal length.** Log of the odds (LOD) scores are shown for each pairwise combination of loci, split by chromosome. The upper-left triangle contains the epistasis LOD scores and the lower-right triangle contains the LOD scores for the full model. LOD scores are colored, increasing from purple to green to yellow. The LOD scores for the epistasis model are shown on the left of the color scale and the LOD scores for the full model are shown on the right.

<img src="img/ch3/supp/S6Fig.png" width="75%"  style="display: block; margin: auto;" />

**Figure S3-6. Two dimensional genome scan for mean animal width.** Log of the odds (LOD) scores are shown for each pairwise combination of loci, split by chromosome. The upper-left triangle contains the epistasis LOD scores and the lower-right triangle contains the LOD scores for the full model. LOD scores are colored, increasing from purple to green to yellow. The LOD scores for the epistasis model are shown on the left of the color scale and the LOD scores for the full model are shown on the right.

<img src="img/ch3/supp/S7Fig.png" width="100%"  style="display: block; margin: auto;" />

**Figure S3-7. Validating the chromosome IV length-associated QTL.** Strain genotypes are displayed as colored rectangles (N2: orange, CB4856: blue) for chromosome IV (left) and in general for the rest of the chromosomes (right). The solid vertical line represents the peak marker of the QTL. The dashed vertical lines represent the confidence interval. (B) Residual mean animal length (x-axis) is plotted as Tukey box plots against strain (y-axis). Statistical significance was calculated by Tukey's HSD (ns = non-significant, p-value \> 0.05).

<img src="img/ch3/supp/S8Fig.png" width="100%"  style="display: block; margin: auto;" />

**Figure S3-8. Validating the chromosome V width-associated QTL.** Strain genotypes are displayed as colored rectangles (N2: orange, CB4856: blue) for chromosome V (left) and in general for the rest of the chromosomes (right). The solid vertical line represents the peak marker of the QTL. The dashed vertical lines represent the confidence interval. (B) Residual mean animal width (x-axis) is plotted as Tukey box plots against strain (y-axis). Statistical significance was calculated by Tukey's HSD (ns = non-significant, p-value \> 0.05; \* and \*\*\* = significant, p-value \< 0.05 or 0.001 respectively).

#### S3-1 Text. Reagents used to generate CSSs and NILs.

**RIAILs used:**

QX49, QX59, QX61, QX62, QX72, QX78, QX85, QX115, QX123, QX134, QX144, QX160, QX161, QX175, QX226, QX227, QX231, QX240, QX241, QX242, QX243, QX244, QX245, QX248, QX250, QX252, QX253, QX254, QX258, QX261, QX263, QX264, QX265, QX266, QX267, QX268, QX269, QX270, QX271, QX272, QX273, QX274, QX275, QX276, QX277, QX278, QX279, QX280, QX281, QX282, QX283, QX284, QX285, QX286, QX287, QX288, QX289, QX290, QX291, QX293, QX294, QX295, QX296, QX297, QX298, QX299, QX300, QX301, QX302, QX303, QX304, QX305, QX306, QX307, QX309, QX310, QX311, QX314, QX315, QX316, QX318, QX319, QX320, QX321, QX322, QX323, QX324, QX325, QX326, QX327, QX328, QX329, QX330, QX331, QX332, QX333, QX334, QX335, QX336, QX337, QX338, QX339, QX340, QX341, QX343, QX345, QX346, QX347, QX348, QX349, QX350, QX352, QX353, QX354, QX355, QX356, QX357, QX358, QX359, QX360, QX361, QX362, QX363, QX364, QX365, QX366, QX367, QX368, QX369, QX370, QX371, QX372, QX373, QX374, QX375, QX376, QX377, QX378, QX379, QX380, QX381, QX382, QX383, QX384, QX385, QX386, QX387, QX390, QX391, QX392, QX393, QX394, QX395, QX396, QX397, QX398, QX399, QX400, QX401, QX402, QX403, QX404, QX405, QX406, QX407, QX408, QX409, QX410, QX411, QX412, QX413, QX414, QX416, QX417, QX418, QX419, QX420, QX421, QX423, QX424, QX426, QX427, QX428, QX429, QX430, QX431, QX432, QX433, QX434, QX435, QX436, QX437, QX438, QX439, QX440, QX441, QX443, QX444, QX445, QX446, QX447, QX448, QX449, QX450, QX451, QX452, QX453, QX454, QX455, QX456, QX457, QX458, QX459, QX460, QX461, QX463, QX464, QX465, QX466, QX467, QX468, QX469, QX470, QX471, QX472, QX473, QX474, QX475, QX476, QX477, QX478, QX479, QX480, QX481, QX482, QX483, QX484, QX485, QX486, QX487, QX488, QX489, QX490, QX491, QX492, QX493, QX494, QX495, QX496, QX497, QX498, QX500, QX501, QX503, QX506, QX508, QX511, QX512, QX513, QX514, QX515, QX517, QX520, QX521, QX523, QX524, QX525, QX526, QX527, QX528, QX529, QX530, QX531, QX533, QX534, QX538, QX539, QX540, QX542, QX545, QX549, QX550, QX551, QX553, QX554, QX555, QX556, QX557, QX559, QX560, QX561, QX563, QX564, QX565, QX570, QX572, QX573, QX574, QX579, QX580, QX583, QX585, QX587, QX588, QX594, QX596, QX597, QX598

**Reagents to generate CSSs and NILs:**

+-------------+-----------------------------+----------------------+---------------------+---------------------+
| **Strain**  | **Genotype**                | **Constructed from** | **Left primer**     | **Right primer**    |
+=============+=============================+======================+=====================+=====================+
| ECA232      | eanIR152[V, CB4856>N2]      | QX450xN2             | oECA799 & oECA800   | oECA745 & oECA746   |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA575      | eanIR324[IV, N2>CB4856]     | N2xCB4856            | oECA1132 &          | oECA1135 &          |
|             |                             |                      | oECA1133            | oECA1136            |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA597      | eanIR330[IV, CB4856>N2]     | ECA231xN2            | oECA781 & oECA782   | oECA857 & oECA858   |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA599      | eanIR332[IV, N2>CB4856]     | ECA598xCB4856        | oECA781 & oECA782   | oECA857 & oECA858   |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA828      | eanIR359[X, N2>CB4856]      | N2xCB4856            | oECA1313 & oECA1314 | oECA1246 & oECA1247 |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA929      | eanIR411[X, CB4856>N2]      | N2xCB4856            | oECA1313 & oECA1314 | oECA1246 & oECA1247 |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA1058     | eanIR433[V, N2>CB4856]      | ECA1029xCB4856       | oECA1408 & oECA1409 | oECA1341 & oECA1342 |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA1060     | eanIR435[V, N2 > CB4856]    | ECA554xCB4856        | oECA745 & oECA746   | oECA763 & oECA764   |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA1064     | eanIR439[IV, CB4856>N2]     | N2xCB4856            | oECA1131 & oECA1132 | oECA1135 & oECA1136 |
+-------------+-----------------------------+----------------------+---------------------+---------------------+
| ECA2006     | eanIR446[V, CB4856>N2]      | N2xCB4856            | oECA1141 & oECA1142 | oECA1147 & oECA1148 |
+-------------+-----------------------------+----------------------+---------------------+---------------------+

**Primers:**

| **Primer** | **Genomic position** | **Sequence**           |
|------------|----------------------|------------------------|
| oECA745    | V:13,110,045         | tgcagaggtggagtaaccct   |
| oECA746    | V:13,110,045         | ctcggtctctcccccactaa   |
| oECA763    | V:15,121,356         | cgcacattctttatttctggcg |
| oECA764    | V:15,121,356         | atcggccgtttttcacctga   |
| oECA781    | IV:5,110,734         | gagcactttggcgactttcg   |
| oECA782    | IV:5,110,734         | tccgggcaaattagtgtggc   |
| oECA799    | V:7,862,556          | ttctcgctactggaacacgc   |
| oECA800    | V:7,862,556          | tcaagaagcgttgggaagtct  |
| oECA1131   | IV:1,039,851         | tacccaccgcatcaaaacca   |
| oECA1132   | IV:1,039,851         | acaggcgttcaaagacacca   |
| oECA1135   | IV:17,317,014        | tttcagacaggaaagcgcct   |
| oECA1136   | IV:17,317,014        | gttgagagatccggaccgac   |
| oECA1141   | V:144,547            | ctcatgggagtaacctgggc   |
| oECA1142   | V:144,547            | cggtgacaacggagaatcca   |
| oECA1147   | V:20,622,851         | gtttagtaccagcggggcat   |
| oECA1148   | V:20,622,851         | tgcattccgacccaagagac   |
| oECA1246   | X:11,696,902         | tgcggtgggacttttcttgt   |
| oECA1247   | X:11,696,902         | gtcccagcatgtaaccgtct   |
| oECA1313   | X:8,038,337          | gctgtgcaggactggatgta   |
| oECA1314   | X:8,038,337          | tgctttctgatctgtgccgt   |
| oECA1341   | V:7,104,674          | cccatccccacaatgtttcg   |
| oECA1342   | V:7,104,674          | aatcgacgagtggcacttgt   |
| oECA1408   | V:3,778,859          | cacgtgcccttttgcaatga   |
| oECA1409   | V:3,778,859          | gagctcccggaaaactcgaa   |
