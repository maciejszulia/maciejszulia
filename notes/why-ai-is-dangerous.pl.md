# Dlaczego AI jest niebezpieczna

Sztuczna inteligencja to bardzo niebezpieczna technologia, bo trzeba wiedzieć, czego się od niej chce. Gdy człowiek prosi AI o coś, musi konkretnie wiedzieć, co chce uzyskać, gdyż to, o co prosi, zawiera zarówno rzeczy, których chce, jak i te, których nie chce.

W logice matematycznej:

- $`P`$: zbiór wyników, które spełniają prośbę, czyli to, co zostało powiedziane;
- $`C`$: zbiór wyników, których człowiek naprawdę chce.

Każda prośba rozpada się na dwie rozłączne części:

```math
P = (P \cap C) \cup (P \setminus C), \qquad (P \cap C) \cap (P \setminus C) = \varnothing
```

AI zwraca jakiś wynik $`x \in P`$: spełnia prośbę, a nie intencję. Prośba jest bezpieczna wtedy i tylko wtedy, gdy każdy wynik, który ją spełnia, jest chciany:

```math
\mathrm{bezpieczna}(P) \iff \forall x\,\big(x \in P \rightarrow x \in C\big) \iff P \subseteq C \iff P \setminus C = \varnothing
```

Jeśli $`\exists x\,(x \in P \land x \notin C)`$, AI może dostarczyć dokładnie to, o co proszono, i dokładnie to, czego nie chciano. Dlatego zanim o coś poproszę, zawężam $`P`$, aż $`P \setminus C = \varnothing`$: podaję cel, granice i to, czego ma nie robić.

[Profil](../README.pl.md)
