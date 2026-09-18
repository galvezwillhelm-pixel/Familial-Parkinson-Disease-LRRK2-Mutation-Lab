# From Gene Mutation to Disease: Molecular Analysis of the LRRK2 G2019S Variant in Familial Parkinson Disease

**Student:** Willhelm Galvez  
**Course:** Cell and Molecular Biology Laboratory  
**Disease/Phenotype:** Familial Parkinson Disease  
**Gene:** LRRK2  
**Reference Transcript:** NM_198578.4  
**Reference Protein:** NP_940980.4  
**Documented Variant:** NM_198578.4:c.6055G>A  
**Protein Change:** p.Gly2019Ser (G2019S)

---

## Disease Background

Familial Parkinson disease associated with LRRK2 is a hereditary neurodegenerative disorder that mainly affects movement. Common clinical manifestations include bradykinesia, resting tremor, rigidity, gait disturbance, and postural instability. The disorder primarily affects the nervous system, particularly dopaminergic neurons associated with the substantia nigra and basal ganglia motor pathways.

The genetic basis of this form of Parkinson disease involves pathogenic variants in the LRRK2 gene. LRRK2-associated Parkinson disease is usually inherited in an autosomal dominant manner, although penetrance may be incomplete and age-dependent. The documented mutation investigated in this activity was NM_198578.4:c.6055G>A, which produces the amino-acid substitution p.Gly2019Ser, commonly called G2019S.

---

## Gene and Normal Protein Function

The official gene symbol is LRRK2, which stands for leucine rich repeat kinase 2. The gene is located on chromosome 12 at 12q12. The reference transcript used in this investigation was NM_198578.4, and the corresponding reference protein was NP_940980.4.

LRRK2 encodes leucine-rich repeat serine/threonine-protein kinase 2, a large multidomain protein with kinase and GTPase-related functions. It participates in intracellular signaling, Rab-mediated membrane trafficking, vesicle transport, endolysosomal regulation, autophagy-related processes, and cytoskeletal regulation.

LRRK2 is mainly cytoplasmic but can associate with intracellular membranes and organelles. The G2019 residue is located within the kinase domain, making this position functionally important because changes in this region can alter kinase activity.

---

## Documented Mutation

The documented mutation selected was **NM_198578.4:c.6055G>A**. This nucleotide substitution produces the protein change **p.Gly2019Ser (G2019S)**.

The mutation is a missense single-nucleotide substitution. At CDS nucleotide position 6055, the wild-type nucleotide G was replaced by A.

The wild-type codon was:

**GGC = Glycine**

The mutant codon was:

**AGC = Serine**

Therefore:

**GGC → AGC**  
**Glycine 2019 → Serine 2019**

Only one nucleotide was substituted. No nucleotide was inserted or deleted, so the reading frame remained unchanged.

---

## Hypothesis

It was predicted that the c.6055G>A mutation would produce a missense substitution without changing the reading frame or total protein length. Glycine at amino-acid position 2019 was expected to be replaced by serine.

Because residue 2019 is located within the LRRK2 kinase domain, the substitution was predicted to affect protein function despite changing only one amino acid. The mutant protein was expected to remain full length but potentially show altered kinase activity.

---

## Methods

### Reference Sequence Retrieval

The human LRRK2 reference transcript NM_198578.4 was obtained from the NCBI RefSeq database. Only the coding sequence or CDS was downloaded in FASTA nucleotide format. The corresponding reference protein was NP_940980.4.

The WT CDS was saved as:

`LRRK2_WT_CDS.fasta`

It was uploaded to a Galaxy history named:

`Galvez_Familial_Parkinson_Disease_LRRK2_Mutation_Lab`

### Wild-Type Translation

The WT CDS was translated using SeqKit translate in Galaxy using Frame 1 and the Standard Genetic Code. The predicted protein was saved as:

`LRRK2_WT_protein.fasta`

The predicted protein was compared with the accepted reference protein NP_940980.4.

### Creation of the Documented Mutation

A copy of the WT CDS was used so that the original WT sequence remained unchanged.

Using the Galaxy Replace parts of text tool, the sequence:

