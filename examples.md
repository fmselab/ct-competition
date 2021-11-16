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

[Relation]
-- this section is optional
-- general format Rx : (p1, p2, ..., pk, Strength)

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
### Csv output example ###
```
p1,p2,p3,p4,p5
v1,v1,v2,true,true
v1,v2,v1,false,false
v2,v1,v1,false,false
v2,v2,v2,false,false
v1,v2,v2,true,false
v1,v1,v1,false,true
```
## CTWedge grammar  ##
