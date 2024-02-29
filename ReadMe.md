# Snakemake Tutorial


## Snakemake Installation
```
   mamba create -c conda-forge -c bioconda -n bioinfo
   mamba install snakemake
   R
   install.packages() in the environment
   ```

## Data collection


### Making different directories
Make different directories called "Kidney", "Bladder", "Breast", etc. 

### Downloading datasets
Download the datasets from `TISCH2` and categorize them under their respective directories and put all of them in directory named "data".
 
### Add additional files

1. Make 3 directories named `data`, `scripts` and `workflow`. 

2. Place the .h5 files inside data in respective folder.

3. Place the .R scripts files inside scripts in respective folder.

4. Make Snakefile and place inside the workflow directory.


## Snakemake commands for analysis


1. **Setting the environment**
   ```
   mamba activate bioinfo
   ```
   Replace `"bioinfo"` with your environment name.

2. **Getting into the workflow directly**
   ```
   cd snakemake/workflow/
   ```
   Replace `"snakemake/workflow/"` with your directory path.

3. **Snakemake dry run**
   ```
   snakemake -n
   ```

4. **Snakemake command to run**
   
   ```
   snakemake --cores 1 -j1
   snakemake --lint
   ```
   - Note: Number of `cores` can be changed according to the file size and processing time.
   
## Creation of DAG using GraphViz

```
snakemake --dag > workflow.dag
dot -Tpdf workflow.dag > workflow.pdf
```

## Conclusion
This tutorial covers the basic usage of Snakemake. This will result in generation of different markers and vlnplots for various datasets. 
