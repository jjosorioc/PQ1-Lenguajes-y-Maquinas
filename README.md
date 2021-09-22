# PQ1 Lenguajes y Maquinas

ISIS-1106 Lenguajes y Máquinas (Inglés)
Practical Quiz


We can specify Petri net with the language defined below.

- A Petri net specification begins with keyword PN followed by an identifier and end with the
keyword NP.
- Between PN name and NP we have the following:
  - A list of places: The keyword PLACES followed place specifications separated by
commas. A place specification is an identifier followed by its capacity within parenthesis.
The capacity is a number.
  - A list of transitions: The keyword TRANSITIONS followed by transition specifications
separated by semicolons. A transition specification is an identifier followed by the
inputs and the outputs separated by a comma and within parenthesis,
    - Both the inputs and the outputs are sets of place names: sequences of zero or
more places separated by commas withing {}’s.


Terminals: PN, NP, PLACES, TRANSITIONS, “,”, “;”, “(“, “)”,, “{“, “}”, ids.
An identifier is a sequence of alphanumeric characters that begin with a letter.
A number is a sequence of digits:


This is an example:
*PN myNet
Places Waiting (100) , Ready (1), Working(1)
Transitions Arrive({},{Waiting}); Start({Waiting, Ready},{});
Finish({Working},{Ready})
NP*


# TASK:
Define the grammar for Petri net specifications; implement a JavaCC yes/no parser; and integrate it to
the attached parserTester project. You must verify that the sets in transition specifications are in fact
place names defined previously.
