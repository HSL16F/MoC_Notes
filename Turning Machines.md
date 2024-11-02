Formally defined as a 7 tuple.
$(Q, \Sigma, \Gamma, \delta, q_0, q_{accept}, q_{rej})$
$\Sigma$ input alphabet
$\Gamma$ is tape alphabet, $\Sigma\subseteq\Gamma$, includes blank _ character
$q_0$ initial state, $q_{accept}$ accept state, $q_{rej})$ reject state
$\delta: Q\times\Gamma\rightarrow Q\times\Gamma\times\{L,R\}$
$\delta(q,a)=(r,b,R)$
For current state $q$, current symbol under tape is $a$, change state to $r$, overwrite $a$ with $b$ and move cell in $R$ direction (right, In this specific example), though can be $L$ as well

Informally TM is defined as:
- Head can read/write tape
- Head is two way, can move left/right
- Tape is infinite
- Infinite many _  following end of input
- Can accept or reject at any time

Graphical representation for a TM
![[Pasted image 20241102120327.png]]
TM to recognise $\{w|w$ contains substring 11$\}$
![[Pasted image 20241102120405.png]]

## Recogniser and deciders
![[Pasted image 20241102120545.png]]
A is Turning Recognisable if for $A=L(M)$ where $L$ is a function, for some TM
For given $TM$  $M$, is a decider if $M$ halts on ALL inputs
$A$ is turning-decidable if $A=L(M)$ for some $TM$ decider $M$

A turning enumerator is a deterministic TM with a printer, start at blank tape and print strings $w_1,w_2,...$ up to possibly forever. Language is set of all strings it prints, it is a GENERATOR NOT a recogniser. For enumerator, we define as $L(E)=\{w|E \text{ prints } w\}$
If $A$ is turning-recognisable iff $A=L(E)$ for some turning-enumerator $E$
This is to show the equivalence of variants of TMS
T-Decidable $\not\implies$ T-recognisable, but T-recognisable$\implies$T-decidable

By the Church-Turning Thesis:
Choice of model is irrelevant, anything, all reasonable models are equivalent. TM chosen for one standard method.

Can accept multi tape designs
![[Pasted image 20241102124419.png]]

In general, English is used to describe many TM's, for example $M=$ on input $w$ English description of algorithm
$\langle\cdot\rangle$ is used to describe some encoding, encodes it into a string for the Machine to read, everything from a graph, to polynomials, to an automaton etc. All discrete objects have a string representation

DFA's and even empty DFA's are decidable, see [[Week 10]], lec 2, pg 10-13 for more info.