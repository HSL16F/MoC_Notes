CGF's can be used to generate [[Context Free Languages]], a simple algorithm follows:
CFG's consist of variables and terminals.
Starting with the LHS of the first rule, you replace a variable on the with some terminal or variable on the RHS, you repeat this until no variables remain
The strings creates are called sentential forms
Formally they are defined as a 4 tuple $(V, \Sigma, R, S)$
1. $V$ is a finite set of variables
2. $\Sigma$ is a finite set, disjoint from V of terminals
3. $R\subseteq V \times (V\cup\Sigma)^*$ is finite set of rules
4. $S\in V$ is the start variable
For example:
$$\begin{align}
A\rightarrow0A0 \\
A\rightarrow1A1 \\
A\rightarrow\epsilon
\end{align}
$$
Which produced grammars such as $00100100, 0110, 00111100, 010010$ is formally defined
$V={A}, \Sigma={0,1}, S=A$
$$\begin{align}
R=\{(A, 0A0),\\
(A,1A1),\\
(A,\epsilon)\} \end{align}
$$
OR statements are permitted in context free grammars, general rule is you use the first variable. In the case of parse trees, are used.
Grammar is defined as ambiguous if and only iff there is two or more different parse trees for some given string.
Often equivalent but unambiguous grammar can be found, but for every CFG for the following grammar is ambiguous $\{a^ib^jc^k|i=j\lor j=k\}$, such [[Context Free Languages|CFL's]] are ambiguous

Regular Grammars generally correspond to regular languages, but CFG's can be of either form depending on how you restrict it.