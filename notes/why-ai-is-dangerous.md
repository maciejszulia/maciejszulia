# Why AI is dangerous

AI is a very dangerous technology, because you have to know what you want from it. When you ask an AI for something, you must know exactly what you want to get, because what you ask for contains both things you want and things you do not want.

In mathematical logic:

- $`P`$: the set of results that satisfy the request, that is, what was said;
- $`C`$: the set of results the person actually wants.

Every request splits into two disjoint parts:

```math
P = (P \cap C) \cup (P \setminus C), \qquad (P \cap C) \cap (P \setminus C) = \varnothing
```

The AI returns some $`x \in P`$: it satisfies the request, not the intent. A request is safe exactly when every result that satisfies it is wanted:

```math
\mathrm{safe}(P) \iff \forall x\,\big(x \in P \rightarrow x \in C\big) \iff P \subseteq C \iff P \setminus C = \varnothing
```

If $`\exists x\,(x \in P \land x \notin C)`$, the AI can deliver exactly what was asked for and exactly what was not wanted. So before I ask, I narrow $`P`$ until $`P \setminus C = \varnothing`$: I state the goal, the limits and what must not happen.

[Profile](../README.md)
