All regular languages are context free.
DFA and NFA are just PDA with no stack
Defined by:
![[Pasted image 20241101210703.png]]
Has memory and can therefore recognise languages which are not [[Regular Languages]] such as $L=\{a^nb^n|n\geq0\}$
It is defined by:
A pushdown automaton (PDA) is a 6-tuple $(Q, \Sigma, \Gamma, \delta, q_0, F)$ where:
- $Q$ is a finite set of states,
- $\Sigma$ is the finite input alphabet,
- $\Gamma$ is the finite stack alphabet,
- $\delta : Q \times \Sigma_\epsilon \times \Gamma_\epsilon \rightarrow P(Q \times \Gamma_\epsilon)$ is the transition function,
- $q_0 \in Q$ is the start state, and
- $F \subseteq Q$ is the set of accept states.

The transition function depends on the current state, input symbol and the top of the stack. In general operations on a PDA follow:
1. Start state
2. Input remains or not in final state
	1. Nondeterministically pick valud transition $a,b\rightarrow c$ from current state $q$, else reject
	2. $a$ is consumed
	3. replace top of stack $b$ with $c$
	4. Move to state $q$
3. Accept
We are permitted for the stack to be empty.

The PDA $(Q, \Sigma, \Gamma, \delta, q_0, F)$ accepts input $w$ if $w = v_1 v_2 \cdots v_n$ with each $v_i \in \Sigma_\epsilon$, and there are states $r_0, r_1, \dots, r_n \in Q$ and strings $s_0, s_1, \dots, s_n \in \Gamma^*$ such that:

1. $r_0 = q_0$ and $s_0 = \epsilon$,
2. $(r_{i+1}, b) \in \delta(r_i, v_{i+1}, a)$, $s_i = at$, $s_{i+1} = bt$ with $a, b \in \Gamma_\epsilon$ and $t \in \Gamma^*_\epsilon$,
3. $r_n \in F$.

**Notes:**
- There is no requirement that $s_n = \epsilon$, so the stack may be non-empty when the machine stops (even when it accepts).
- The empty stack cannot be popped.

An example configuration:
For $L=\{a^nb^n|n\geq0\}$
![[Pasted image 20241101213507.png]]
- $Q = \{q_0, q_1, q_2, q_3\}$
- $\Sigma = \{a, b\}$
- $\Gamma = \{a, \$\}$
- $\delta$ transitions:
  - $\delta(q_0, \epsilon, \epsilon) = \{(q_1, \$)\}$
  - $\delta(q_1, a, \epsilon) = \{(q_1, a)\}$
  - $\delta(q_1, b, a) = \{(q_2, \epsilon)\}$
  - $\delta(q_2, b, a) = \{(q_2, \epsilon)\}$
  - $\delta(q_2, \epsilon, \$) = \{(q_3, \epsilon)\}$
- For other inputs, $\delta$ returns $\emptyset$
- $q_0 = q_0$
- $F = \{q_0, q_3\}$
