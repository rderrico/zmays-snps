# *Zea mays* SNP calling

We sequenced three lines of *Zea mays*, using pair-end sequencing. This sequencing was done by our sequencing core and we received the data on 10-05-2013. Each variety should have **two** sequence files, with suffixes `_R1.fastq` and `_R2.fastq`, indicating which member of the pair it is.

## Sequencing Files

All raw FASTQ sequences are ind `data/seqs/`:

	$ find data/seqs -name "*.fastq"
	data/seqs/zmaysA_R1.fastq
	data/seqs/zmaysA_R2.fastq
	data/seqs/zmaysB_R1.fastq
	data/seqs/zmaysC_R1.fastq
	data/seqs/zmaysB_R2.fastq
	data/seqs/zmaysC_R2.fastq
	
## Quality Control Steps

After the sequencing data was received, our first stage of analysis was to ensure the sequeces were high quality. We ran each of the three lines' two paired-end FASTQ files through a quality diagnostic and control pipeline. Our planned pipeline is:

1. Create base quality diagnostic graphs.
2. Check reads for adapter sequences.
3. Trim adapter sequences.
4. Trim poor quality bases.

Recommended trimming programs:

- Trimmomatic
- Scythe
Project started 03-01-2013
TODO: ask sequencing center about adapters
Samples expected from sequencing core on 10-01-2013
