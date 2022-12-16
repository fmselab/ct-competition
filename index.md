## Objective

The area of Combinatorial Interaction testing has seen tremendous progress over the last years. Many tools have been developed but a comparison among algorithms and techniques is difficult to carry on.
With this competition, we want to motivate implementors to present their work to a broader audience and to compare it with that of others.

## Call for Participation — Procedure

The competition compares state-of-the-art tools for generating combinatorial test suites with respect to the generation time and test suite size.  
The competition consists of two phases:
- a **training phase**, in which example benchmarks are given to the tool developers (starting from end-Dec 2022)
  - the example benchmarks can be found here: [ACTS](https://github.com/fmselab/ct-competition/raw/gh-pages/examples/ACTS2023.zip) or [CTWedge](https://github.com/fmselab/ct-competition/raw/gh-pages/examples/CTWedge2023.zip). 
- and an **evaluation** phase, in which all participating CT tools will be executed on benchmark test tasks, and their performances are measured. The competition is performed (some days before the workshop) and presented during the IWCT workshop.

Researchers from both academia and industry are invited to submit their tools.
*In order to easily include in the competition both open source and commercial tools, participants have to submit only the executable and no submission of the source code is required.*

### Benchmarks characteristics

*Benchmarks* used for tool comparison will be **randomly** generated, both in terms of parameters, domains and constraints, or taken from well known test sets.
However, the random generation will be guided by setting the number of variables (included between a lower and an upper limit) and their types, and the number (included between a lower and an upper limit) and characteristics of constraints (like depth of logical operators, type of operators, ...).

The code of the benchmark generator is available [here](https://github.com/fmselab/CIT_Benchmark_Generator), together with benchmarks used during the previous editions of the competition.

### Categories/Tracks

Different generators can compete in different categories, and the participants may choose the category in which the tool competes (depending on the capabilities of the tool). We identify the following categories:

- Models with no constraints
  - With only boolean parameters (`UNIFORM_BOOLEAN`)
  - MCA
  - Uniform with n > 2 (`UNIFORM_ALL`)
- Models containing constraints
  - With boolean parameters and logical operators in constraints (`BOOLC`)
  - With also enumerative parameters (MCA), and logical and equal operators in constraints (`MCAC`)
  - With also integer parameters, and logical, mathematical, and relational operators in constraints (`NUMC`)
  - Models deriving from feature models translation (`FM`)
  - Models deriving from industrial case studies (`INDUSTRIAL`)
  - Highly constrained models, with validity ratio < 1% (`HIGHLY_CONSTRAINED`)
  - Models with constraints in CNF (`CNF`)

During tools evaluation, test models will be distributed as in the following table:

| **Category Name** | **Parameters** | **Constraints** | **Control variables** | **Boundaries** | **# Tests** |
|:---|:---|:---|:---|:---|:---|
| `UNIFORM` | Only booleans | NO | *k*: number of parameters | *k*: random in the interval \[2, 20\] | 25 |
| `UNIFORM` | Uniform | NO | *k*: number of parameters<br /><br /> *v*: number of elements for each parameter | *k*: random in the interval \[2, 20\]<br /><br /> *v*: random in the interval \[2, 20] | 25 |
| `MCA` | MCA | NO | *k*: number of parameters<br /><br /> *v\[\]*: array containing the number of elements for each parameter | *k*: random in the interval \[2, 20\]<br /><br /> each element of *v\[\]*: random in the interval \[2,20\] | 50 |
| `BOOLC` | Only booleans | randomly chosen between AND, OR, <=>, NOT, => | *k*: number of parameters<br /><br /> *c*: number of constraints<br /><br />*d\[\]*: array containing the complexity of each of the *c* constraints | *k*: random in the interval \[2, 20\]<br /><br /> *c*: random in the interval \[1, 100\]<br /><br /> each element of *d\[\]*: random in the interval \[1, 20\] | 50 |
| `MCAC` | MCA | randomly chosen between AND, OR, <=>, NOT, =>, = (both *x*=*C* and *x*=*y*, where *x* and *y* are parameters and *C* a constant of *x*), != |  *k*: number of parameters<br /><br /> *v\[\]*: array containing the number of elements for each parameter<br /><br /> *c*: number of constraints<br /><br />*d\[\]*: array containing the complexity of each of the *c* constraints | *k*: random in the interval \[2, 20\]<br /><br /> each element of *v\[\]*: random in the interval \[2,20\]<br /><br /> *c*: random in the interval \[1, 100\]<br /><br /> each element of *d\[\]*: random in the interval \[1, 20\] | 50 |
| `NUMC` | Booleans, Enumeratives and Integer ranges | randomly chosen between AND, OR, <=>, NOT, =>, = (both *x*=*C* and *x*=*y*, where *x* and *y* are parameters and *C* a constant of *x*), !=, mathematical and relational operators | *k*: number of parameters<br /><br /> *v\[\]*: array containing the number of elements for each parameter<br /><br /> *c*: number of constraints<br /><br />*d\[\]*: array containing the complexity of each of the *c* constraints | *k*: random in the interval \[2, 20\]<br /><br /> each element of *v\[\]*: random in the interval \[2,20\]<br /><br /> *c*: random in the interval \[1, 100\]<br /><br /> each element of *d\[\]*: random in the interval \[1, 20\] | 50 |
| `FM` | MCA | As required in the corresponding feature model from which the benchmark derives |  |  |
| `INDUSTRIAL` | As required by the industrial case study from which the benchmark derives  | As required by the industrial case study from which the benchmark derives |  |  |
| `HIGHLY_CONSTRAINED` | MCA | randomly chosen between AND, OR, <=>, NOT, =>, = (both *x*=*C* and *x*=*y*, where *x* and *y* are parameters and *C* a constant of *x*), != |  *k*: number of parameters<br /><br /> *v\[\]*: array containing the number of elements for each parameter<br /><br /> *c*: number of constraints<br /><br />*d\[\]*: array containing the complexity of each of the *c* constraints | *k*: random in the interval \[2, 20\]<br /><br /> each element of *v\[\]*: random in the interval \[2,20\]<br /><br /> *c*: random in the interval \[1, 100\]<br /><br /> each element of *d\[\]*: random in the interval \[1, 20\] | 50 |
| `CNF` | MCA | in CNF randomly chosen between AND, OR, NOT, = (both *x*=*C* and *x*=*y*, where *x* and *y* are parameters and *C* a constant of *x*), != |  *k*: number of parameters<br /><br /> *v\[\]*: array containing the number of elements for each parameter<br /><br /> *c*: number of constraints<br /><br />*d\[\]*: array containing the complexity of each of the *c* constraints | *k*: random in the interval \[2, 20\]<br /><br /> each element of *v\[\]*: random in the interval \[2,20\]<br /><br /> *c*: random in the interval \[1, 100\]<br /><br /> each element of *d\[\]*: random in the interval \[1, 20\] | 50 |

### Input and output formats

The benchmark models will be distributed in the CTWedge and ACTS formats. The tools must be able to process models in one of these formats (**you must specify whether your submission supports CTWedge or ACTS**) and produce its output in CSV on the standard output file descriptor (stdout). Examples of the inputs and outputs, together with the full grammar of CTWedge, can be found [here](https://fmselab.github.io/ct-competition/examples.html).

### Tool execution

Generators will be executed inside a Docker container provided by the competition organizers, on the same Linux machine with the following specs:
- 2 CPUs Intel(R) Xeon(R) E5-2620 v4 @ 2,10 GHz
- RAM DDR4, 2400 MHz, 4x32 Gb
- 2xSSD Samsung 850 (256GB each) in RAID1
- OS: Ubuntu 18.04.6 LTS

The results (size, generation time, completeness, and validity) will be gathered through the generation of test suites from 50 test models for each category, randomly generated.

Your submission will be invoked as follows:
```
toolExecutable strength modelFileName
```
For example:
```
hyperspeed_ca_generator 4 input.ctwedge
```

The test model will be processed with a maximum execution time of 300 seconds each. Note that multiple executions for the same test model (details about the number of executions will follow) will be done, and the considered result will be the one of the fastest execution.

#### Submission format and dependencies

Your submission can be in one of two formats:
* A Linux (ELF) executable
* A [docker-compose](https://docs.docker.com/compose/) file that points towards a Docker container provided by you, plus the path to your executable in this container

If you are facing issues with providing any of these formats, please contact the organizers. We are unable to set up custom environments.

If you submit an executable, you must not make any assumptions about libraries or versions thereof available in the Docker container.
This means that if your submission requires any shared libraries besides libc (e.g. boost or GMP), you should submit a statically linked version (details on this process depend on your compiler and build system).

To work around issues with more complex dependencies (such as Java), you can instead prepare a Docker container, upload it to a repository and submit a docker-compose file along with the path to the executable in the Docker container (if your docker-compose file includes multiple images, please also specify which container holds the executable). We will manually audit submitted docker-compose files.

All invocations of your executable will follow the format described above. This means that if you require additional command line flags (e.g. `java -Xmx 65500 -jar my_ca_generator.jar -Ddoi=5`), you must write a wrapper that takes the arguments described above (strength and input file) and invokes your actual executable.

Regardless of the submission format, your submission **must not** make network connections or execute malicious code.
Failure to adhere to these conditions will result in immediate disqualification and possibly legal action.

### Tools evaluation

Each tool will be evaluated by considering:

- Test suite size (50% of the final score)
- Test suite generation time (50% of the final score)
- Test suite completeness and validity (required for all the test suites)

Note that the test suite validity and completeness will be mandatory for the evaluation of how the tool performs over a benchmark model: an invalid or incomplete test suite produced for a model will be marked as not correct and its score will be considered like the tool has been unable to complete the generation of the test suite for that model.

The tools will be ranked
- For the total size of the test suites, in a decreasing order
- For the total time, in an increasing order
Supposing that there will be n tools competing, the first tool in the rank will receive n points, the second n-1, and so on.

Having fixed the *timeout* (300 seconds), some tools may not complete the computation of the test suite for certain models. In this case the size and the time (for the ranking) will be considered as follows: if a tool X does not complete the benchmark Y, the greatest time required by the other tools for Y (+1) and the greatest size for Y (+1) will be assigned to X.

For the strength, we will execute the tool with **strength t** starting from 2 to maximum *k-1* (still to be decided, probably only a subset).

If no tool is able to generate a full covering array for a given strength and model, that strength will be skipped in the evaluation for this model.

## Publication and Presentation of the Competition Candidates

Participants may submit a paper presenting their tool at [IWCT2023](https://conf.researchr.org/home/icst-2023/iwct-2023) or just send the proposed tool to one of the competition organizers. 
If a paper is submitted, it can present either a new CIT generator tool or an already existing one.
If a new tool (or an extension) is presented, the authors should present a paper describing the tool and the performance obtained with the models given as examples by the competition organizers (as full or short paper).
If an already existing tool is presented, the authors should present a paper introducing the tool and the performance obtained with the models given as examples by the competition organizers (short paper). If the paper is accepted, the organizers will contact the authors about how to provide the tool executable that will be run for the competition itself.

## Important Dates
- End-Dicember 2022, the release of the benchmarks for training
- End-January 2023, submission of the tools and, possibly, papers with the results over the benchmarks
- April 2023, competition with new benchmarks and comparison among all the competing tools

### Organization

If you want to know more, or need clarification, do not hesitate to contact us:

- For the University of Bergamo, Andrea Bombarda <andrea.bombarda@unibg.it>
- for SBA Research, Michael Wagner <MWagner@sba-research.org>

### Sponsors/prize

If you are interested to support the competition, please contact us.

## History: Other editions of the combinatorial testing competition

- The rules and general information about the first edition of the combinatorial testing competitions are published [here](https://fmselab.github.io/ct-competition/index2022.html).
- The results of the 1st edition of the CT Competition are published [here](https://fmselab.github.io/ct-competition/Competition2022.html).
