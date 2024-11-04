Reducing the scope of problems for a TM
For Recogniser/Decider's $M_1, M_2$ and $L_1, L_2$
Build $M_1$ via reduction:
![[Pasted image 20241102131910.png]]
```python
def M1(x):
	return M2(f(x))
```
For $EQ_{DFA}=\{\langle A, B\rangle |A \text{ and } B \text{ are DFAs and } L(A)=L(B)\}, EQ_{DFA}$ is decidable
$D_{EQ-DFA} =$ “On input $A$, $B$ (IDEA: Make DFA $C$ that accepts $w$ where $A$ and $B$ disagree.)
1. Construct DFA $C$ where $L(C) = (L(A) \cap \overline{L(B)}) \cup (\overline{L(A)} \cap L(B))$.
2. Run $D_{E-DFA}$ on $\langle C \rangle$.
3. Accept if $D_{E-DFA}$ accepts. Reject if $D_{E-DFA}$ rejects.”

#### Acceptance of CFG
Let $A_{CFG}=\{\langle G, w\rangle | G \text{ is a } CFG, w\in L(G)\}, A_{CFG}$ is decidable, we find that all CFL's are decidable.
Chomsky Normal Form or CNF allows:
$S\rightarrow\epsilon$
$A\rightarrow BC$
$B \rightarrow b$
![[Pasted image 20241102132828.png]]
$A_{TM}$ is Turing-recognisable BUT is it undecidable, see slides 7

Recognisable $L$: halt when $w$ is in $L$ but not when $w$ is not in $L$
Decidable $L$: halt either way
Can be thought of as unbounded vs bounded search spaces
For example:$A_{CFG}$(Search all possible derivatives vs search all derivatives of CNF of length $2|w|-1$)
![[Pasted image 20241102133919.png]]
VERY IMPORTANT:
![[Pasted image 20241102133933.png]]
Compliment $\not=$ the contrapositive
We find that also $HALT_{TM}=\{\langle M, w\rangle|M \text{ halts on input } w\}$ is undecidable
This explores the halting problem.
	