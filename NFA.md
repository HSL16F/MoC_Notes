Formally defined by 
$(Q, \Sigma, \delta, q_0, F)$, with
- $Q$ finite set of states
- $\Sigma$ finite alphabet
- $\delta:Q\times\Sigma_\epsilon\rightarrow \mathcal{P}(Q)$ transition function
- $q_0\in Q$ start state
- $F\subseteq Q$ accept states
Where $\Sigma_\epsilon$ is $\Sigma\cup\{\epsilon\}$
The acceptance of languages and strings operates the same with the caveat of $w=v_1v_2,...v_n$ where $v_i\in\Sigma_\epsilon$

#### Closure of [[Regular Languages]]
##### Union
![[Pasted image 20241031141927.png]]
##### Concatenation
![[Pasted image 20241031141942.png]]

##### Kleene Star
![[Pasted image 20241031142005.png]]
#### Examples
An example of an NFA is for
$A=\{w|w\in\{0,1\}^*$ has length of $3$ or more, and third lasts symbol of $w$ is $1\}$
![[Pasted image 20241031134921.png]]
Note that there is no further transition at $q_4$ and multiple transitions is permitted for state $q_1$
An equivalent [[DFA]] would be:
![[Pasted image 20241031135016.png]]
A critical application of NFA's is the $\epsilon$ transition, which allows for the easy construction of two languages.
