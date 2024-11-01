CFL's are generated by [[Context Free Grammars]], CFL's are accepted by [[Pushdown Automata]]
A language is context free iff it is generated by some Context Free Grammar
### Closure CFL's:
- Union
- Concatenation
- Kleene star
- Reversal
### NOT Closed under:
Intersection

For the following CFL's:
$C=\{a^mb^nc^n|m,n\geq0\}, D=\{a^nb^mc^m|m,n\geq0\}, C\cap D$ is not context free
To prove that the intersection is not context free, use the [[Pumping lemma]] for context CFL's

### Examples
When operating with grammars, they can be used to express numeric expressions. For example
![[Pasted image 20241012135033.png]]
![[Pasted image 20241012135041.png]]
![[Pasted image 20241012135054.png]]
For example with the grammar:
$E\rightarrow E+E|E*E|(E)|0|1|...|9$
![[Pasted image 20241012135143.png]]