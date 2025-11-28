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
![<b>Genome assembly analysis of <i>Erysimum wilczekianum</i>. A.</b> Read length distribution from PacBio Hifi sequencing. <b>B.</b> K-mer coverage distribution from Illumina HiSeq short reads. <b>C.</b> Dotplot alignment between final draft assembly and chromosomes from <i>Erysimum cheiranthoides</i> (ECHEv2.0). Chromosomes in <i>E. wilczekianum</i> are ordered according to their sized but named after ECHEv2.0 homolog chromosome. <b>D.</b> BUSCO analysis based on Brassicales results from draft genome assembly.](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/Figure_Ewi_Genome.png)


Proportion of genomic components in <i>Erysimum wilczekianum</i>.

<img src="https://github.com/carlosolmedo13/erysimum-genomes/blob/main/type_seqs_Ewi.png" width="400">


## Synteny analysis between <i>Erysimum incanum</i> and <i>Erysimum wilczekianum</i>.

Global synteny analisis using nucmer for draft assemblies of Ei and Eche (A), Ewi and Eche (B), Ei and Ewi (C) and Ei draft assembly and Ewi contig assembly before scaffolding with Eche (D). Circle representation was done in R 4.3.3 using circlize package.

![](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/figure_global_synteny.png)



## Gene ontology of <i>Erysimum incanum</i>.

From a initial set of 29991 aminoacid sequences, we obtained an annotation
for 26261 sequences.

