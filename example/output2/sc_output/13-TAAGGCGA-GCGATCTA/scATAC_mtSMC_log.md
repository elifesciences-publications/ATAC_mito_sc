----------------------------------------
##### [Pipeline run code and environment:]
*              Command:  `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/src/scATACseq_mtSMC_3.py -P 8 -M 100 -O /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2 -R -S 13-TAAGGCGA-GCGATCTA -s 0 -G hg19 -Q paired -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz -I2 /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz`
*         Compute host:  changrila2.stanford.edu
*          Working dir:  /storage/jinxu/pipeline_pypiper/ATAC_mito_sc/example
*            Outfolder:  /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/
*  Pipeline started at:   (07-30 15:20:51) elapsed:0:00:04 _TIME_

##### [Version log:]
*       Python version:  2.7.5
*          Pypiper dir:  `/storage/jinxu/.local/lib/python2.7/site-packages/pypiper`
*      Pypiper version:  0.6.0
*         Pipeline dir:  `/storage/jinxu/pipeline_pypiper/ATAC_mito_sc/src`
*     Pipeline version:  None
*        Pipeline hash:  cdc25f0f896bbb8ed73151376941bfda0a610dc3
*      Pipeline branch:  * develop
*        Pipeline date:  2017-08-17 11:24:05 -0700
*        Pipeline diff:  81 files changed, 153475 insertions(+), 1665262 deletions(-)

##### [Arguments passed to pipeline:]
*             `input2`:  `['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz']`
*         `paired_end`:  `True`
*       `manual_clean`:  `False`
*              `input`:  `['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz']`
*                `mem`:  `100`
*        `sample_name`:  `13-TAAGGCGA-GCGATCTA`
*        `config_file`:  `scATACseq_mtSMC_3.yaml`
*      `output_parent`:  `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2`
*   `single_or_paired`:  `paired`
*    `genome_assembly`:  `hg19`
*              `stopN`:  `0`
*              `cores`:  `8`
*              `fresh`:  `False`
*            `recover`:  `True`
*       `force_follow`:  `False`

----------------------------------------


Change status from initializing to running
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz
Command is not callable: pigz

### Merge/link and fastq conversion:  (07-30 15:20:51) elapsed:0:00:00 _TIME_

Number of input file sets:		2

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz`
> `ln -sf /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz`

<pre>
</pre>
Process 23523 returned: (0). Elapsed: 0:00:00.
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz`
> `ln -sf /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz`

<pre>
</pre>
Process 23535 returned: (0). Elapsed: 0:00:00.
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz
['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz', '/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz']

