# First edition of the CT Competition  ##

In this page you can find the information and the results obtained by each participant to the first edition of the CT competition.

### Participants ###

- **APPTS**: a tabu search-based optimization of Cas, uses ACTS for initial generation
- **CAgen**: a multithreaded optimized IPO-based tool
- **IPO Solver**: a C++ implementation of the IPO algorithm
- **pMEDICI**: a multi-thread implementation of the MEDICI tool, based on Multi-valued Decision Diagrams

### Benchmarks and execution rules ###

For this edition of the CT competition:
- 300 [benchmark models](https://github.com/fmselab/CIT_Benchmark_Generator/tree/main/Benchmarks_CITCompetition_2022) have been generated
- Strengths from 2 to 5 have been used
- Each benchmark has been executed 3 times for each tool and strength (you can find the list of all the execution results [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/output.csv)), and the best run has been selected for the attribution of the score (see [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/output_best.csv) for the best executions list)

# Results #

All the results reported into this section derives from the [list of best executions](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/output_best.csv).

## Validity and timeouts ##

All the tools have reported at least one timeout or produced an invalid test suite (even if not in all the categories and all strenghts).
The list of timed out instances for each category and each strength can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/TimedoutInstances.csv), while the one of invalid instances can be found [here](https://github.com/fmselab/CIT_Benchmark_Generator/blob/main/ToolEvaluator/data/InvalidInstances.csv).

## Score - Time and Size ##

The competition score has been given considering in an equal way the generation time and the test suite size. However, for completeness, we here report in a separate way the score given either only considering the time or the test suite size, by distinguishing between different strengths.
| **Time score** | **Size score**  |
|--|--|
|![Time score](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/Time.jpg)|![Size score](https://github.com/fmselab/ct-competition/raw/gh-pages/imgs/Size.jpg)|

## Overall ranking ##
