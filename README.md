# Genome assembies of <i>Erysimum incanum</i> and <i>Erysimum wilczekianum</i>

We present the first drafts of genome sequences of <i>Erysimum incanum</i> and <i>Erysimum wilczekianum</i> combining long and short read sequencing techiniques. We employed RNAseq as well to do the gneome annotation of both genomes.

For <i>Erysimum incanum</i>, we used ONT MinION sequences and Illumina HiSeq short reads. We obtained a first assembly with Wtdbg2 and polished with Pilon. Scaffolding step was done using RagTag and the genome of <i>Erysimum cheiranthoides</i> available on [erysimum.org](erysimum.org) as template.

For <i>Erysimum wilczekianum</i>, we used PacBio HiFi sequences and Illumina HiSeq short reads.  We obtained a first assembly with hifiasm and polished with Pilon. Scaffolding step was done using RagTag and the genome of <i>Erysimum cheiranthoides</i> as template too.


Both genomes were analysed using [this script](https://github.com/ISUgenomics/common_scripts/blob/master/new_Assemblathon.pl) from Genome Informatics Facility. Quality was assessed via BUSCO sequences. We tracked repeated sequences too using RepeatModeler and RepeatMasker. 


For genome annotation we used RNA sequences obtained with Illumina HiSeq 200 paired-end technique and we employed BRAKER2 for gene prediction. Predicted aminoacid sequences were annoted using [SMA3S script](https://github.com/UPOBioinfo/sma3s). 


<b>Genome assembly analysis of <i>Erysimum incanum</i>. A.</b> Read length distribution from ONT MinION sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. incanum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.

![<b>Genome assembly analysis of <i>Erysimum incanum</i>. A.</b> Read length distribution from ONT MinION sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. incanum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/Figure_Ei_Genome.png)

<b>Genome assembly analysis of <i>Erysimum wilczekianum</i>. A.</b> Read length distribution from PacBio Hifi sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. wilczekianum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.
![<b>Genome assembly analysis of <i>Erysimum wilczekianum</i>. A.</b> Read length distribution from PacBio Hifi sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. wilczekianum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/Figure_Ei_Genome.png)