Target exists: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/`
> `File_MB`	7.8075	scATAC_mtSMC	_RES_
> `GenomeV`	hg19	scATAC_mtSMC	_RES_

### Adapter trimming: in-house script (07-30 15:20:51) elapsed:0:00:01 _TIME_

Traceback (most recent call last):
  File "/home/jinxu/pipeline_pypiper/ATAC_mito_sc/src/scATACseq_mtSMC_3.py", line 102, in <module>
    trimmed_fastq= str.replace("fastq.gz","trim.fastq")
TypeError: replace() takes at least 2 arguments (1 given)

Pypiper terminating spawned child process 23304...
child process terminated
Pipeline status is: running

### Pipeline failed at:  (07-30 15:20:52) elapsed:0:00:01 _TIME_

Total time: 0:00:05

Change status from running to failed
Error in atexit._run_exitfuncs:
Traceback (most recent call last):
  File "/usr/lib64/python2.7/atexit.py", line 24, in _run_exitfuncs
    func(*targs, **kargs)
  File "/home/jinxu/.local/lib/python2.7/site-packages/pypiper/pypiper.py", line 1172, in _exit_handler
    self.fail_pipeline(Exception("Unknown exit failure"))
  File "/home/jinxu/.local/lib/python2.7/site-packages/pypiper/pypiper.py", line 1111, in fail_pipeline
    raise e
Exception: Unknown exit failure
Error in sys.exitfunc:
Traceback (most recent call last):
  File "/usr/lib64/python2.7/atexit.py", line 24, in _run_exitfuncs
    func(*targs, **kargs)
  File "/home/jinxu/.local/lib/python2.7/site-packages/pypiper/pypiper.py", line 1172, in _exit_handler
    self.fail_pipeline(Exception("Unknown exit failure"))
  File "/home/jinxu/.local/lib/python2.7/site-packages/pypiper/pypiper.py", line 1111, in fail_pipeline
    raise e
Exception: Unknown exit failure
----------------------------------------
##### [Pipeline run code and environment:]
*              Command:  `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/src/scATACseq_mtSMC_3.py -P 8 -M 100 -O /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2 -R -S 13-TAAGGCGA-GCGATCTA -s 0 -G hg19 -Q paired -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz -I2 /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz`
*         Compute host:  changrila2.stanford.edu
*          Working dir:  /storage/jinxu/pipeline_pypiper/ATAC_mito_sc/example
*            Outfolder:  /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/
*  Pipeline started at:   (07-30 15:23:29) elapsed:0:00:03 _TIME_

##### [Version log:]
*       Python version:  2.7.5
*          Pypiper dir:  `/storage/jinxu/.local/lib/python2.7/site-packages/pypiper`
*      Pypiper version:  0.6.0
*         Pipeline dir:  `/storage/jinxu/pipeline_pypiper/ATAC_mito_sc/src`
*     Pipeline version:  None
*        Pipeline hash:  cdc25f0f896bbb8ed73151376941bfda0a610dc3
*      Pipeline branch:  * develop
*        Pipeline date:  2017-08-17 11:24:05 -0700
*        Pipeline diff:  81 files changed, 153475 insertions(+), 1665262 deletions(-)

##### [Arguments passed to pipeline:]
*             `input2`:  `['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz']`
*         `paired_end`:  `True`
*       `manual_clean`:  `False`
*              `input`:  `['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz']`
*                `mem`:  `100`
*        `sample_name`:  `13-TAAGGCGA-GCGATCTA`
*        `config_file`:  `scATACseq_mtSMC_3.yaml`
*      `output_parent`:  `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2`
*   `single_or_paired`:  `paired`
*    `genome_assembly`:  `hg19`
*              `stopN`:  `0`
*              `cores`:  `8`
*              `fresh`:  `False`
*            `recover`:  `True`
*       `force_follow`:  `False`

----------------------------------------


Change status from initializing to running
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R1.fastq.gz
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/test_data/13-TAAGGCGA-GCGATCTA_S1_001_R2.fastq.gz
Command is not callable: pigz

### Merge/link and fastq conversion:  (07-30 15:23:29) elapsed:0:00:00 _TIME_

Number of input file sets:		2

Target exists: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz`
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz

Target exists: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz`
Local input file: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz
['/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz', '/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz']

Target exists: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/`
> `File_MB`	7.8075	scATAC_mtSMC	_RES_
> `GenomeV`	hg19	scATAC_mtSMC	_RES_

### Adapter trimming: in-house script (07-30 15:23:29) elapsed:0:00:00 _TIME_


Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq`
> `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/src/adapterTrimming /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz`

<pre>


Running adapter trimming
	FASTQ file for read1 = /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.fastq.gz
	FASTQ file for read2 = /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.fastq.gz
	Query length = 25

Opened FASTQ files

Printing output to:
	/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq
	/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.trim.fastq

COMPLETE

TOTAL number of reads = 56480
Total number of trimmed reads = 454
	Reads with 0 mismatches = 392
	Reads with 1 mismatches = 62
</pre>
Process 29490 returned: (0). Elapsed: 0:00:16. Peak memory: (Process: 0.001GB; Pipeline: 0.0GB)
> `Raw_reads`	112960	scATAC_mtSMC	_RES_
> `Trimmed_reads`	112960.0	scATAC_mtSMC	_RES_
> `Trim_loss_rate`	0.0	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R1.sai`
> `/home/jinxu/software/bwa-0.7.15/bwa aln  -t  8 /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R1.sai`

