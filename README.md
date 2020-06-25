#UCSC Tracks for DMD exon labelling

## Supports:
  * hg38
  * hg19
  * hg18
  * mm10
  * mm9

## Data that is included here

  * DMD exon positions
  * DMD intron positions
  * known variants with allele frequency
  * case study DMD mutations (in progress)


## Building a track hub

Basic instructions are to:
 
Create BED file (chrom, start, stop, name). Make sure it is sorted by chrom, start.

Convert BED to BigBED. You will need the bedToBigBed utility and fetchChromSizes from
the UCSC genome browser tools.

Command:

 bedToBigBed mytrack.bed hg19.chrom.sizes mytrack.bigbed

Create the hub.txt, genome.txt, trackDb.txt files as described here:
https://genome.ucsc.edu/goldenPath/help/hubQuickStart.html

Upload all files to the hosting webserver. Must be publically accessible.

In the UCSC genome browser, connect a track hub using the 'track hub' input.
