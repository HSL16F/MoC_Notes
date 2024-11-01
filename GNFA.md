[[Notes in Sipser's lectures]]
A GNFA is a NFA in which the transitions are represented with [[Regular expression]] 
Defined by:
$(S, \Sigma, T, s, a)$, consisting of
- a finite set of states $(S)$;
- a finite set called the alphabet $(\Sigma)$;
- a transition function $(T : (S \setminus \{a\}) \times (S \setminus \{s\}) \to R)$;
- a start state $(s \in S)$;
- an accept state $(a \in S)$.