<pre>
[bwa_aln] 17bp reads: max_diff = 2
[bwa_aln] 38bp reads: max_diff = 3
[bwa_aln] 64bp reads: max_diff = 4
[bwa_aln] 93bp reads: max_diff = 5
[bwa_aln] 124bp reads: max_diff = 6
[bwa_aln] 157bp reads: max_diff = 7
[bwa_aln] 190bp reads: max_diff = 8
[bwa_aln] 225bp reads: max_diff = 9
[bwa_aln_core] calculate SA coordinate... 28.92 sec
[bwa_aln_core] write to the disk... 0.02 sec
[bwa_aln_core] 56480 sequences have been processed.
[main] Version: 0.7.15-r1140
[main] CMD: /home/jinxu/software/bwa-0.7.15/bwa aln -t 8 -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R1.sai /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq
[main] Real time: 9.980 sec; CPU: 34.514 sec
</pre>
Process 30191 returned: (0). Elapsed: 0:00:16. Peak memory: (Process: 3.073GB; Pipeline: 0.001GB)

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R2.sai`
> `/home/jinxu/software/bwa-0.7.15/bwa aln  -t 8 /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.trim.fastq -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R2.sai`

<pre>
[bwa_aln] 17bp reads: max_diff = 2
[bwa_aln] 38bp reads: max_diff = 3
[bwa_aln] 64bp reads: max_diff = 4
[bwa_aln] 93bp reads: max_diff = 5
[bwa_aln] 124bp reads: max_diff = 6
[bwa_aln] 157bp reads: max_diff = 7
[bwa_aln] 190bp reads: max_diff = 8
[bwa_aln] 225bp reads: max_diff = 9
[bwa_aln_core] calculate SA coordinate... 27.66 sec
[bwa_aln_core] write to the disk... 0.01 sec
[bwa_aln_core] 56480 sequences have been processed.
[main] Version: 0.7.15-r1140
[main] CMD: /home/jinxu/software/bwa-0.7.15/bwa aln -t 8 -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R2.sai /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.trim.fastq
[main] Real time: 9.075 sec; CPU: 32.945 sec
</pre>
Process 30311 returned: (0). Elapsed: 0:00:16. Peak memory: (Process: 3.102GB; Pipeline: 3.073GB)

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.sam`
> `/home/jinxu/software/bwa-0.7.15/bwa sampe -r "@RG\tID:13-TAAGGCGA-GCGATCTA\tSM:MT\tPL:ILLUMINA" /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R1.sai /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R2.sai /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.trim.fastq -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.sam`

<pre>
[bwa_sai2sam_pe_core] convert to sequence coordinate... 
[infer_isize] (25, 50, 75) percentile: (182, 246, 387)
[infer_isize] low and high boundaries: 75 and 797 for estimating avg and std
[infer_isize] inferred external isize from 37261 pairs: 293.098 +/- 150.921
[infer_isize] skewness: 0.995; kurtosis: 0.420; ap_prior: 1.26e-05
[infer_isize] inferred maximum insert size: 1324 (6.83 sigma)
[bwa_sai2sam_pe_core] time elapses: 11.78 sec
[bwa_sai2sam_pe_core] changing coordinates of 1414 alignments.
[bwa_sai2sam_pe_core] align unmapped mate...
[bwa_paired_sw] 6672 out of 11443 Q17 singletons are mated.
[bwa_paired_sw] 49 out of 131 Q17 discordant pairs are fixed.
[bwa_sai2sam_pe_core] time elapses: 1.53 sec
[bwa_sai2sam_pe_core] refine gapped alignments... 0.15 sec
[bwa_sai2sam_pe_core] print alignments... 0.56 sec
[bwa_sai2sam_pe_core] 56480 sequences have been processed.
[main] Version: 0.7.15-r1140
[main] CMD: /home/jinxu/software/bwa-0.7.15/bwa sampe -r @RG\tID:13-TAAGGCGA-GCGATCTA\tSM:MT\tPL:ILLUMINA -f /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.sam /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R1.sai /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA_R2.sai /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R1.trim.fastq /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/raw/13-TAAGGCGA-GCGATCTA_R2.trim.fastq
[main] Real time: 14.265 sec; CPU: 14.256 sec
</pre>
Process 30567 returned: (0). Elapsed: 0:00:16. Peak memory: (Process: 3.783GB; Pipeline: 3.102GB)

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.bam`
> `java -Xmx4g -jar /home/jinxu/software/picard-tools-2.4.1/picard.jar SortSam SORT_ORDER=coordinate CREATE_INDEX=true VALIDATION_STRINGENCY=SILENT INPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.sam OUTPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.bam`

<pre>
[Mon Jul 30 15:24:33 PDT 2018] picard.sam.SortSam INPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.sam OUTPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.bam SORT_ORDER=coordinate VALIDATION_STRINGENCY=SILENT CREATE_INDEX=true    VERBOSITY=INFO QUIET=false COMPRESSION_LEVEL=5 MAX_RECORDS_IN_RAM=500000 CREATE_MD5_FILE=false GA4GH_CLIENT_SECRETS=client_secrets.json
[Mon Jul 30 15:24:33 PDT 2018] Executing as jinxu@changrila2.stanford.edu on Linux 3.10.0-693.el7.x86_64 amd64; OpenJDK 64-Bit Server VM 1.8.0_161-b14; Picard version: 2.4.1(7c4d36e011df1aec4689b51efcada44e92d1817f_1464389670) JdkDeflater
INFO	2018-07-30 15:24:34	SortSam	Finished reading inputs, merging and writing to output now.
[Mon Jul 30 15:24:36 PDT 2018] picard.sam.SortSam done. Elapsed time: 0.06 minutes.
Runtime.totalMemory()=2058354688
</pre>
Process 30847 returned: (0). Elapsed: 0:00:06. Peak memory: (Process: 0.041GB; Pipeline: 3.783GB)
> `Aligned_reads`	106047	scATAC_mtSMC	_RES_
> `Alignment_rate`	0.94	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam`
> `java -Xmx4g -jar /home/jinxu/software/picard-tools-2.4.1/picard.jar MarkDuplicates CREATE_INDEX=true ASSUME_SORTED=true VALIDATION_STRINGENCY=SILENT REMOVE_DUPLICATES=true INPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.bam OUTPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam METRICS_FILE=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.metrics`

