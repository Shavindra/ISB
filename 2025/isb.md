##  Summary 

### Charge balance

### FBA
FBA calculates the flow of metabolites through this metabolic network, thereby making it possible to predict the growth rate of an organism or the rate of production of a biotechnologically important metabolite. 

Defining bounds: Every reaction in a metabolic model has upper and lower bounds on its flux.Upper bound Vmax: Represents the maximum rate a reaction can operate at, often limited by factors like substrate availability or enzyme capacity.Lower bound Vmin: Represents the minimum rate. For reversible reactions, the lower bound is often set to the negative of the upper bound, while for irreversible reactions, it's frequently set to zero.Constraint on FBA: These bounds provide a realistic set of constraints, preventing the model from predicting infinite fluxes which are biologically impossible.


### DATA INTEGRATION


transcriptomics: measures “all” the mRNA concentrations in a cell
- proteomics: measures “all” the protein concentrations in a cell
-fluxomics: measures “all” the metabolic fluxes in a cell
- metabolmics: measures “all” the metabolite concentrations in a cell


![](https://github.com/Shavindra/ISB/blob/main/2025/assets/flux.png?raw=true)

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/flux2.png?raw=true)

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/flux3.png?raw=true)

### Null space and vectors

* It’s not “elements in each **reaction** add up to zero,” it’s: for each **metabolite (row of** (S)), the **net production rate equals zero** at steady state. In matrix speak: (S,v=\mathbf{0}). That set ({v\mid S v=0}) is exactly the **null space** (kernel) of (S) and contains all steady-state flux vectors. 

* If a flux vector (v) satisfies (S,v=0), then yes—(v) is in the null space (and is a valid steady-state flux). A **collection of linearly independent** such vectors **spans** the null space. Their columns are often shown as a **kernel matrix**; each column is a **flux mode** (a steady-state route).

* Any **linear combination** of those spanning vectors stays in the null space.

