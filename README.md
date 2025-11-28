# Genome assembies of <i>Erysimum incanum</i> (Ei) and <i>Erysimum wilczekianum</i> (Ewi)

We present the first drafts of genome sequences of <i>Erysimum incanum</i> and <i>Erysimum wilczekianum</i> combining long and short read sequencing techiniques. We employed RNAseq as well to do the gneome annotation of both genomes.

For <i>Erysimum incanum</i>, we used ONT MinION sequences and Illumina HiSeq short reads. We obtained a first assembly with Wtdbg2 and polished with Pilon. Scaffolding step was done using RagTag and the genome of <i>Erysimum cheiranthoides</i> available on [erysimum.org](erysimum.org) as template.

For <i>Erysimum wilczekianum</i>, we used PacBio HiFi sequences and Illumina HiSeq short reads.  We obtained a first assembly with hifiasm and polished with Pilon. Scaffolding step was done using RagTag and the genome of <i>Erysimum cheiranthoides</i> as template too.


Both genomes were analysed using [this script](https://github.com/ISUgenomics/common_scripts/blob/master/new_Assemblathon.pl) from Genome Informatics Facility. Quality was assessed via BUSCO sequences. We tracked repeated sequences too using RepeatModeler and RepeatMasker. 


For genome annotation we used RNA sequences obtained with Illumina HiSeq 200 paired-end technique and we employed BRAKER2 for gene prediction. Predicted aminoacid sequences were annoted using [SMA3S script](https://github.com/UPOBioinfo/sma3s). 


## <b>Genome assembly analysis of <i>Erysimum incanum</i>.
| Ensamblador / Dataset | # contigs | Total length  | N50 length | % >10 Kb |
| --------------------- | --------- | ------------- | ---------- | -------- |
| ONT MinION            | 185,934   | 1,586,430,815 | 15,789     | 32.7%    |
| Wtdbg2                | 472       | 117,347,710   | 663,698    | 90.3%    |
| Wtdbg2-Pilon          | 472       | 120,030,576   | 679,018    | 90.5%    |
| RagTag (scaffolds)    | 101       | 120,067,676   | 13,971,638 | 73.3%    |


A.</b> Read length distribution from ONT MinION sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. incanum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.

![<b>Genome assembly analysis of <i>Erysimum incanum</i>. A.</b> Read length distribution from ONT MinION sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. incanum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/Figure_Ei_Genome.png)


Proportion of genomic components in <i>Erysimum incanum</i>.

<img src="https://github.com/carlosolmedo13/erysimum-genomes/blob/main/type_seqs_Ei.png" width="400">


## <b>Genome assembly analysis of <i>Erysimum wilczekianum</i>

| Ensamblador / Dataset | # contigs | Total length   | N50 length | % >10 Kb |
| --------------------- | --------- | -------------- | ---------- | -------- |
| PacBio HiFi           | 1,733,559 | 10,272,354,145 | 6,555      | —        |
| hifiasm               | 1,333     | 317,313,907    | 3,731,806  | 94.2%    |
| hifiasm-Pilon         | 1,333     | 317,141,130    | 3,728,219  | 94.2%    |
| RagTag (scaffolds)    | 1,179     | 317,156,530    | 24,435,675 | 93.6%    |


A.</b> Read length distribution from PacBio Hifi sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. wilczekianum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.
![<b>Genome assembly analysis of <i>Erysimum wilczekianum</i>. A.</b> Read length distribution from PacBio Hifi sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. wilczekianum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/Figure_Ei_Genome.png)


Proportion of genomic components in <i>Erysimum wilczekianum</i>.

<img src="https://github.com/carlosolmedo13/erysimum-genomes/blob/main/type_seqs_Ewi.png" width="400">


## Synteny analysis between <i>Erysimum incanum</i> and </i>Erysimum wilczekianum<i>.
Global synteny analisis using nucmer for draft assemblies of Ei and Eche (A), Ewi and Eche (B), Ei and Ewi (C) and Ei draft assembly and Ewi contig assembly before scaffolding with Eche (D). Circle representation was done in R 4.3.3 using circlize package.

![](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/figure_global_synteny.png)









