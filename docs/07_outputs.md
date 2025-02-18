Outputs files may be aggregated including information for all samples or provided per sample. Per-sample files will be prefixed with respective aliases and represented below as {{ alias }}.

| Title | File path | Description | Per sample or aggregated |
|-------|-----------|-------------|--------------------------|
| workflow report | wf-transcriptomes-report.html | a HTML report document detailing the primary findings of the workflow | aggregated |
| Per file read stats | fastq_ingress_results/reads/fastcat_stats/per-file-stats.tsv | A TSV with per file read stats, including all samples. | aggregated |
| Read stats | fastq_ingress_results/reads/fastcat_stats/per-read-stats.tsv | A TSV with per read stats, including all samples. | aggregated |
| Run ID's | fastq_ingress_results/reads/fastcat_stats/run_ids | List of run IDs present in reads. | aggregated |
| Meta map json | fastq_ingress_results/reads/metamap.json | Metadata used in workflow presented in a JSON. | aggregated |
| Concatenated sequence data | fastq_ingress_results/reads/{{ alias }}.fastq.gz | Per sample reads concatenated in to one FASTQ file. | per-sample |
| Assembled transcriptome | {{ alias }}_transcriptome.fas | Per sample assembled transcriptome. | per-sample |
| Annotated assembled transcriptome | {{ alias }}_merged_transcriptome.fas | Per sample annotated assembled transcriptome. | per-sample |
| Alignment summary statistics | {{ alias }}_read_aln_stats.tsv | Per sample alignment summary statistics. | per-sample |
| GFF compare results. | {{ alias }}_gffcompare | All GFF compare output files. | per-sample |
| Differential gene expression results | /de_analysis/results_dge.tsv | This is a gene-level result file that describes genes and the probability that they show differential expression between experimental conditions . | aggregated |
| Differential gene expression report | /de_analysis/results_dge.pdf | Summary report of differential gene expression analysis as a PDF. | aggregated |
| Differential transcript usage gene TSV | /de_analysis/results_dtu_gene.tsv | This is a gene-level result file from DEXSeq that lists annotated genes and their probabilities of differential expression. | aggregated |
| Differential transcript usage report | /de_analysis/results_dtu.pdf | Summary report of differential transcript usage results as a PDF. | aggregated |
| Differential transcript usage TSV | /de_analysis/results_dtu_transcript.tsv | This is a transcript-level result file from DEXSeq that lists annotated genes and their probabilities of differential expression. | aggregated |
| Differential transcript usage stageR TSV | /de_analysis/results_dtu_stageR.tsv  | This is the output from StageR and it shows both gene and transcript probabilities of differential expression | aggregated |
| Differential transcript usage DEXSeq TSV | /de_analysis/results_dexseq.tsv | The complete output from the DEXSeq-analysis, shows both gene and transcript probabilities of differential expression. | aggregated |
| Gene counts | /de_analysis/all_gene_counts.tsv | Raw gene counts created by the Salmon tool, before filtering. | aggregated |
| Transcript counts | /de_analysis/all_transcript_counts.tsv | Raw transcript counts created by the Salmon tool, before filtering. | aggregated |
| Transcript counts filtered | /de_analysis/all_counts_filtered.tsv | Filtered transcript counts, used for DE_analysis. | aggregated |
| Transcript per million counts | /de_analysis/de_tpm_transcript_counts.tsv | This file shows transcript per million (TPM) of the raw counts to facilitate comparisons across sample. | aggregated |
| Final non redundant transcriptome | /de_analysis/final_non_redundant_transcriptome.fasta | Transcripts that were used for differential expression analysis including novel transcripts with the identifiers used for DE analysis. | aggregated |
| Fusion transcript sequences | /jaffal_output_{{ alias }}/jaffa_results.fasta | Fusion transcript sequences output by Jaffa. | per-sample |
| Fusion transcript sequence summary file | /jaffal_output_{{ alias }}/jaffa_results.csv | Fusion transcript sequences summary file output by Jaffa. | per-sample |
