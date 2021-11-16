## Examples  ##

### CTWEDGE input example ###
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

### csv output example ###
