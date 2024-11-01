Any given [[Languages|language]] is regular iff there is a [[Finite Automata]] which can recognise/accept it. But not all languages are regular.
Regular operations of languages are:
- Union $A\cup B$
- Concatenation $A\textopenbullet B=\{xy|x\in A, y\in B\}$
- Kleene Star $A^*=\{x_1x_2,...,x_k|k\geq0,x_i\in A\}$ and $\epsilon$ is always in the set
- $A\cap B$
- $A^c=\Sigma^*\backslash A$
- $A\backslash B=A\cap B^c$
- Reversal of $A$
- Regular languages are also closed under Boolean combinations

Examples of the set
$A = \{aa, abba\}$  
$B = \{a, ba, bba, bbba\}$  
$A \cup B = \{a, aa, abba, ba, bba, bbba\}$  
$A \circ B = \{aaa, abbaa, aaba, abbaba, aabba, abbabba, \dots\}$  
$A^* = \{\epsilon, aa, abba, aaaa, aaabba, abbaaa, abbaabba, aaaaaa, aaaaabba, aaabbaaa, aabbabba, \dots\}$
We note that there exists closure of the regular languages where all set operations are still regular
This can be proved with nondeterminism, through a non-deterministic finite automata [[NFA]]