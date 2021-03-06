# Analysis-pipeline-for-piRNA
The bash-based pipeline for analyzing PIWI-interacting RNA

## Environment
For managing the environment conveniently, we install [Conda](https://docs.conda.io/en/latest/), and installed the following programs by it.
* Samtools
* Bedtools
* Weblogo
* MirDeep2
* STAR
* Bowtie

## First step, extracting piRNAs

In order to filiter out rRNA, tRNA, and microRNA we use Bowtie.
For mapping to human genome, we use STAR and create the bed file with multiple alignments for each read.

[Main Extraction Code](https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/code/main.sh)

## Selecting unique sequence from multiple alignments for each sequencing read

[Selecting Code](https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/code/unify.sh)

## Using weblogo to plot

The diagram created by weblogo can show 1U10A feature of piwi-interacting RNA.

[Data processing and plotting](https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/code/runPiRWeblogo.sh)

[<img src="https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/weblogo.png" width="600"/>](https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/weblogo.png)

The example of piRNA reads shown in Weblogo.

[<img src="https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/distribution.png" width="600"/>](https://github.com/SodiumJu/Analysis-pipeline-for-piRNA/blob/master/distribution.png)

The distribution of overlapping base counts of selecting small RNA. If the process of producing piRNA involved with ping-pong cycle, the pool of piRNA shows 10 base pairs feature.
