Related to [[Finite Automata]]
A compact notation to describe [[Regular Languages]]
For given alphabet $\Sigma=\{a_1,...,a_n\}$, composed of various regex groups

$L(a) = \{a\}$
$L(\epsilon) = \{\epsilon\}$
$L(\emptyset) = \emptyset$
$L(R_1 \cup R_2) = L(R_1) \cup L(R_2)$
$L(R_1 R_2) = L(R_1) \circ L(R_2)$
$L(R^*) = L(R)^*$

There is the precedence for regex, star>concatenation>union
1. $ab$ means $(a \circ b)$
2. $ab^*$ means $(a \circ (b^*))$
3. $a \cup bc^*$ means $(a \cup (b \circ (c^*)))$

![[Pasted image 20241101141118.png]]

## Steps to construct NFA from Regular Expression
[[NFA]] constructed from regex $(a\cup b)^*bc$
![[Pasted image 20241101141321.png]]
![[Pasted image 20241101141327.png]]

## Converting NFA's to Regex:
Represent generalised NFA's or [[GNFA]]
General rule is for $m$ incoming and $n$ outgoing arrows, replace with $mn$ bypassing arrows.
#### Useful laws:
$A\cup A=A$
$A \cup B = B \cup A$
$(A \cup B) \cup C = A \cup (B \cup C) = A \cup B \cup C$
$(A \circ B) \circ C = A \circ (B \circ C) = A \circ B \circ C$
$\emptyset \cup A = A \cup \emptyset = A$
$\epsilon \circ A = A \circ \epsilon = A$
$\emptyset \circ A = A \circ \emptyset = \emptyset$
$(A \cup B) \circ C = (A \circ C) \cup (B \circ C)$
$A \circ (B \cup C) = (A \circ B) \cup (A \circ C)$
$(A^*)^* = A^*$
$\emptyset^* = \epsilon^* = \epsilon$
$(\epsilon \cup A)^* = A^*$
$(A \cup B)^* = (A^* B^*)^*$
#### Example:
![[Pasted image 20241101160645.png]]
![[Pasted image 20241101160701.png]]
![[Pasted image 20241101160725.png]]
