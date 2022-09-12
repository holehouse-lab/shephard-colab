# SHEPHARD-colab

This contains data used in the Google colab notebooks for SHEPHARD and links to SHEPHARD Notebook Tutorials on Google-Colab

---
## SHEPHARD Code & Documentation
The SHEPHARD code can be found [here](https://github.com/holehouse-lab/shephard).

The SHEPHARD documentation can be found here: [https://shephard.readthedocs.io/en/latest/](https://shephard.readthedocs.io/en/latest/)

---
## Supporting Data & Manuscript Analysis Notebooks 

Ginell, Flynn & Holehouse 2022

All data and code used for the analysis in the paper can be found here [here](https://github.com/holehouse-lab/supportingdata/tree/master/2022/ginell_2022)

---
## Google-Colab Human Proteome Notebook
We provide a ready-to-analyze notebook with the annotated human proteome which can be taken and used to perform novel proteome-wide analysis. 

The human proteome is annotated with the following data:

1. Post-translational modifications
2. Intrinsically disordered regions
3. Prion-like domains
4. Per-residue secondary structure annotation
5. Per-residue solvation scores
6. Protein copy number

Once the first three cells are run, the user is free to either run the demo cells or begin novel analysis.

##### Google-Colab: [human\_proteome\_analysis](https://colab.research.google.com/drive/1cUHClcA4Fcl-byP_syIDRwycANpO8Na2)


## Google-Colab Tutorial Notebooks 
Below are links to run each of the SHEPHARD examples with google-colab:

To start learning how to use SHEPHARD click a google colab link below!

*NOTE: The analyses done in the example notebooks are purely a demonstration of what is capable in SHEPHARD*

| **Google-Colab Notebook Descriptions:** |
| :--- |
| [read_fasta_map_domains](https://github.com/holehouse-lab/shephard-colab#google-colab-read_fasta_map_domains),  [get_overlaping_domains](https://github.com/holehouse-lab/shephard-colab#google-colab-get_overlaping_domains),  [get_sequence_around_site](https://github.com/holehouse-lab/shephard-colab#google-colab-get_sequence_around_site),  [find_sites_near_PTMs](https://github.com/holehouse-lab/shephard-colab#google-colab-find_sites_near_ptms),  [find_lxvp_sites](https://github.com/holehouse-lab/shephard-colab#google-colab-find_lxvp_sites),  [uniprot_id_to_gene_name](https://github.com/holehouse-lab/shephard-colab#google-colab-uniprot_id_to_gene_name),  [add_callable_attributes](https://github.com/holehouse-lab/shephard-colab#google-colab-add_callable_attributes) |

### Working with sequences:

#### Domain Examples:

##### Google-Colab: [read_fasta_map_domains](https://colab.research.google.com/drive/1Q_OTNAxCHk43MeUQ4gCVs9GetUk_6fAI?usp=sharing)

Functionally the example script identifies the C- and N-terminal domains across the proteins, calculates the serine and glycine content
of those terminal domains, and returns the proteins that have C- of N- domains comprised of poly-GS. This example demonstrates how to: 

 * Read in a FASTA using `shephard.api.fasta` module
 * Add domains to proteins
 * Analyze domains 
 * Assign domain attributes

##### Google-Colab: [get_overlaping_domains](https://colab.research.google.com/drive/1gBSbQWtBzSwIm1SaR0Cj9Vk4CgU44DtW?usp=sharing)

This notebook provides an example for how to evaluate overlap of domains in proteins, as well as getting the 
fraction of overlap between any two domains. This example demonstrates how to: 

 * Initialize an empty proteome and add proteins 
 * Add domains to proteins
 * Use built-in domain manipulation functions and functions in `shephard.tools.domain_tools`
 * Calculate the fractional overlap between domains

#### Site Examples:

##### Google-Colab: [get_sequence_around_site](https://colab.research.google.com/drive/1bb_j9kTZj06NOJMfYOlQCGY3OAK6vR5d?usp=sharing) 

This example provides code that takes an input sequence and (1) defines all the arginines (R) residues as sites and (2) then gets the local sequence context around those sites. This example demonstrates how to: 

 * Initialize an empty proteome and add protein 
 * Find specific positions of residues
 * Add sites to proteins (adding a numerical value to the site)
 * Perform site-specific analysis
 * Get the local sequence context around a site

##### Google-Colab: [find_sites_near_PTMs](https://colab.research.google.com/drive/1D2TOFDO6rYgMjAQB3Ft1u_GEIFjSE_Yt?usp=sharing)

This notebook reads in all the proteins from the human proteome and annotates them with PTMs. It then calculates the frequency of PTMs near sites of dimethyl-arginine  in the human proteome. This example demonstrates how to: 

 * Initialize an empty proteome and add proteins from a shepard protein file 
 * Add sites from a sites file
 * Filter a proteome for sites of specific type
 * Get sites near other sites 
 * Add proteome attribute for quick reference of performed analysis
 * Calculate frequency of PTM sites proximal to a site type 

##### Google-Colab: [find_lxvp_sites](https://colab.research.google.com/drive/1iMDgYAozgNgGEn518XOp0IZGuWpcJ2Jb?usp=sharing)

This notebook reads in all the proteins and intrinsically disordered regions in the human proteome and annotates all examples of 'LXVP' motifs as Sites in the proteome. This example demonstrates how to: 

 * Read in a uniprot FASTA using the `shephard.api.uniprot` module
 * Add domains from a shepard domains file
 * Iterate over domains in proteome
 * Find amino acid patterns in domain sequences
 * Add and count site based on identified pattern locations

### Tools for streamlined analysis:

#### Working with attributes:

##### Google-Colab: [uniprot_id_to_gene_name](https://colab.research.google.com/drive/1kIyC9cBSPf9UeeMuUlwmupro77RZF0ef?usp=sharing)

This notebook provides an example for how to parse the complex protein headers of uniprot FASTA files and 
extract the proteins associated gene name. This example demonstrates how to: 

 * Read in a UniProt FASTA using the `shephard.api.uniprot` module
 * Parse the UniProt FASTA header when annotated as a protein name 
 * Add protein attribute
 * Write protein attributes using SHEPHARD interfaces 
 * Read in protein attributes using SHEPHARD interfaces

##### Google-Colab: [add_callable_attributes](https://colab.research.google.com/drive/1NwZJ9PWOy5B-XILBdX1Mo7L06NEq5ZtY?usp=sharing)

This notebook provides an example for how to use associated attributes to save functions and call them later in analysis. 

In this example, a lambda function is saved as proteome attribute which allows one to call the attribute and pass a protein length to 
identify the what percentile the in protein length is in in the proteome.  This example demonstrates how to: 

 *  Read in a UniProt FASTA using the `shephard.api.uniprot` module
 * Generate an array comprised of protein lengths in the proteome
 * Save a lambda function as proteome attribute 
 * Get the value of a parameter at a specific percentile relative to the proteome
 * Call a proteome attribute and pass it an input