<pre>
[Mon Jul 30 15:24:38 PDT 2018] picard.sam.markduplicates.MarkDuplicates INPUT=[/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.bam] OUTPUT=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam METRICS_FILE=/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.metrics REMOVE_DUPLICATES=true ASSUME_SORTED=true VALIDATION_STRINGENCY=SILENT CREATE_INDEX=true    MAX_SEQUENCES_FOR_DISK_READ_ENDS_MAP=50000 MAX_FILE_HANDLES_FOR_READ_ENDS_MAP=8000 SORTING_COLLECTION_SIZE_RATIO=0.25 REMOVE_SEQUENCING_DUPLICATES=false TAGGING_POLICY=DontTag DUPLICATE_SCORING_STRATEGY=SUM_OF_BASE_QUALITIES PROGRAM_RECORD_ID=MarkDuplicates PROGRAM_GROUP_NAME=MarkDuplicates READ_NAME_REGEX=<optimized capture of last three ':' separated fields as numeric values> OPTICAL_DUPLICATE_PIXEL_DISTANCE=100 VERBOSITY=INFO QUIET=false COMPRESSION_LEVEL=5 MAX_RECORDS_IN_RAM=500000 CREATE_MD5_FILE=false GA4GH_CLIENT_SECRETS=client_secrets.json
[Mon Jul 30 15:24:38 PDT 2018] Executing as jinxu@changrila2.stanford.edu on Linux 3.10.0-693.el7.x86_64 amd64; OpenJDK 64-Bit Server VM 1.8.0_161-b14; Picard version: 2.4.1(7c4d36e011df1aec4689b51efcada44e92d1817f_1464389670) JdkDeflater
INFO	2018-07-30 15:24:38	MarkDuplicates	Start of doWork freeMemory: 2045987336; totalMemory: 2058354688; maxMemory: 3817865216
INFO	2018-07-30 15:24:38	MarkDuplicates	Reading input file and constructing read end information.
INFO	2018-07-30 15:24:38	MarkDuplicates	Will retain up to 14684096 data points before spilling to disk.
INFO	2018-07-30 15:24:40	MarkDuplicates	Read 111866 records. 6 pairs never matched.
INFO	2018-07-30 15:24:41	MarkDuplicates	After buildSortedReadEndLists freeMemory: 1917851584; totalMemory: 2058354688; maxMemory: 3817865216
INFO	2018-07-30 15:24:41	MarkDuplicates	Will retain up to 119308288 duplicate indices before spilling to disk.
INFO	2018-07-30 15:24:42	MarkDuplicates	Traversing read pair information and detecting duplicates.
INFO	2018-07-30 15:24:42	MarkDuplicates	Traversing fragment information and detecting duplicates.
INFO	2018-07-30 15:24:42	MarkDuplicates	Sorting list of duplicate records.
INFO	2018-07-30 15:24:42	MarkDuplicates	After generateDuplicateIndexes freeMemory: 1092245072; totalMemory: 2058354688; maxMemory: 3817865216
INFO	2018-07-30 15:24:42	MarkDuplicates	Marking 32039 records as duplicates.
INFO	2018-07-30 15:24:42	MarkDuplicates	Found 0 optical duplicate clusters.
INFO	2018-07-30 15:24:42	MarkDuplicates	Reads are assumed to be ordered by: coordinate
INFO	2018-07-30 15:24:45	MarkDuplicates	Before output close freeMemory: 2045837808; totalMemory: 2058354688; maxMemory: 3817865216
INFO	2018-07-30 15:24:45	MarkDuplicates	After output close freeMemory: 2045905112; totalMemory: 2058354688; maxMemory: 3817865216
[Mon Jul 30 15:24:45 PDT 2018] picard.sam.markduplicates.MarkDuplicates done. Elapsed time: 0.11 minutes.
Runtime.totalMemory()=2058354688
</pre>
Process 30923 returned: (0). Elapsed: 0:00:16. Peak memory: (Process: 1.688GB; Pipeline: 3.783GB)
> `rmdup_reads`	74008	scATAC_mtSMC	_RES_
> `dup_rate`	0.3	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.genomeQ30PE.bam`
> `/usr/local/bin/samtools view -b -q  30   -f 0x2 /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam  -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.genomeQ30PE.bam chr1 chr2 chr3 chr4 chr5 chr6 chr7 chr8 chr9 chr10 chr11 chr12 chr13 chr14 chr15 chr16 chr17 chr18 chr19 chr20 chr21 chr22 chrX`

<pre>
</pre>
Process 31314 returned: (0). Elapsed: 0:00:06. Peak memory: (Process: 0.004GB; Pipeline: 3.783GB)
> `genomeQ30PE_reads`	50622	scATAC_mtSMC	_RES_
> `genomeQ30PE_rate`	0.48	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.RefTSSCount`
> `/seq/bedtools-master/bin/bedtools coverage  -abam /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.genomeQ30PE.bam -b /home/jinxu/DB/hg19/annotation/hg19_refGene_TSSRound2kb.bed -counts  > /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.RefTSSCount`

