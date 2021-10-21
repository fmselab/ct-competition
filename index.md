## Objective

The area of Combinatorial Interaction testing has seen tremendous progress over the last years. Many tools have been developed but a comparison among algorithms and techniques is difficult to carry on. 
With this competition, we want to motivate implementors to present their work to a broader audience and to compare it with that of others.


## Call for Participation — Procedure

The competition compares state-of-the-art tools for generating combinatorial test suites with respect to the generation time and test suite size.  
The competition consists of two phases: 
- a **training phase**, in which example benchmarks are given to the tool developers (strarting from mid Nov 2021)
- and an **evaluation** phase, in which all participating CT tools will be executed on benchmark test tasks, and their performances are measured. The competition is performed (some days before the workshop) and presented during the IWCT workshop.

Researchers from both academia and industry are invited to submit their tools.
*In order to easily include in the competition both open source and commercial tools, participants have to submit only the executable and no submission of the source code is required.*

### Tools evaluation

Each tool will be evaluated by considering: 

- Test suite size (50% of the final score)
- Test suite generation time (50% of the final score)
- Test suite completeness and validity (required)

Note that the test suite validity and completeness will be mandatory for the evaluation of the tool: an invalid or non complete test suite produced for a model will be marked as not correct and its score will be considered null.

### Benchmarks characteristics

*Benchmarks* used for tool comparison will be **randomly** generated, both in terms of parameters, domains and constraints.
However, the random generation will be guided by setting the number of variables (included between a lower and an upper limit) and their types, and the number (included between a lower and an upper limit) and charateristics of constraints (like depth of logical operators, type of operators, ...). 

### Categories/Tracks

Different generators can compete in different categories, and the participants may choose the category in which the tool competes (depending on the capabilities of the tool). We identify the following categories:
- Models containing only boolean parameters
- Models containing enumerative parameters
- Models containing integer parameters
- Models containing relational operators in the constraints (with or without arithmetical operations)

### Input and output formats

The benchmark models will be distributed in the CTWedge and ACTS formats. The tools must produce as output a file in **csv** format.

### Tool execution

Generators will be executed, inside a *docker* provided by the competition organizers, on the same Linux machine with the following specs:
- 2 CPUs Intel(R) Xeon(R) E5-2620 v4 @ 2,10 GHz
- RAM DDR4, 2400 MHz, 4x32 Gb
- 2xSSD Samsung 850 (256GB each) in RAID1
- OS: Ubuntu 18.04.6 LTS

The results (size, generation time, completeness and validity) will be gathered through the generation of test suites from 50 test models for each category, randomly generated (TODO: some distribution to be discussed about size ...).

All the tools must be **compiled for Linux** and be invoked as in the following:
```
toolExecutable n-wise modelFileName
```

The test model will be processed with a maximum execution time of 120 seconds each. 
The tools will be ranked
- For the total size of the test suites, in a decreasing order
- For the total time, in an increasing order
Supposing that there will be n tools competing, the first tool in the rank will receive n points, the second n-1, and so on.

Having fixed the *timeout*, some tools may non complete the computation of the test suite for certain models. In this case the size and the time (for the ranking) will be considered as follows: if a tool X does not complete the benchmark Y, the greatest time required by the other tools for Y and the greatest size for Y will be assigned to X.

## Publication and Presentation of the Competition Candidates

Participants can submit a paper presenting a new CIT generator tool or an already existing one. 
If a new tool (or an extension) is presented, the authors should present a paper describing the tool and the performance obtained with the models given as example by the competition organizers (as full or short paper).
If an already existing tool is presented, the authors should present a paper introducing the tool and the performance obtained with the models given as example by the competition organizers (short paper).

## Important Dates
- Mid November 2021, release of the benchmarks for training 
- Beginning of January 2022, submission of the papers and tools (with the results over the benchmarks)
- April 2022, competition with new benchmarks and comparison among all the accepted tools

### Organization
- ....

### Sponsors/prize


