## Examples  ##

In this page you can find examples of the input and output formats that have to be supported by the tools wanting to compete in the CT competition.

### CTWedge input example ###

A detailed description of the CTWedge input format can be found here:

[CTWedge wiki grammar](https://github.com/fmselab/ctwedge/wiki/Grammar)

An example follows.
```
Model Concurrency

Parameters:
p1: { v1 v2 };
p2: { v1 v2 };
p3: { v1 v2 };
p4: Boolean;
p5: Boolean;

Constraints:
	# ( p3!=v1 OR p2!=v1 OR p5 OR p4 OR p1!=v1) #
	# ( p1!=v2 OR p5!=true) #
	# ( p2!=v1 OR p5 OR p4!=true OR p3!=v2 OR p1!=v1) #
	# ( p5!=true OR p2!=v2) #
	# ( p4 OR p3!=v2 OR p1!=v1) #
	# ( p4!=true OR p1!=v2) #
	# ( p3!=v1 OR p4!=true) #
```
### ACTS input example ###

The ACTS input format is described in [the ACTS User Guide](https://csrc.nist.gov/CSRC/media/Projects/Automated-Combinatorial-Testing-for-Software/documents/acts_user_guide_2_92.pdf). Please note that the input files generated for this competition do not use the [Relations] or [Test Set] sections; the former would only be relevant for variable strength covering arrays (VCAs), while the latter would only be useful for extending existing test sets.

```
[System]
-- specify system name
Name: Concurrency

[Parameter]
-- general syntax is parameter_name : value1, value2, ...
p1 (enum) : v1, v2
p2 (enum) : v1, v2
p3 (enum) : v1, v2
p4 (boolean) : true, false
p5 (boolean) : true, false

[Constraint]
-- this section is also optional
(((((p3)!=("v1"))||((p2)!=("v1")))||(p5))||(p4))||((p1)!=("v1"))
((p1)!=("v2"))||((p5)!=(true))
(((((p2)!=("v1"))||(p5))||((p4)!=(true)))||((p3)!=("v2")))||((p1)!=("v1"))
((p5)!=(true))||((p2)!=("v2"))
((p4)||((p3)!=("v2")))||((p1)!=("v1"))
((p4)!=(true))||((p1)!=("v2"))
((p3)!=("v1"))||((p4)!=(true))
```
### CSV output example ###

We expect a CSV file with a header; in other words, the first line should contain the names of the parameters.
Failure to include the header line will result in the first line not being counted towards coverage.

Do not surround values with quotes or use any separators besides commas. Your CSV file should only contain the literal parameter names and values provided in the input file, commas to separate them (we will never use commas in parameter names or values), and newlines to separate rows (it is irrelevant whether these are Windows or UNIX line separators).

```
p1,p2,p3,p4,p5
v1,v1,v2,true,true
v1,v2,v1,false,false
v2,v1,v1,false,false
v2,v2,v2,false,false
v1,v2,v2,true,false
v1,v1,v1,false,true
```
