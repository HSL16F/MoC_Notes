If you have a language and that describes some automata A than that language is regular

If A is regular, then for some regular expression

GNFA is general nondeterministic finite automata, similar to NFA but have regex transition labels, it reads entire strings
Smallest GNFA is 2 states, need to have start state and an accept state, must be different
Proof for converting to state k-1 with induction to show that GFNA can be converted to Regular Expressions.
![[Pasted image 20241006141506.png]]
Removing the state x, but ensure that the regular expression is still value

Non regular languages:
To show language is not regular, require a proof to show you can not make a DFA, to show its regular, just make a DFA

ALL regular languages have pumping lemma property, so if it does not have that property, than it is not regular

Introduction to context free grammars:
Containts various substition rules
Rule is variable->String of variables and terminals
Anything on left side is a variable, everything on the righthand side is a terminal if its not a variable. empty string is a string NOT A terminal, just has length of 0
Top left symbol is typically the starting symbol.
Grammars define languages and generate strings
Generate until only terminals remain
CFG can create languages that DFA's can not be used