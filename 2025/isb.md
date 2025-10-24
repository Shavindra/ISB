Transcriptome
Proteome 
Metablome
Data integration

10 data integration into genome scale models.pdf

transcriptomics: measures “all” the mRNA concentrations in a
cell
• proteomics: measures “all” the protein concentrations in a cell
• fluxomics: measures “all” the metabolic fluxes in a cell
• metabolmics: measures “all” the metabolite concentrations in a
cell

##  Summary 

### Charge balance

### FBA
FBA calculates the flow of metabolites through this metabolic network, thereby making it possible to predict the growth rate of an organism or the rate of production of a biotechnologically important metabolite. 

Defining bounds: Every reaction in a metabolic model has upper and lower bounds on its flux.Upper bound Vmax: Represents the maximum rate a reaction can operate at, often limited by factors like substrate availability or enzyme capacity.Lower bound Vmin: Represents the minimum rate. For reversible reactions, the lower bound is often set to the negative of the upper bound, while for irreversible reactions, it's frequently set to zero.Constraint on FBA: These bounds provide a realistic set of constraints, preventing the model from predicting infinite fluxes which are biologically impossible.

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