`TGCTGACTACGGCATTGCTCA`

was replaced with:

`TGCTGACTACAGCATTGCTCA`

This reproduced the documented c.6055G>A mutation.

The mutant CDS was saved as:

`LRRK2_G2019S_CDS.fasta`

The mutant CDS was translated using the same SeqKit settings as the WT and saved as:

`LRRK2_G2019S_protein.fasta`

### WT and Mutant Protein Comparison

The WT and G2019S protein FASTA files were combined using Concatenate datasets tail-to-head. The combined sequences were aligned using MAFFT in amino-acid mode with BLOSUM62 scoring.

The alignment was saved as:

`LRRK2_WT_vs_G2019S_alignment.fasta`

### Artificial Mutation Experiment

A separate WT CDS copy was used to create a student-designed one-nucleotide deletion. One guanine at CDS position 1500 was deleted, producing **c.1500delG**.

This artificial mutation was created only for the controlled sequence experiment and was not considered a documented Parkinson disease mutation.

The artificial mutant CDS was translated using SeqKit, and the predicted protein was compared with the WT protein using MAFFT.

---

## Results

### Wild-Type LRRK2

The WT LRRK2 CDS contained 7,584 nucleotides. It began with the start codon ATG and ended with the stop codon TAA.

Translation produced a predicted protein containing 2,527 amino acids, consistent with the reference protein NP_940980.4.

| Characteristic | Result |
|---|---|
| Transcript accession | NM_198578.4 |
| Protein accession | NP_940980.4 |
| CDS length | 7,584 nt |
| Start codon | ATG |
| Stop codon | TAA |
| Reading frame | Frame 1 |
| Predicted protein length | 2,527 aa |
| First 10 amino acids | MASGSCQGCE |
| Last 10 amino acids | AEKMRRTSVE |

### Documented G2019S Mutation

| Characteristic | Result |
|---|---|
| DNA variant | c.6055G>A |
| WT codon | GGC |
| Mutant codon | AGC |
| WT amino acid | Glycine |
| Mutant amino acid | Serine |
| Protein change | p.Gly2019Ser |
| Mutation type | Missense |
| CDS length | 7,584 nt |
| Protein length | 2,527 aa |
| Frameshift | No |
| Premature stop codon | No |
| First difference | Amino acid 2019 |

---

## WT versus Mutant Protein Comparison

The WT and G2019S protein sequences first differed at amino-acid position 2019.

The WT residue was glycine, while the mutant residue was serine.

A local comparison was:

**WT:**  
`AAIIAKIADYGIAQYCCRMGI`

**G2019S:**  
`AAIIAKIADYSIAQYCCRMGI`

Only one amino acid was affected. No amino acid was inserted or deleted, no premature stop codon was produced, and the reading frame remained unchanged.

Both WT and G2019S predicted proteins contained 2,527 amino acids. Therefore, the documented G2019S mutation caused a localized missense substitution rather than a frameshift or protein truncation.

---

## Artificial Mutation Experiment

The artificial mutation consisted of a one-nucleotide deletion:

**c.1500delG**

Before translation, it was predicted that deleting one nucleotide would alter the reading frame because one nucleotide is not divisible by three. This was expected to change multiple downstream codons and possibly create a premature stop codon.

The WT CDS contained 7,584 nucleotides, whereas the artificial mutant CDS contained 7,583 nucleotides.

The first altered amino acid occurred at position 501.

The WT residue at position 501 was:

**Q = Glutamine**

The artificial mutant residue was:

**S = Serine**

The frameshift generated a premature stop codon at position 512. Therefore, the biologically relevant predicted translation would terminate after approximately 511 amino acids.

| Characteristic | WT | Artificial c.1500delG |
|---|---:|---:|
| CDS length | 7,584 nt | 7,583 nt |
| Mutation type | None | 1-nt deletion / frameshift |
| Reading-frame change | No | Yes |
| First altered amino acid | — | Position 501 |
| Residue at position 501 | Q | S |
| Premature stop codon | No | Position 512 |
| Predicted product before first stop | 2,527 aa | About 511 aa |