![](https://github.com/carlosolmedo13/erysimum-genomes/blob/main/go_ei.png)

Cellular component:

| Num | Description                           | Count |
| --- | ------------------------------------- | ----- |
| 1   | nucleus                               | 5239  |
| 2   | plastid                               | 3773  |
| 3   | cytosol                               | 3252  |
| 4   | plasma membrane                       | 3099  |
| 5   | cytoplasm                             | 2672  |
| 6   | protein complex                       | 2485  |
| 7   | vacuole                               | 2281  |
| 8   | intracellular                         | 1968  |
| 9   | extracellular region                  | 1869  |
| 10  | Golgi apparatus                       | 1860  |
| 11  | mitochondrion                         | 1845  |
| 12  | endoplasmic reticulum                 | 1503  |
| 13  | cell wall                             | 1418  |
| 14  | organelle                             | 1054  |
| 15  | nucleoplasm                           | 1003  |
| 16  | endosome                              | 992   |
| 17  | nucleolus                             | 907   |
| 18  | thylakoid                             | 882   |
| 19  | cytoskeleton                          | 755   |
| 20  | cell                                  | 740   |
| 21  | ribosome                              | 687   |
| 22  | cytoplasmic, membrane-bounded vesicle | 571   |
| 23  | peroxisome                            | 515   |
| 24  | chromosome                            | 511   |
| 25  | nuclear chromosome                    | 438   |
| 26  | nuclear envelope                      | 309   |
| 27  | microtubule organizing center         | 299   |
| 28  | extracellular space                   | 260   |
| 29  | lipid particle                        | 251   |
| 30  | lysosome                              | 194   |
| 31  | cilium                                | 115   |
| 32  | proteinaceous extracellular matrix    | 56    |
| 33  | cytoplasmic chromosome                | 37    |
| 34  | external encapsulating structure      | 8     |

Biological processes:
| Num | Description                                              | Count |
| --- | -------------------------------------------------------- | ----- |
| 1   | anatomical structure development                         | 3903  |
| 2   | biosynthetic process                                     | 3866  |
| 3   | response to stress                                       | 3335  |
| 4   | cellular nitrogen compound metabolic process             | 3307  |
| 5   | reproduction                                             | 2996  |
| 6   | cellular protein modification process                    | 2050  |
| 7   | catabolic process                                        | 2039  |
| 8   | transport                                                | 1846  |
| 9   | signal transduction                                      | 1788  |
| 10  | small molecule metabolic process                         | 1594  |
| 11  | cell differentiation                                     | 1415  |
| 12  | growth                                                   | 1390  |
| 13  | carbohydrate metabolic process                           | 1388  |
| 14  | lipid metabolic process                                  | 1380  |
| 15  | embryo development                                       | 1117  |
| 16  | cell wall organization or biogenesis                     | 1087  |
| 17  | homeostatic process                                      | 1028  |
| 18  | DNA metabolic process                                    | 1027  |
| 19  | chromosome organization                                  | 984   |
| 20  | translation                                              | 950   |
| 21  | developmental maturation                                 | 917   |
| 22  | cell cycle                                               | 913   |
| 23  | immune system process                                    | 893   |
| 24  | transmembrane transport                                  | 881   |
| 25  | vesicle-mediated transport                               | 881   |
| 26  | cell morphogenesis                                       | 734   |
| 27  | cell death                                               | 706   |
| 28  | anatomical structure formation involved in morphogenesis | 704   |
| 29  | secondary metabolic process                              | 696   |
| 30  | protein complex assembly                                 | 695   |
| 31  | mRNA processing                                          | 645   |
| 32  | cell division                                            | 639   |
| 33  | protein targeting                                        | 559   |
| 34  | sulfur compound metabolic process                        | 557   |
| 35  | cellular component assembly                              | 557   |
| 36  | cytoskeleton organization                                | 554   |
| 37  | ribosome biogenesis                                      | 549   |
| 38  | aging                                                    | 546   |
| 39  | cofactor metabolic process                               | 514   |
| 40  | cellular amino acid metabolic process                    | 494   |
| 41  | membrane organization                                    | 489   |
| 42  | cell proliferation                                       | 469   |
| 43  | photosynthesis                                           | 450   |
| 44  | generation of precursor metabolites and energy           | 444   |
| 45  | mitochondrion organization                               | 444   |
| 46  | protein folding                                          | 429   |
| 47  | mitotic nuclear division                                 | 427   |
| 48  | ribonucleoprotein complex assembly                       | 381   |
| 49  | chromosome segregation                                   | 353   |
| 50  | nucleocytoplasmic transport                              | 341   |
| 51  | vacuolar transport                                       | 322   |
| 52  | cell-cell signaling                                      | 313   |
| 53  | tRNA metabolic process                                   | 300   |
| 54  | symbiosis (mutualism–parasitism)                         | 263   |
| 55  | autophagy                                                | 253   |
| 56  | extracellular matrix organization                        | 248   |
| 57  | nucleobase-containing compound catabolic process         | 240   |
| 58  | protein maturation                                       | 209   |
| 59  | pigmentation                                             | 163   |
| 60  | cell motility                                            | 125   |
| 61  | macromolecular complex assembly                          | 123   |
| 62  | cell adhesion                                            | 121   |
| 63  | plasma membrane organization                             | 109   |
| 64  | locomotion                                               | 108   |
| 65  | nitrogen cycle metabolic process                         | 96    |
| 66  | neurological system process                              | 86    |
| 67  | cell junction organization                               | 79    |
| 68  | cytoskeleton-dependent intracellular transport           | 66    |
| 69  | transposition                                            | 53    |
| 70  | circulatory system process                               | 45    |


Molecular functions:
| Num | Description                                        | Count |
| --- | -------------------------------------------------- | ----- |
| 1   | ion binding                                        | 4703  |
| 2   | DNA binding                                        | 2611  |
| 3   | kinase activity                                    | 2309  |
| 4   | oxidoreductase activity                            | 1858  |
| 5   | transmembrane transporter activity                 | 1359  |
| 6   | nucleic acid binding transcription factor activity | 1239  |
| 7   | RNA binding                                        | 1230  |
| 8   | peptidase activity                                 | 1030  |
| 9   | transferase activity (glycosyl groups)             | 990   |
| 10  | ligase activity                                    | 987   |
| 11  | ATPase activity                                    | 952   |
| 12  | hydrolase activity (glycosyl bonds)                | 686   |
| 13  | enzyme binding                                     | 677   |
| 14  | enzyme regulator activity                          | 655   |
| 15  | transferase activity (acyl groups)                 | 642   |
| 16  | phosphatase activity                               | 640   |
| 17  | methyltransferase activity                         | 635   |
| 18  | lyase activity                                     | 633   |
| 19  | structural constituent of ribosome                 | 607   |
| 20  | isomerase activity                                 | 492   |
| 21  | nuclease activity                                  | 480   |
| 22  | nucleotidyltransferase activity                    | 479   |
| 23  | lipid binding                                      | 459   |
| 24  | signal transducer activity                         | 439   |
| 25  | translation factor activity (RNA binding)          | 419   |
| 26  | helicase activity                                  | 415   |
| 27  | cytoskeletal protein binding                       | 384   |
| 28  | GTPase activity                                    | 327   |
| 29  | transcription factor activity (protein binding)    | 283   |
| 30  | transcription factor binding                       | 238   |
| 31  | structural molecule activity                       | 224   |
| 32  | transferase activity (alkyl/aryl groups)           | 216   |
| 33  | mRNA binding                                       | 195   |
| 34  | rRNA binding                                       | 187   |
| 35  | hydrolase activity (C–N bonds, non-peptide)        | 159   |
| 36  | protein transporter activity                       | 141   |
| 37  | histone binding                                    | 139   |
| 38  | ubiquitin-like protein binding                     | 110   |
| 39  | unfolded protein binding                           | 98    |
| 40  | protein binding, bridging                          | 44    |





