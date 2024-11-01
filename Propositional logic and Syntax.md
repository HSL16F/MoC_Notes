Connectives
Let A be 1, B be 0
- ¬: no ¬A:0
- ∧: and A∧B:0, ¬A∧B:1 (Sometimes noted as &&)
- ∨: or A∧B:0
- ⇒: implies A⇒B:0 (Also written as ->), A⇒¬B: 1
- ⇔: equivalent (if and only if) (Also written as <->) A<->¬B: 1, ¬A<->B: 0
Various propositional letters and connectives
A, B, C,..., Z act as propositions.
Connectives connect and (, ) acts as bounds and clarification
### Well-formed formula
WFF are generated from set of syntax and grammar
a well formed proof is defined by
wff:=A|B|C|...|Z| ¬wff | (wff∧wff) | (wff∨wff) | (wff -> wff) | (wff<-> wff) |
wff say Q is a wff then ¬Q is also a wff, but as ¬Q is a wff, lets say S, then ¬S is also a wff, which is ¬¬Q and so on, it is still comprised of the valid grammar.
Pay careful attention to the braces "(",  ")"

Some examples of well formed formula:
$P$
$(P\rightarrow Q)$
$(P\vee  ¬Q$
$¬(P\wedge ¬P)$
$(P \iff ¬P)$
$(((P\rightarrow Q)\rightarrow P)\rightarrow P)$

Notable symbols include:
¬ Not


There are also informal rules, these include:
Dropping outermost parentheses
Drop inner parentheses in nested Or/AND, for example P&&Q&&R is logequiv to ((P&&Q))&&R) and (P&&Q(&&R)) but parenthesis is required for P&&QVR, unclear if (P&&Q)VR or P&&(QVR)

Truth table used to represent operations. Connectives are truth-functional example
![[Pasted image 20240810232421.png]]
Truth's can be assigned, for example
v = {P|->1, Q|->0}
Therefore, for v(P)=1, but v(Q)=v(R)=...v(Z)=0, anything but P maps to 0
There also exists the shorthand notation of ⊨ (`|=`), that is when for some function v and some sentence on the right represented as φ, for v|=φ, that is v double turnstile, phi, then phi is true under v, read as entails, models or semantic consequence, when every set of v sentences is true, then phi is true

Logically equivalent occurs iff and only iff they have equal true values UNDER EVERY truth assignment

Noting the use if the implies -> symbol, causality is not required for the conditioning
![[Pasted image 20240810234348.png]]

Modus Ponens is for when a rule is sound if every model of the premises is a model of the conclusion


  $\vDash$ is the model satisfies or is a model of, for example, $\{P\mapsto1,Q\mapsto0\}\vDash P\wedge Q$, $\{P\mapsto0\}\vDash\neg P$
Tautology is always true, Contradiction is always false
Tautologies are valid, but non-valid is *sometimes* false
Contradictions are unsatisfiable, that is never true whilst satisfiable is sometimes true.
Most statements are contingent. Substitution preserves validity and preserves logical equivalence.
![[Pasted image 20241022224847.png]]
![[Pasted image 20241022224853.png]]
![[Pasted image 20241022224900.png]]


## Review
Implies, modus ponens and double turnstile