This file documents the code used to analyze and visualize mutations in the coat protein (CP) of the CPMosaicVirus. The analysis is based on the following four sequences:

aa_ORF5_Babaco
aa_ORF5_Papaya
aa_ORF5_Alternanthera
aa_ORF5_Senna
Workflow
Filter sequences: The script first filters the aa_CPMosaicVirus.fasta file to keep only the four relevant sequences.
Align sequences: The four sequences are aligned using MAFFT and the resulting alignment is saved as aa_ali_CPMosaicVirus.fasta.
Parse alignment: The alignment file is parsed using Biopython to extract the individual sequences as SeqRecord objects.
Create dictionary: A dictionary is created where the key is the sequence ID and the value is the corresponding SeqRecord object.
Define mutation function: A function is defined to identify amino acid mutations between two sequences.
Calculate pairwise mutations: The script calculates the number of amino acid mutations between each pair of sequences and stores the results in a dictionary.
Visualize mutations: A matplotlib plot is created to visualize the mutations for each sequence compared to the Babaco sequence. The plot shows the aligned amino acid sequences with the following elements:
Horizontal lines connecting sequences at the same position.
Labels for each sequence indicating the number of mutations compared to Babaco.
Individual mutation labels at the corresponding positions in the alignment.
Save plot: The plot is saved as PNG, JPEG, and PDF files.
Dependencies
Biopython
matplotlib
Running the script
Save the code as a Python script (e.g., mosaic_virus_analysis.py).
Make sure you have the required dependencies installed (pip install biopython matplotlib).
Run the script from the command line: python mosaic_virus_analysis.py.
This will create the plot files in the same directory as the script.

Output
The script generates three plot files:

MosaicVirus_CP_mutations.png
MosaicVirus_CP_mutations.jpg
MosaicVirus_CP_mutations.pdf
These files visualize the amino acid mutations between the Babaco sequence and the other three sequences.
