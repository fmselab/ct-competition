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

<!---
The competition score has been given considering in an equal way the generation time and the test suite size. However, for completeness, we here report in a separate way the score given either only considering the time or the test suite size, by distinguishing between different strengths.

![Time score](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/Time.jpg)
![Size score](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/Size.jpg)

## OVERALL ranking ##

This section reports the overall ranking, considering the aggregated score of each category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/OVERALL_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/OVERALL_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/OVERALL_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/OVERALL_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/OVERALL_5.csv))

1. **CAgen** (1795.5 pts)
2. **APPTS** (1384 pts)
3. **IPO Solver** (967.5 pts)
4. **pMEDICI** (566 pts)

For completeness, we here report the score given for each strength.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/Overall.png)

## UNIFORM_BOOLEAN ranking ##

This section reports the ranking for the UNIFORM_BOOLEAN category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_BOOLEAN_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_BOOLEAN_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_BOOLEAN_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_BOOLEAN_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_BOOLEAN_5.csv))

1. **CAgen** (614.5 pts)
2. **IPO Solver** (468.5 pts)
3. **APPTS** (452.5 pts)
4. **pMEDICI** (274.5 pts)

For completeness, we here report the score given for each strength for this category.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/UNIFORM_BOOLEAN.png)

## UNIFORM_ALL ranking ##

This section reports the ranking for the UNIFORM_ALL category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_ALL_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_ALL_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_ALL_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_ALL_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/UNIFORM_ALL_5.csv))

1. **CAgen** (482 pts)
2. **APPTS** (326 pts)
3. **IPO Solver** (319 pts)
4. **pMEDICI** (148.5 pts)

For completeness, we here report the score given for each strength for this category.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/UNIFORM_ALL.png)

## MCA ranking ##

This section reports the ranking for the MCA category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCA_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCA_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCA_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCA_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCA_5.csv))

1. **CAgen** (423.5 pts)
2. **APPTS** (298 pts)
3. **IPO Solver** (273 pts)
4. **pMEDICI** (107.5 pts)

For completeness, we here report the score given for each strength for this category.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/MCA.png)

## BOOLC ranking ##

This section reports the ranking for the BOOLC category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/BOOLC_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/BOOLC_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/BOOLC_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/BOOLC_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/BOOLC_5.csv))

1. **CAgen** (280.5 pts)
2. **APPTS** (216.5 pts)
4. **pMEDICI** (40 pts)

For completeness, we here report the score given for each strength for this category.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/BOOLC.png)

## MCAC ranking ##

This section reports the ranking for the MCAC category. The detailed data can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCAC_allStrengths.csv) for all the strenghts (or, if interested in a specific strength, you can look at the specific file - [2](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCAC_2.csv), [3](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCAC_3.csv), [4](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCAC_4.csv), [5](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/MCAC_5.csv))

1. **CAgen** (140 pts)
2. **APPTS** (192 pts)
4. **pMEDICI** (62 pts)

For completeness, we here report the score given for each strength for this category.

![](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/MCAC.png)

## NUMC ranking ##

None of the participants was able to deal with NUMC instances.

## INDUSTRIAL ranking ##

## FM ranking ##

## CNF ranking ##

## HIGHLY_CONSTRAINED ranking ##

-->