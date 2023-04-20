# Second edition of the CT Competition  ##

In this page you can find the information and the results obtained by each participant to the second edition of the CT competition.

### Participants ###

- **ACTS**: Java Implementation of IPO, one of the most used combinatorial test generation tools. Executed with default settings (IPOG with MFT);
- **CAgen**: a multithreaded FIPOG implementation written in Rust;
- **CAopt**: a sampling and an optimization phase, based on a SAT solver;
- **KALI**: a java multi-thread tool exploiting SMT solvers;
- **MEDICI**: a C++ tool for combinatorial test generation based on the use of Multi-Valued Decision Diagrams;
- **pMEDICI**: a java multi-thread implementation of the MEDICI tool, based on Multi-valued Decision Diagrams;

### Benchmarks and execution rules ###

For this edition of the CT competition:
- 240 [benchmark models](https://github.com/fmselab/CIT_Benchmark_Generator/tree/main/Benchmarks_CITCompetition_2023) have been generated
- Strengths from 2 to 6 have been used
- Each benchmark has been executed 3 times for each tool and strength (you can find the list of all the execution results [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/output.csv)), and the best run has been selected for the attribution of the score (see [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/output_best.csv) for the best executions list)

# Results #

All the results reported into this section derives from the [list of best executions](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/output_best.csv).

The file containing all the CAs which have been analyzed for giving the score to each tool can be found [here](#TODO).

## Validity and timeouts ##

All the tools have reported at least one timeout or produced an invalid test suite (even if not in all the categories and all strenghts).
The list of timed out instances for each category and each strength can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/TimedoutInstances.csv), while the one of invalid instances can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/InvalidInstances.csv).

## Score - Time and Size ##


The competition score has been given considering in an equal way the generation time and the test suite size. However, for completeness, we here report in a separate way the score given either only considering the time or the test suite size, by distinguishing between different strengths.

### Time

![Time score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/OVERALL_PerStrength_Time.png)

### Size

![Size score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/OVERALL_PerStrength_Size.png)

## OVERALL ranking ##

This section reports the overall ranking, considering the aggregated score of each category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/OVERALL_6.csv))


1. **CAgen** (3666.0 pts)
2. **ACTS** (3056.5 pts)
3. **CAopt** (2104.0 pts)
4. **MEDICI** (1997.0 pts)
5. **pMEDICI** (1560.5 pts)
6. **KALI** (537.0 pts)

For completeness, we here report the graph with the score given for each strength.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/OVERALL_PerStrength_Overall.png)

## UNIFORM_BOOLEAN ranking ##

This section reports the ranking for the UNIFORM_BOOLEAN category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_BOOLEAN_6.csv))

1. **CAgen** (410.5 pts)
2. **ACTS** (363.0 pts)
3. **CAopt** (324.5 pts)
4. **MEDICI** (280.0 pts)
5. **KALI** (223.5 pts)
6. **pMEDICI** (222.0 pts)

For completeness, we here report the graph showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/UNIFORM_BOOLEAN_PerStrength_Overall.png)

## UNIFORM_ALL ranking ##

This section reports the ranking for the UNIFORM_ALL category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/UNIFORM_ALL_6.csv)

1. **CAgen** (289.5 pts)
2. **ACTS** (235.5 pts)
3. **CAopt** (141.5 pts)
4. **pMEDICI** (131.0 pts)
5. **MEDICI** (126.0 pts)
6. **KALI** (104.5 pts)

For completeness, we here report the graph showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/UNIFORM_ALL_PerStrength_Overall.png)

## MCA ranking ##

This section reports the ranking for the MCA category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCA_6.csv))

1. **CAgen** (591.5 pts)
2. **ACTS** (468.0 pts)
3. **pMEDICI** (232.0 pts)
4. **CAopt** (211.0 pts)
5. **MEDICI** (172.0 pts)
6. **KALI** (157.5 pts)

For completeness, we here report the plot showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/MCA_PerStrength_Overall.png)

## BOOLC ranking ##

This section reports the ranking for the BOOLC category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/BOOLC_6.csv))

1. **CAgen** (741.5 pts)
2. **ACTS** (627.5 pts)
3. **MEDICI** (600.5 pts)
4. **pMEDICI** (431.5 pts)
5. **CAopt** (380.0 pts)
6. **KALI** (61.5 pts)

For completeness, we here report the plot showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/BOOLC_PerStrength_Overall.png)

## MCAC ranking ##

This section reports the ranking for the MCAC category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/MCAC_6.csv))

1. **CAgen** (286.5 pts)
2. **ACTS** (263.0 pts)
3. **MEDICI** (178.5 pts)
4. **CAopt** (172.0 pts)
5. **pMEDICI** (100.0 pts)
6. **KALI** (9.5 pts)

For completeness, we here report the plot showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/MCAC_PerStrength_Overall.png)

## NUMC ranking ##

This section reports the ranking for the NUMC category. The detailed data can be found [here](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_2.csv), [3](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_3.csv), [4](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_4.csv), [5](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_5.csv), [6](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/data/NUMC_6.csv)).

In this case, only CAGen, ACTS, CAopt and KALI have been considered, since the other tools declared not to able to support the constraints available in the NUMC category.

1. **CAgen** (272.0 pts)
2. **ACTS** (216.0 pts)
3. **CAopt** (131.0 pts)
4. **KALI** (0.0 pts)

For completeness, we here report the plot showing the score given for each strength for this category.

![Overall score](https://github.com/fmselab/ct-competition/raw/gh-pages/results/2023/figs/NUMC_PerStrength_Overall.png)

<!---
None of the participants was able to deal with NUMC instances.

## INDUSTRIAL ranking ##

## FM ranking ##

## CNF ranking ##

## HIGHLY_CONSTRAINED ranking ##

-->