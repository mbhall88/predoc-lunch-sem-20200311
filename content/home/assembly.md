+++
weight = 22
+++
{{% section %}}

## Assessing (semi) *de novo* assemblies

---

## Data

Nine samples with **matched**  

-   Illumina >100x
-   Nanopore >100x
-   PacBio CCS >30x

🤘

---

<img src="images/dag.png"  height="650" width="800" style="border: none;">

---

## ALE score

A generic assembly likelihood evaluation framework for assessing the accuracy of genome and metagenome assemblies

> The assembly with the higher ALE score is also the one with the larger probability of being correct. Moreover, the difference between two assemblies’ ALE scores describes their relative probabilities of correctness.

<p id="ref">Scott C. Clark, Rob Egan, Peter I. Frazier, Zhong Wang, ALE: a generic assembly likelihood evaluation framework for assessing the accuracy of genome and metagenome assemblies, Bioinformatics, Volume 29, Issue 4, 15 February 2013, Pages 435–443, https://doi.org/10.1093/bioinformatics/bts723</p>

---

## ALE score

-   **Placement** - how well the reads match where they map (matches/orientation)
-   **Insert** - how well the mate pair's insert lengths match the expected length
-   **Depth** - how well depth at position agrees with expected, given GC content at location
-   **K-mer** - describes the likelihood of the assembly based on k-mer frequencies

---

![ale plot](images/ale.png)

---

## ALE score

| Assembler  | Count  |
|--:|---|
| Flye  | 4  |  
| Spades  |  3 |  
| Unicycler  | 2  |  



| Technology  | Count  |
|--:|---|
| Nanopore  | 2  |  
| PacBio  | 7  |

---

## Disagreement rate

---

![sample disagree plot](images/disagree_sample.png)

---

![assembler disagree plot](images/disagree_assembler.png)

---

## Disagreement rate

| Assembler  | Count  |
|--:|---|
| HASLR  | 7  |  
| Unicycler  | 2  |  



| Technology  | Count  |
|--:|---|
| Nanopore  | 6  |  
| PacBio  | 3  |

---

## Number of contigs

---

![number contigs plot](images/contigs.png)

---

## Number of contigs


| Assembler  | Count  |
|--:|---|
| Canu  | 12  |  
| Flye  | 10  |  
| Spades  | 8  |  
| HASLR  | 2  |  



| Technology  | Count  |
|--:|---|
| Nanopore  | 8  |  
| PacBio  | 24  |

---

## Total length

---

![Total length per sample plot](images/length_sample.png)

---

![Total length per assembler plot](images/length_assembler.png)

---

## Total length

| Assembler  | Count  | Sum (kbp) |
|--:|---|---|
| Canu  | 3  | 2335  |
| Flye  | 2  |  600  |  
| Unicycler  | 2  |  757  |  
| Spades  | 1  |  **163**  |  
| HASLR  | 1  |  1990  |  


| Technology  | Count  |
|--:|---|
| Nanopore  | 4  |  
| PacBio  | 5  |

---

## Mismatch rate

---

![mismatch rate plot](images/mismatch.png)

---

![mismatch technology plot](images/mismatch_tech.png)

---

## Mismatch rate

| Assembler  | Count  |
|--:|---|
| Unicycler  | 2  |  
| Spades  | 1  |  
| HASLR  | 6  |


| Technology  | Count  |
|--:|---|
| Nanopore  | 4  |  
| PacBio  | 5  |

---

## Indel rate

---

![indel rate plot](images/indel.png)

---

![indel rate technology plot](images/indel_tech.png)

---

## Indel rate

| Assembler  | Count  |
|--:|---|
| Unicycler  | 2  |  
| Spades  | 3  |  
| HASLR  | 4  |


| Technology  | Count  |
|--:|---|
| Nanopore  | 0  |  
| PacBio  | 9  |


{{% /section %}}