* Practical caveat: the null space is purely stoichiometric. Feasibility also needs bounds/directionality (e.g., 𝑣vmin ≤ v ≤v max


### Medical and biotechnological applications of flux modes
1. Whether a microbe can produce a product implies that at least one flux mode exists that makes it
2. Whether a microbe can grow on a medium implies that a flux mode exists that allows for growth from all those medium components. 
3. 
3. If you want to kill a pathogenic microbe you inhibit the set of enzyme(s) (can have 1 element) such that no flux mode exists that supports growth
4. If a cancer cell makes more product than theoretically expected from knowledge of one flux mode, then at least one more flux mode exists that makes the compound. E.g. more than two molecules of lactate cannot be made from a single molecule of glucose. If


## Summary notes
### Genome annotations
Genome annotationis the process of finding and designating locations of individual genes and other features on raw DNA sequences, calledassemblies.
Annotation gives meaning to a given sequence and makes it much easier for researchers to view and analyze its contents.
![](https://github.com/Shavindra/ISB/blob/main/2025/gene_annotations.png?raw=true?raw=true)

### Metabolic Regulation
![](https://github.com/Shavindra/ISB/blob/main/2025/assets/metabolic_regulation.png?raw=true)

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/metabolic_reg2.png?raw=true)

the rate (isotopomer flux analysis) of an enzyme-catalysed reaction depends on the 
- concentrations of the reactants (metabolomics)
- the concentration of the enzyme (proteomics), set by its mRNA concentration (transcriptomics), set by the gene activity, and set by mRNA and protein degradation rates
- the kinetic parameters of the enzyme, set by the gene sequence, 3D protein structure and organic chemistry of the catalysis the enzyme mechanism

### Protein Synthesis
**GENE (promoter + coding region)**
   
   > **↓ transcription (RNA polymerase)**
   
**pre-mRNA —[5′ cap | splicing | poly-A]→ mRNA (5′UTR • AUG • coding • STOP • 3′UTR)**
   
  >  **↓ translation (ribosome + tRNAs)**

**amino-acid chain —[folding/PTMs/targeting]→ functional protein**
![](https://github.com/Shavindra/ISB/blob/main/2025/assets/protein_synth.png?raw=true)

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/protein_synth.png?raw=true)
![](https://github.com/Shavindra/ISB/blob/main/2025/assets/transcription.png?raw=true)
![](https://github.com/Shavindra/ISB/blob/main/2025/assets/translation.png?raw=true)


### Transcription & Translation — high-level overview (UK)

#### Big picture

**DNA → transcription → RNA → translation → protein**
Cells first make a **copy of a gene** into RNA, then **use that message** to build a protein.

---

#### Transcription (making RNA from DNA)

* **Purpose:** turn the information in a gene into a **portable message (mRNA)**.
* **Where:** in the **nucleus** (eukaryotes); in the **cytoplasm** (prokaryotes).
* **How (simple):** a polymerase **binds near a gene, moves along the DNA**, and **builds a matching RNA strand** until it reaches a **stop signal**.
* **Afterwards (eukaryotes):** the RNA is **tidied up** (capped, spliced, and given a tail) so it’s ready for export and use.
* **Outcome:** a **mature mRNA** that carries the recipe for a protein.

---

#### Translation (making protein from mRNA)

* **Purpose:** **decode** the mRNA to assemble a **chain of amino acids** that folds into a functional protein.
* **Where:** at **ribosomes** in the cytoplasm (and on the rough ER in eukaryotes).
* **How (simple):** the ribosome **locks onto the mRNA**, reads it in **three-letter “words” (codons)**, and **adds the matching amino acids** with the help of adaptor molecules, until a **stop** is reached.
* **Outcome:** a **new protein**, ready to fold and (often) be modified or delivered to where it’s needed.

---

#### A few big differences to remember

* **Separation:** In **eukaryotes**, transcription (nucleus) and translation (cytoplasm) are **separate**; in **prokaryotes** they can happen **at the same time**.
* **Processing:** Eukaryotic mRNA is **processed** before use; prokaryotic mRNA is **used as made**.
* **Control points:** Cells regulate gene expression mostly by **when/how much RNA is made**, **how stable the mRNA is**, and **how efficiently it’s translated**.

---



#### Key takeaways

* Transcription = **copy the recipe**; translation = **cook the dish**.
* Messages are read in **codons**; there’s a **start**, a **reading frame**, and a **stop**.
* Both steps **use energy** and are **tightly controlled** to meet the cell’s needs.

### Metabolism — quick revision sheet

#### 1) ATP from glycolysis (per glucose)

* **Net ATP:** **2**
* (4 ATP produced − 2 ATP invested = **2 ATP net**)
* Also yields **2 NADH** and **2 pyruvate**.

####  2) Catabolism

* **Breakdown** pathways that convert complex molecules → simpler ones, **releasing energy** (captured as **ATP** and reduced cofactors like **NADH/NADPH**) and generating intermediates for biosynthesis.

####  3) Anabolism

* **Biosynthetic** pathways that assemble complex molecules from simpler precursors, **requiring energy** (**ATP**) and **reducing power** (typically **NADPH**).

####  4) Small molecules vs precursor metabolites

* **Small molecules:** low-molecular-weight metabolites (e.g., amino acids, monosaccharides, nucleotides, fatty acids, acetyl-CoA, pyruvate, vitamins).
* **Precursor metabolites:** a **defined set of central-carbon intermediates** that feed anabolism (e.g., glucose-6-P, fructose-6-P, glyceraldehyde-3-P, 3-phosphoglycerate, PEP, pyruvate, acetyl-CoA, oxaloacetate, α-ketoglutarate, ribose-5-P, erythrose-4-P, succinyl-CoA).

####  5) Macromolecules and their monomers

| Macromolecule                    | Built from (monomers)                             | Notes / examples                                                                   |
| -------------------------------- | ------------------------------------------------- | ---------------------------------------------------------------------------------- |
| **Proteins**                     | **Amino acids**                                   | Peptide bonds form polypeptides.                                                   |
| **Nucleic acids (DNA/RNA)**      | **Nucleotides** (deoxy-/ribo-)                    | Phosphodiester backbone; base pairing.                                             |
| **Polysaccharides**              | **Monosaccharides** (e.g., glucose)               | Glycogen, starch, cellulose (glycosidic bonds).                                    |
| **Lipids** *(not true polymers)* | **Fatty acids** + **glycerol** (± phosphate/head) | Triacylglycerols; phospholipids (glycerol-P + head group); sterols from isoprenes. |
| **Bacterial peptidoglycan**      | **NAG/NAM sugars** + short **peptides**           | Forms the cell wall mesh.                                                          |

####  6) Why cells require energy

* **Drive endergonic reactions** and maintain **low entropy/order**.
* **Biosynthesis** of macromolecules and assembly of cellular structures.
* **Active transport** and maintenance of **ion gradients/membrane potential**.
* **Mechanical work** (e.g., motility, muscle contraction, cytokinesis).
* **Signalling**, **repair**, **turnover**, **detoxification**, and general **homeostasis**.
* In some organisms, **thermogenesis** (heat production).

---


## Workgroup 1
1. The European Space Agency (ESA) has asked you to design a probe that will look
for signs of life in another planet. What will your probe search for?

    > Chemical signatures
    > Molecular signatures
    > Bio Signautres
    > Environmental condtions
   
2. The function of a protein depends on it’s three dimensional structure, but
knowing how a protein folds in 3D is a complex problem. Do you see any way
trying to predict a protein function from its sequence?

    > Homologs. 

5. Imagine you have a process, with a variable rate, that is making a product **A**. Another process is also consuming **A**. It’s very important to keep the concentration of **A** as stable as possible.
    **a)** If you have complete control over the production of **A**, how would you design a **controller** to keep **[A]** stable? What would you **measure**, and what would you **influence**?
    **b)** Could the mechanism you described be done **using only molecular interactions**? Explain briefly. 


## Example
![](https://github.com/Shavindra/ISB/blob/main/2025/assets/1.png?raw=true)


## FLOW

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/2.png?raw=true)

![](https://github.com/Shavindra/ISB/blob/main/2025/assets/3.png?raw=true)


## Glossary
**Genome annotation**
> is the process of finding and designating locations of individual genes and other features on raw DNA sequences, calledassemblies.
Annotation gives meaning to a given sequence and makes it much easier for researchers to view and analyze its contents.

**Homologs**
> Homology refers to biological features including genes and their products that are descended from a feature present in a common ancestor. Homologous features such as genes are referred to as homologs 

** Anfinsen Dogma**
> 

Translation

Transcription



A pivot (element) is the first nonzero entry in a row when the matrix is in (row) echelon form—i.e., scanning left→right within that row.
A row of all zeros has no pivot.

If a diagonal entry is 0 during elimination, you typically swap rows to bring a nonzero into that pivot position (partial pivoting).