The artificial mutation therefore produced a much more severe predicted effect than the documented G2019S mutation.

---

## Molecular Interpretation: Gene → Mutation → Protein → Cellular Effect → Phenotype

The molecular mechanism of the documented mutation can be summarized as:

**LRRK2 gene**  
↓  
**c.6055G>A nucleotide substitution**  
↓  
**GGC codon changes to AGC**  
↓  
**Glycine 2019 changes to serine**  
↓  
**Alteration within the LRRK2 kinase domain**  
↓  
**Altered kinase activity reported in published studies**  
↓  
**Changes in phosphorylation and intracellular signaling**  
↓  
**Disturbance of vesicular and endolysosomal processes**  
↓  
**Impaired neuronal cellular homeostasis**  
↓  
**Contribution to Parkinson disease phenotype**

The computational analysis directly demonstrated the nucleotide and predicted protein-sequence consequences of the mutation. Specifically, c.6055G>A changed the codon GGC to AGC and produced the predicted Gly2019Ser substitution.

However, the Galaxy analysis did not directly demonstrate kinase activity, protein expression, intracellular trafficking defects, neuronal degeneration, or clinical symptoms. Those biological conclusions require evidence from published experimental and clinical studies.

---

## Limitations

This investigation was computational and sequence based. Galaxy translation predicts the amino-acid sequence encoded by a CDS but does not demonstrate whether the protein is actually expressed, correctly folded, properly localized, stable, or biologically active inside human cells.

The activity did not directly measure LRRK2 kinase activity, Rab phosphorylation, vesicle trafficking, lysosomal function, neuronal survival, dopamine concentration, or Parkinson disease symptoms.

The artificial c.1500delG mutation was generated only as a controlled sequence experiment. It was not considered a documented Parkinson disease-associated mutation.

In addition, the artificial-mutant translation output may still display amino-acid sequence after an asterisk because sequence translation software can continue reading the nucleotide sequence. Biologically, the first premature stop codon at position 512 was interpreted as the termination point of the predicted protein.

---

## Conclusion

This investigation demonstrated how different DNA mutations can produce different molecular consequences.

The documented LRRK2 mutation c.6055G>A changed the codon GGC to AGC and produced the amino-acid substitution p.Gly2019Ser at position 2019. The mutation did not alter the reading frame, generate a premature stop codon, or change the predicted protein length. Both WT and G2019S proteins contained 2,527 amino acids.

Because G2019S occurs within the LRRK2 kinase domain, published experimental evidence supports the idea that the mutation can alter kinase activity and contribute to disturbed intracellular signaling associated with Parkinson disease.

In contrast, the artificial c.1500delG mutation removed one nucleotide and caused a frameshift. Multiple downstream amino acids changed, and a premature stop codon appeared at position 512, predicting a severely truncated protein.

These results demonstrate that the molecular consequence of a mutation depends on its type, exact position, effect on the reading frame, and the functional importance of the affected protein region.

---

## References

National Center for Biotechnology Information. LRRK2 leucine rich repeat kinase 2 [Homo sapiens]. NCBI Gene. Gene ID: 120892.

National Center for Biotechnology Information. NM_198578.4(LRRK2):c.6055G>A (p.Gly2019Ser) and autosomal dominant Parkinson disease 8. ClinVar. RCV000002017.

Wise, A., Raymond, D., & Saunders-Pullman, R. LRRK2-Related Parkinson Disease. GeneReviews®. University of Washington, Seattle.

Di Fonzo, A., Rohé, C. F., Ferreira, J., et al. (2005). A frequent LRRK2 gene mutation associated with autosomal dominant Parkinson's disease. The Lancet, 365(9457), 412–415.

West, A. B., Moore, D. J., Biskup, S., et al. (2005). Parkinson's disease-associated mutations in leucine-rich repeat kinase 2 augment kinase activity. Proceedings of the National Academy of Sciences, 102(46), 16842–16847.

Covy, J. P., & Giasson, B. I. (2010). The G2019S pathogenic mutation disrupts sensitivity of leucine-rich repeat kinase 2 to manganese kinase inhibition. Journal of Neurochemistry, 115(1), 36–48.
