+++
weight = 21
+++
{{% section %}}

## Tuberculosis

-   \#1 cause of death by a single pathogen
-   Standard of care requires phenotypic testing (DST) of the infecting organism - *Mycobacterium tuberculosis* - against the four first-line drugs
-   *M. tuberculosis* is slow-growing - gold-standard DST takes ~2 months

---

## Mtb genome

-   Some genes not present in H37Rv
-   ~10% of the genome consists of *pe/ppe* genes
    *   A disproportionately large amount of genetic diversity
    *   Nucleotide diversity ~2-fold higher than rest of the genome
    *   Sufficiently similar that short reads fail to map
-   Hard to extract long DNA fragments

---

## TB and Public Health

-   Public health requirements for TB diagnostics are resistance prediction, species identification, and clustering of genomes.
-   Requirements currently met with Illumina
-   Reasons to consider switching to Nanopore: cost, location of burden, speed
-   Patient to result in 12.5 hours (2017) with Nanopore - and yield has improved since then

---

## Genetic clustering

The first step towards clustering a set of genomes is determining a distance matrix.

-   Counting SNP differences and clustering based on these

---

# How

Benchmark Nanopore versus Illumina SNP calling and show our algorithms meet the needs of clinical and public health users.

---

## Species-specific nanopore basecalling

![basecalling comparison](images/basecalling.png)

<p id="ref">Wick, R.R., Judd, L.M. & Holt, K.E. Performance of neural network basecalling tools for Oxford Nanopore sequencing. Genome Biol 20, 129 (2019). https://doi.org/10.1186/s13059-019-1727-y</span>

---

### Need truth for nanopore reads

{{% /section %}}