<pre>
</pre>
Process 31427 returned: (0). Elapsed: 0:00:06.
> ` awk 'BEGIN{sum=0}''{sum+=$6;}''END{print sum}' /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.RefTSSCount`

> `Total_TSS_reads`	23798	scATAC_mtSMC	_RES_
> `TSS_rate`	0.24	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mtQ30PE.bam`
> `/usr/local/bin/samtools view -b -q  30   -f 0x2 /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam  -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mtQ30PE.bam  chrMT `

<pre>
</pre>
Process 31524 returned: (0). Elapsed: 0:00:00. Peak memory: (Process: 0.0GB; Pipeline: 3.783GB)
> `mtQ30PE_reads`	6438	scATAC_mtSMC	_RES_
> `mtQ30PE_rate`	0.06	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.target.intervals`
> `java -Xmx8g -jar /home/jinxu/software/GenomeAnalysisTK.jar  -R /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta  -T RealignerTargetCreator  -known /home/jinxu/DB/hg19_g1k_v37/ALL.chrMT.phase3_callmom-v0_4.20130502.genotypes.Indel.vcf  -known /home/jinxu/DB/hg19_g1k_v37/Mills_and_1000G_gold_standard.indels.hg19.sites.vcf  -nt 8  -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam  -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.target.intervals`

