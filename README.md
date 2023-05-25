# MyMotifFinding

This project is designed to identify motifs in peak sequences. It provides several Python scripts that help to load reference genomes, compute GC content, identify peaks in the sequence, calculate scores of identified motifs, and compute the enrichment of motifs in bound sequences.

**Scripts**:

Background_Frequency.py: Calculates the background frequencies of nucleotides from a genome sequence in comparison to a list of sequences obtained from peaks.
MyMotifFinding.py: Performs motif finding in a provided peaks file.
findPValue.py: Computes the enrichment for each motif and provides Fisher Exact Test p-values.
utils.py: Provides utility functions for loading and processing data.

**Prerequisites**:

**Ensure you have the following installed on your system**:
1. Python 3.8 or higher
2. BioPython
3. NumPy
4. SciPy

**Getting Started**:

**Clone this repository**:
`git clone https://github.com/SaintLucifur/MyMotifFinding.git`

**Instructions**:

The order to run the scripts would be:

1. Run **Background_Frequency.py** script to calculate the background frequency.
    `python Background_Frequency.py`
2. Run **MyMotifFinding.py** with required parameters (HOMER peaks file, faidx Indexed Referencce Genome fasta file, and transfac file from JASPAR):
    `python MyMotifFinding.py --fasta-ref <path_to_fasta_ref> --out <output_file> --peaks <path_to_peaks_file> --fac <path_to_fac_file>`
3. Run **findPValue.py** to calculate the p-values for motif enrichment.
    `python findPValue.py`
4. The utils.py script does not need to be run directly as it is imported by the other scripts.

**Please replace <path_to_fasta_ref>, <output_file>, <path_to_peaks_file>, and <path_to_fac_file> with your actual file paths.**

**Testing**:

Minimal test datasets are included in the test folder for testing purposes. You can run the scripts with these datasets to verify the functionality of the scripts.

**Contributing**:

If you wish to contribute to this project, please create your own fork of this repository and submit a pull request.

**License**:

This project is licensed under the MIT License.
