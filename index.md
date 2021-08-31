# Welcome to Combinatorial Testing Competition (tentative - draft)

## Call for Participation — Procedure

The competition compares state-of-the-art tools for generating combinatorial test suites with respect to the generation time and test suite size.  
The competition consists of two phases: 
- a **training phase**, in which example benchmarks are given to the tool developers, (strarting from OCt 2021 ?)
- and an **evaluation** phase, in which all participating CT tools will be executed on benchmark test tasks, and their performances are measured. The competition is performed (some days before?) and presented during the IWCT workshop.

### Tools evaluation

Each tool will be evaluated by considering: 

- Test suite size (50% of the final score)
- Test suite generation time (50% of the final score)
- Test suite completeness and validity (required)

Note that the test suite validity and completeness will be mandatory for the evaluation of the tool: a tool producing an invalid or a non complete test suite will be excluded from the competition. (or only the test suite which is invalid or incomplete?)

### Catergories
Different generators can compete in different categories, and the participants may choose the category in which the tool competes. We identify the following categories:
- Models containing only boolean parameters
- Models containing enumerative parameters
- Models containing integer parameters
- Models containing relational operators in the constraints (with or without arithmetical operations)

### Input and output formats

The benchmark models will be distributed in the CTWedge format (and others?). The tools must produce as output a file with the following format (TODO)

### Tool execution

Generators will be executed on the same Linux machine (complete spec) and the results (size, generation time, completeness and validity) will be gathered through the generation of test suites from 50 test models for each category, randomly generated (todo: some distribution to be discussed about size ...).

The test model will be processed with a maximum execution time of 120 seconds each. 
The tools will be ranked
For the size, in a decreasing order
For the time, in an increasing order
Supposing that there will be n tools competing, the first tool in the rank will receive n points, the second n-1, and so on.

Having fixed the *timeout*, some tools may non complete the computation of the test suite for certain models. In this case the size and the time (for the ranking) will be considered as follows: if a tool X does not complete the benchmark Y, the greatest time required by the other tools for Y and the greatest size for Y will be assigned to X.



## Publication and Presentation of the Competition Candidates

Participants can submit a paper presenting a new CIT generator tool or an already existing one. 
If a new tool (or an extension) is presented, the authors should present a paper describing the tool and the performance obtained with the models given as example by the competition organizers (max. 8 pages including references).
If an already existing tool is presented, the authors should present a paper introducing the tool and the performance obtained with the models given as example by the competition organizers (max. 2 pages including references).

## Important Dates
- mid October 2021, release of the beanchmarks for training 
- beginning of January 2022, submission of the papers and tools (with the results over the benchmarks)
- April 2022, competition with new benchamrks and comparison among all the accepted tools