<pre>
INFO  15:25:07,737 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:25:07,740 HelpFormatter - The Genome Analysis Toolkit (GATK) v3.5-0-g36282e4, Compiled 2015/11/25 04:03:56 
INFO  15:25:07,740 HelpFormatter - Copyright (c) 2010 The Broad Institute 
INFO  15:25:07,740 HelpFormatter - For support and documentation go to http://www.broadinstitute.org/gatk 
INFO  15:25:07,745 HelpFormatter - Program Args: -R /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta -T RealignerTargetCreator -known /home/jinxu/DB/hg19_g1k_v37/ALL.chrMT.phase3_callmom-v0_4.20130502.genotypes.Indel.vcf -known /home/jinxu/DB/hg19_g1k_v37/Mills_and_1000G_gold_standard.indels.hg19.sites.vcf -nt 8 -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.target.intervals 
INFO  15:25:07,751 HelpFormatter - Executing as jinxu@changrila2.stanford.edu on Linux 3.10.0-693.el7.x86_64 amd64; OpenJDK 64-Bit Server VM 1.8.0_161-b14. 
INFO  15:25:07,752 HelpFormatter - Date/Time: 2018/07/30 15:25:07 
INFO  15:25:07,752 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:25:07,753 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:25:07,866 GenomeAnalysisEngine - Strictness is SILENT 
INFO  15:25:08,014 GenomeAnalysisEngine - Downsampling Settings: Method: BY_SAMPLE, Target Coverage: 1000 
INFO  15:25:08,022 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,061 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.04 
INFO  15:25:08,205 MicroScheduler - Running the GATK in parallel mode with 8 total threads, 1 CPU thread(s) for each of 8 data thread(s), of 64 processors available on this machine 
INFO  15:25:08,285 GenomeAnalysisEngine - Preparing for traversal over 1 BAM files 
INFO  15:25:08,402 GenomeAnalysisEngine - Done preparing for traversal 
INFO  15:25:08,403 ProgressMeter - [INITIALIZATION COMPLETE; STARTING PROCESSING] 
INFO  15:25:08,403 ProgressMeter -                 | processed |    time |    per 1M |           |   total | remaining 
INFO  15:25:08,404 ProgressMeter -        Location |     sites | elapsed |     sites | completed | runtime |   runtime 
INFO  15:25:08,570 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,581 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,582 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,594 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,595 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,604 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,605 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,614 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,615 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,624 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,625 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,634 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:08,635 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:25:08,646 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.01 
INFO  15:25:38,408 ProgressMeter -  chr1:234877841   2.12533248E8    30.0 s       0.0 s        7.6%     6.6 m       6.1 m 
INFO  15:26:08,411 ProgressMeter -  chr2:240099237   4.88522557E8    60.0 s       0.0 s       15.8%     6.3 m       5.3 m 
INFO  15:26:38,414 ProgressMeter -   chr4:53873693   7.32988904E8    90.0 s       0.0 s       24.0%     6.3 m       4.8 m 
INFO  15:27:08,416 ProgressMeter -  chr5:108993869   9.83469644E8   120.0 s       0.0 s       31.9%     6.3 m       4.3 m 
INFO  15:27:38,419 ProgressMeter -  chr6:157120977   1.217682056E9     2.5 m       0.0 s       39.3%     6.4 m       3.9 m 
INFO  15:28:08,424 ProgressMeter -   chr8:56842813   1.443766314E9     3.0 m       0.0 s       46.7%     6.4 m       3.4 m 
INFO  15:28:38,427 ProgressMeter -  chr10:21741769   1.678374295E9     3.5 m       0.0 s       54.9%     6.4 m       2.9 m 
INFO  15:29:08,429 ProgressMeter - chr11:114152145   1.929088562E9     4.0 m       0.0 s       62.2%     6.4 m       2.4 m 
INFO  15:29:38,432 ProgressMeter -  chr13:90982433   2.150203997E9     4.5 m       0.0 s       70.1%     6.4 m     114.0 s 
INFO  15:30:08,435 ProgressMeter -  chr15:98473957   2.381554391E9     5.0 m       0.0 s       77.6%     6.4 m      86.0 s 
INFO  15:30:38,438 ProgressMeter -  chr18:55373385   2.632206626E9     5.5 m       0.0 s       85.0%     6.5 m      58.0 s 
INFO  15:31:08,440 ProgressMeter -    chrX:2211157   2.863043654E9     6.0 m       0.0 s       93.0%     6.5 m      27.0 s 
INFO  15:31:38,443 ProgressMeter - chrGL000192.1:547489   3.050408131E9     6.5 m       0.0 s      100.0%     6.5 m       0.0 s 
INFO  15:32:08,446 ProgressMeter - chrGL000192.1:547489   3.063908547E9     7.0 m       0.0 s      100.0%     7.0 m       0.0 s 
INFO  15:32:17,050 ProgressMeter -            done   3.101804739E9     7.1 m       0.0 s      100.0%     7.1 m       0.0 s 
INFO  15:32:17,052 ProgressMeter - Total runtime 428.65 secs, 7.14 min, 0.12 hours 
INFO  15:32:17,058 MicroScheduler - 9960 reads were filtered out during the traversal out of approximately 80104 total reads (12.43%) 
INFO  15:32:17,058 MicroScheduler -   -> 0 reads (0.00% of total) failing BadCigarFilter 
INFO  15:32:17,058 MicroScheduler -   -> 52 reads (0.06% of total) failing BadMateFilter 
INFO  15:32:17,059 MicroScheduler -   -> 0 reads (0.00% of total) failing DuplicateReadFilter 
INFO  15:32:17,059 MicroScheduler -   -> 0 reads (0.00% of total) failing FailsVendorQualityCheckFilter 
INFO  15:32:17,059 MicroScheduler -   -> 0 reads (0.00% of total) failing MalformedReadFilter 
INFO  15:32:17,060 MicroScheduler -   -> 0 reads (0.00% of total) failing MappingQualityUnavailableFilter 
INFO  15:32:17,061 MicroScheduler -   -> 9905 reads (12.37% of total) failing MappingQualityZeroFilter 
INFO  15:32:17,061 MicroScheduler -   -> 0 reads (0.00% of total) failing NotPrimaryAlignmentFilter 
INFO  15:32:17,062 MicroScheduler -   -> 0 reads (0.00% of total) failing Platform454Filter 
INFO  15:32:17,062 MicroScheduler -   -> 3 reads (0.00% of total) failing UnmappedReadFilter 
INFO  15:32:18,748 GATKRunReport - Uploaded run statistics report to AWS S3 
</pre>
Process 31527 returned: (0). Elapsed: 0:07:33. Peak memory: (Process: 4.39GB; Pipeline: 3.783GB)

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.realigned.bam`
> `java -Xmx10g -jar /home/jinxu/software/GenomeAnalysisTK.jar -R /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta -T IndelRealigner  -known /home/jinxu/DB/hg19_g1k_v37/Mills_and_1000G_gold_standard.indels.hg19.sites.vcf  -known /home/jinxu/DB/hg19_g1k_v37/ALL.chrMT.phase3_callmom-v0_4.20130502.genotypes.Indel.vcf  -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam  -targetIntervals /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.target.intervals -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.realigned.bam`

<pre>
INFO  15:32:41,329 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:32:41,332 HelpFormatter - The Genome Analysis Toolkit (GATK) v3.5-0-g36282e4, Compiled 2015/11/25 04:03:56 
INFO  15:32:41,333 HelpFormatter - Copyright (c) 2010 The Broad Institute 
INFO  15:32:41,333 HelpFormatter - For support and documentation go to http://www.broadinstitute.org/gatk 
INFO  15:32:41,338 HelpFormatter - Program Args: -R /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta -T IndelRealigner -known /home/jinxu/DB/hg19_g1k_v37/Mills_and_1000G_gold_standard.indels.hg19.sites.vcf -known /home/jinxu/DB/hg19_g1k_v37/ALL.chrMT.phase3_callmom-v0_4.20130502.genotypes.Indel.vcf -I /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.bam -targetIntervals /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.target.intervals -o /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.realigned.bam 
INFO  15:32:41,344 HelpFormatter - Executing as jinxu@changrila2.stanford.edu on Linux 3.10.0-693.el7.x86_64 amd64; OpenJDK 64-Bit Server VM 1.8.0_161-b14. 
INFO  15:32:41,345 HelpFormatter - Date/Time: 2018/07/30 15:32:41 
INFO  15:32:41,346 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:32:41,346 HelpFormatter - -------------------------------------------------------------------------------- 
INFO  15:32:41,568 GenomeAnalysisEngine - Strictness is SILENT 
INFO  15:32:41,708 GenomeAnalysisEngine - Downsampling Settings: No downsampling 
INFO  15:32:41,716 SAMDataSource$SAMReaders - Initializing SAMRecords in serial 
INFO  15:32:41,755 SAMDataSource$SAMReaders - Done initializing BAM readers: total time 0.04 
INFO  15:32:42,232 GenomeAnalysisEngine - Preparing for traversal over 1 BAM files 
INFO  15:32:42,238 GenomeAnalysisEngine - Done preparing for traversal 
INFO  15:32:42,239 ProgressMeter - [INITIALIZATION COMPLETE; STARTING PROCESSING] 
INFO  15:32:42,239 ProgressMeter -                 | processed |    time |    per 1M |           |   total | remaining 
INFO  15:32:42,240 ProgressMeter -        Location |     reads | elapsed |     reads | completed | runtime |   runtime 
INFO  15:32:43,244 ReadShardBalancer$1 - Loading BAM index data 
INFO  15:32:43,245 ReadShardBalancer$1 - Done loading BAM index data 
INFO  15:33:02,382 ProgressMeter -            done     80921.0    20.0 s       4.1 m      100.0%    20.0 s       0.0 s 
INFO  15:33:02,383 ProgressMeter - Total runtime 20.14 secs, 0.34 min, 0.01 hours 
INFO  15:33:02,386 MicroScheduler - 0 reads were filtered out during the traversal out of approximately 80921 total reads (0.00%) 
INFO  15:33:02,387 MicroScheduler -   -> 0 reads (0.00% of total) failing BadCigarFilter 
INFO  15:33:02,387 MicroScheduler -   -> 0 reads (0.00% of total) failing MalformedReadFilter 
INFO  15:33:09,851 GATKRunReport - Uploaded run statistics report to AWS S3 
</pre>
Process 43563 returned: (0). Elapsed: 0:00:51. Peak memory: (Process: 1.592GB; Pipeline: 4.39GB)

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mpileup`
> `/usr/local/bin/samtools mpileup  -l /home/jinxu/DB/hg19_g1k_v37/chrM.len  -f /home/jinxu/DB/hg19_g1k_v37/human_g1k_v37.fasta  -q 20  -Q 20 -x /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.rmdup.realigned.bam > /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mpileup`

