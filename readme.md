# SHEPHARD-colab

This contains data used in the Google colab notebooks for SHEPHARD and links to SHEPHARD Notebook Tutorials on Google-Colab

---
## SHEPHARD Code & Documentation
The SHEPHARD Code can be found [here](https://github.com/holehouse-lab/shephard).

SHEPHARD Documentation: https://shephard.readthedocs.io/en/latest/

---
## Supporting Data & Manuscript Analysis Notebooks 

Ginell et al. 2022

Notebooks for specific analysis found in paper are [here](https://github.com/holehouse-lab/supportingdata/tree/master/2022/ginell_2022)

---
## Google-Colab Tutorial Notebooks 
Below are links to run each of the SHEPHARD examples with google-colab:

To start learning how to use SHEPHARD click a google colab link below!

*NOTE: The analyses done in the example notebooks are purely a demonstration of what is capable in SHEPHARD*

### Working with sequences:

#### Domain Examples:

[read_fasta_map_domains](https://colab.research.google.com/drive/1Q_OTNAxCHk43MeUQ4gCVs9GetUk_6fAI?usp=sharing)

Functionally the example script identifies the C- and N- domains of protiens, calculates the Serine and Glycine content
of the terminal domains, and returns protiens that have C- of N- domains comprised of Poly-GS. This example demostrates how to: 

 * Read in a FASTA using SHEPHARD.APIs 
 * Add domains to protiens
 * Anylize domains assigning domain attributes

[get_overlaping_domains](https://colab.research.google.com/drive/1gBSbQWtBzSwIm1SaR0Cj9Vk4CgU44DtW?usp=sharing)

Here this notebook provides an example for how to evaluate overlap of domains in a protien, as well as getting the 
fraction of overlap between any two domains. This example demostrates how to: 

 * Initialize an empty proteome and add proteins 
 * Add domains to proteins
 * Use build-in domain functions and domain_tools 
 * Evaluate for overlaping domains

#### Site Examples:

[get_sequence_around_site](https://colab.research.google.com/drive/1bb_j9kTZj06NOJMfYOlQCGY3OAK6vR5d?usp=sharing) 

The get_sequence_around_site example takes and inputed protien sequence and defines all the Arginines (R) residues
as sites and then gets the local sequence context around these sites. This example demostrates how to: 

 * Initialize an empty proteome and add protein 
 * Find specific positions of residues
 * Add sites to proteins (adding a numerical value to the site)
 * Perform Site specific analysis
 * Get local sequence around a Site

[find_sites_near_PTMs](https://colab.research.google.com/drive/1D2TOFDO6rYgMjAQB3Ft1u_GEIFjSE_Yt?usp=sharing)

This notebook reads in all the proteins and annotated PTMs in the human proteome and calculates the 
frequency occurence of PTMs near Dimethylation sites in the human proteome. This example demostrates how to: 

 * Initialize an empty proteome and add proteins from shprd protein file 
 * Add sites from shprd site file
 * Filter proteome for sites of specific type
 * Get sites near other sites 
 * Add proteome attribute for quick reference of performed analysis
 * Calculate frequency of PTM sites proximal to a site type 

[find_lxvp_sites](https://colab.research.google.com/drive/1iMDgYAozgNgGEn518XOp0IZGuWpcJ2Jb?usp=sharing)

This notebook reads in all the proteins and Intrisically disordered regions in the human proteome and uses 
python string parsing to map all 'LXVP' as Sites in the proteome. This example demostrates how to: 

 * Read in a uniprot FASTA using SHEPHARD.APIs 
 * Add domains from shprd domains file
 * Iterate over domains in proteome
 * Find amino acid patterns in domain sequences (using string parsing)
 * Add and count site based on identified pattern locations

### Tools for streemlined analysis:

#### Working with attributes:

[add_callable_attributes](https://colab.research.google.com/drive/1NwZJ9PWOy5B-XILBdX1Mo7L06NEq5ZtY?usp=sharing)

This notebook provides an example for how to use associated attributes to save functions and call them later in analysis. In
this example a lambda function is saved as proteome attribute which allows one to call the attribute and pass a protein length to 
identify the what percentile the in protein legnth is in in the proteome.  This example demostrates how to: 

 * Read in a uniprot FASTA using SHEPHARD.APIs 
 * Generate an array comprised of protein lengths in proteome
 * Save a lambda function as proteome attribute 
 * Get the value of a parameter at a specific percentile relitive to the proteome
 * Call a proteome attribute and pass it an intput

