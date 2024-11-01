A DFA is formally defined as a 5 tuple,
$(Q, \Sigma, \delta, q_0, F)$, with
- $Q$ finite set of states
- $\Sigma$ finite alphabet
- $\delta:Q\times\Sigma\rightarrow Q$ transition function
- $q_0\in Q$ start state
- $F\subseteq Q$ accept states
The transition function $\delta$ must be defined for all possible inputs, empty strings are denotes by $\epsilon$ and $\Sigma^*$ is the set of all strings over the alphabet $\Sigma$, $\Sigma$ is a non-empty finite set, note that $\emptyset$ is empty, whilst $\epsilon$ is the empty string, $\emptyset\neq\epsilon$ 
Examples of valid [[Languages]] for alphabet $\Sigma=\{0,1\}$
	$\emptyset$
	$\{\epsilon\}$
	$\{\epsilon, 0, 1\}$
	$\{00, 01, 10, 11\}$
	$\{\epsilon, 0, 00, 000, \dots\}$
	$\{\epsilon, 0, 1, 00, 11, 000, 111, \dots\}$
	$\{\epsilon, 01, 0011, 000111, \dots\}$
	$\{w \in \Sigma^* \mid w \text{ contains an odd number of } 0\}$
	$\{w \in \Sigma^* \mid \text{the length of } w \text{ is a multiple of } 3\}$
	$\{w \in \Sigma^* \mid w \text{ is not the empty string}\}$
	$\{w \in \Sigma^* \mid w \text{ does not contain } 001\}$
	$\Sigma^*$
For an automaton to accept a given string, for $M=(Q, \Sigma, \delta, q_0, F)$, $w=v_1v_2...v_i\in\Sigma$, we define $M$ as accepting $w$ is there is some sequence of states $r_0,r_1,...,r_n$ where $r_i\in Q$ given that
1. $r_0=q_0$
2. $\delta(r_i,v_{i+1}=r_{i+1})$ for $i=0,...,n-1$
3. $r_n\in F$
Given these conditions are met, then for $A$ is set of all strings accepted by Machine $M$, then $A$ is language of $M$, that is $L(M)=A$

DFA's can be minimised (Not examinable)
See pg 14-16
#### Example of states:
![[Pasted image 20241030225210.png]]