<pre>
[mpileup] 1 samples in 1 input files
<mpileup> Set max per-file depth to 8000
</pre>
Process 45507 returned: (0). Elapsed: 0:00:06.

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.counts`
> `/home/jinxu/bin/pileup_inf_rj.pl /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mpileup > /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.counts`

<pre>
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1647.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1707.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1733.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1739.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1741.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1771.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1776.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1778.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1920.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1922.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1926.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1950.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 1951.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 2933.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4072.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4075.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4080.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4082.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4083.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4084.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4089.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4415.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4417.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4418.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4422.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 4429.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7160.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7162.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7176.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7185.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7397.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7409.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7411.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 7413.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 8312.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 10020.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 11753.
Use of uninitialized value $seq in subtraction (-) at /home/jinxu/bin/pileup_inf_rj.pl line 73, <IN> line 15951.
</pre>
Process 45784 returned: (0). Elapsed: 0:00:06.
> ` awk 'BEGIN{sum=0;}''{sum+=$4;}''END{print sum}' /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.counts`

> ` awk 'BEGIN{num=0;}''{num++;}''END{print num}' /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.counts`

> `mt_aver_depth`	36.21	scATAC_mtSMC	_RES_

Target to produce: `/home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.snv`
> `java -Xmx4g  -jar /home/jinxu/software/VarScan.v2.3.7.jar  pileup2snp /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mpileup  --min-var-freq 0.01  --min-reads2 2  > /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.snv`

<pre>
Warning: No p-value threshold provided, so p-values will not be calculated
Min coverage:	8
Min reads2:	2
Min var freq:	0.01
Min avg qual:	15
P-value thresh:	0.99
Reading input from /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/Mapping_hg19/13-TAAGGCGA-GCGATCTA.mpileup
15951 bases in pileup file
11914 met minimum coverage of 8x
30 SNPs predicted
</pre>
Process 46094 returned: (0). Elapsed: 0:00:06.

Change status from running to completed

Cleaning up conditional list...

Removing glob: /home/jinxu/pipeline_pypiper/ATAC_mito_sc/example/output2/sc_output/13-TAAGGCGA-GCGATCTA/13-TAAGGCGA-GCGATCTA*.fq
> `Time`	0:10:20	scATAC_mtSMC	_RES_
> `Success`	07-30-15:33:46	scATAC_mtSMC	_RES_

##### [Epilogue:]
*   Total elapsed time:  0:10:20
*     Peak memory used:  4.39 GB
* Pipeline completed at:  (07-30 15:33:46) elapsed:0:10:17 _TIME_

Pypiper terminating spawned child process 29379...
child process terminated
close failed in file object destructor:
sys.excepthook is missing
lost sys.stderr
