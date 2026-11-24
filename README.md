# L2C90 computational verification

Computational material for *Characterization of graphs with second largest eigenvalue at most 1 and clique number at least 90*.

**Authors:** Chaohui Chen, Hangxi Cha and Haiying Shan.

## Files

- **`L2C90.ipynb`** contains the exact Python enumeration of minimal forbidden marked graphs and the positive-semidefinite 67-screen used in Propositions 2.6 and 2.7. The notebook includes saved results from a complete run.
- **`D.txt`** contains the resulting catalogue, one marking-preserving isomorphism class per line. Each line is `marking graph6(H)`, where `graph6(H)` encodes the graph $H$, not its support graph. Line numbers begin at 1.

## Results

The enumeration through order 10 gives **1,878** minimal forbidden marked graphs. The counts by orders 3–10 are 4, 9, 14, 18, 22, 75, 323 and 1,413. Of the 1,878 graphs, **1,812** are all marked and **66** contain at least one unmarked vertex.

For every $(H,\boldsymbol c)$ in the catalogue, the notebook tests

$$
67\bigl(\widehat A(H,\boldsymbol c)+2I\bigr)
+2\boldsymbol c\boldsymbol c^{\mathsf T}\succeq0.
$$

The only survivor is the fully marked graph $H_*=K_1\vee(K_6\cup K_2\cup K_1)$ (catalogue entry 792).

The paper proves that the relevant minimal forbidden marked graphs have at most ten vertices. This order bound is used as an input to the finite enumeration.

## Running the notebook

1. Use **Python 3.10+** with Jupyter Notebook or JupyterLab.
2. Place `L2C90.ipynb` and `D.txt` in the same folder.
3. Open the notebook and **Run All**. Saved outputs can also be read without executing it.

By default, `RUN_FULL_ENUMERATION = True` recomputes all classes using exact integer arithmetic, writes `results/D_recomputed.txt` and checks it against `D.txt`. To validate the supplied catalogue and rerun only the screening, set `RUN_FULL_ENUMERATION = False`. No additional Python libraries are required for the mathematical computations.

The `results/` folder is generated during a full run and need not be included in the repository.
