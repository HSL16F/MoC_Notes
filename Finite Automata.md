Different classes of machines and languages
![[Pasted image 20241030223000.png]]
Where we have various layers, from simple [[DFA]] to [[Turning Machines]]
We also note that they accept various different [[Languages]], from [[Regular Languages]] to more general definitions of [[Turning Recognisable]]
State diagrams used to represent transitions of different states.

### NFA's and DFA's
Machines are equivalent iff they recognise the same language, that is for $M_1,M_2$ and language $A$, $L(M_1)=L(M_2)=A\implies M_1\equiv M_2$
We note that every [[NFA]] has an equivalent [[DFA]] and we can simulate both

#### Converting NFA to DFA
The subset construction allow the conversion of an NFA to DFA. DFA->NDA is trivial.
Let $N = (Q, \Sigma, \delta, q_0, F)$ be an NFA.
For all $R \subseteq Q$, let $E(R)$ be the $\epsilon$-closure of $R$. That is, 
$E(R) = \{ q \in Q \mid q \text{ is reachable from some } r \in R \text{ by following 0 or more } \epsilon \text{ transitions} \}.$
Let $M = (Q', \Sigma, \delta', q'_0, F')$ be a DFA such that  
- $Q' = P(Q)$,  
- $q'_0 = E(\{q_0\})$,  
- $F' = \{ R \in Q' \mid R \text{ contains an accept state of } N \}$.  

For the transition function $\delta'$ in $M$, we define:  
$$
\delta'(R, a) = \bigcup_{r \in R} E(\delta(r, a)).
$$
Note that accept states are denoted with a star
For NFA:
![[Pasted image 20241031140339.png]]
Converted DFA:
![[Pasted image 20241031140406.png]]


### Examples
Examples of state machines:
![[Pasted image 20241030223734.png]]
