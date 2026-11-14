# Why is a request to a machine dangerous?

What do you get when a machine fulfils your request to the letter?

This note states one thesis about working with a machine. It is built like a chapter of the text [“Perfekcja – koniec ludzkości?”](https://github.com/maciejszulia/philosophy): a phenomenon, a thesis, the weak point of the thesis, questions. The word “machine” covers a program that everyday language calls artificial intelligence (AI).

## Terms

| Term | Definition |
|---|---|
| machine | A system built by people that performs computations. |
| request | The text a person gives a machine as a description of the result. |
| intent | The state of the world the person wants after the request is fulfilled. |
| result | The state of the world the machine produces after the request. |
| set P | The set of results that satisfy the words of the request. |
| set C | The set of results the person wants. |

## Phenomenon

A thermostat keeps 20 °C at its sensor. A person sits by the window, 4 m from the sensor. By the window it is 17 °C. The thermostat satisfies what was written: 20 °C at the sensor. The thermostat does not know the intent: warmth by the window.

Ovid wrote down the same phenomenon in the “Metamorphoses”[^ovid]. King Midas asks a god for a gift: everything Midas touches is to turn into gold. The god fulfils the request to the letter. The bread in Midas's hand turns into gold. Midas got a result that satisfies the words of the request. Midas wanted a different result.

## In set logic

A request splits the set P into two disjoint parts:

$$P = (P \cap C) \cup (P \setminus C) \qquad (1)$$

- $P \cap C$: the results that satisfy the words and that the person wants;
- $P \setminus C$: the results that satisfy the words and that the person rejects.

The machine returns one result from the set P. The machine satisfies the words of the request. The machine does not know the set C.

A request is safe in exactly one case:

$$P \subseteq C \iff P \setminus C = \varnothing \qquad (2)$$

Formula (2) says: every result that satisfies the words is a result the person wants. The golden bread of Midas lies in the part $P \setminus C$. So does 17 °C by the window.

## Thesis

**Thesis.** A machine is a dangerous technology because it requires a person to know their own intent.

The strict form: a request is dangerous only if the part $P \setminus C$ holds at least one result. The danger lies in the request, not in the machine.

A machine is a solution: it removes the problem of execution. Thesis 2 of the text says that every new solution leads to new problems. The new problem is the intent. A person who handed the execution to a machine is left with one question: what do I want?

Norbert Wiener gave the same warning in 1960[^wiener]. A person who hands a purpose to a machine should be sure that the machine received the purpose the person really wants.

## What the person does

Narrowing a request takes the three acts of thesis 8 of the same text: an act of will, an act of attention and an act of responsibility. Do the steps in this order:

1. Will: write the intent as a state you can check.
2. Attention: name what the machine must not change.
3. Attention: name at least one result you reject.
4. Responsibility: check the result before you use it.

Outcome: the part $P \setminus C$ is smaller, and the result of the machine is your result.

A wide request: “Clean up the directory.”

A narrowed request: “Delete from the directory `tmp` every `.log` file older than 30 days. Leave every other file unchanged. Print the names of the deleted files.”

## The weak point of the thesis

A person does not know the whole set C before seeing a result. A person learns part of their own intent only when they see a result they reject. The set P also depends on how the machine reads the words of the request. The person does not see that reading. Formula (2) therefore states a condition that the person cannot check before the request.

## Questions

1. Recall a request that a machine fulfilled to the letter and against your intent. Which word was too wide?
2. Write down three results you reject before you send your next request. How many minutes did that take?
3. Midas got exactly what he asked for. Who answers for the golden bread: Midas or the god?
4. You ask a person and a machine for the same thing. Which of them will ask what you really want?
5. Is there a request for which the part $P \setminus C$ is empty? Give one.

## Related

- [philosophy](https://github.com/maciejszulia/philosophy): thesis 2, thesis 7 and thesis 8.
- [tractatus-skills](https://github.com/maciejszulia/tractatus-skills): the skill `tractatus-sense` narrows the set P before the work, and the skill `tractatus-verify` checks the result after it.
- [polszczyzna-kontrolowana](https://github.com/maciejszulia/polszczyzna-kontrolowana): rules that leave a sentence of a request one meaning.

[Profile](../README.md) | [Polski](why-ai-is-dangerous.pl.md)

[^ovid]: Ovid, “Metamorphoses”, book XI, lines 85–145.
[^wiener]: N. Wiener, “Some Moral and Technical Consequences of Automation”, “Science” 131 (3410), 1355–1358 (1960). [doi:10.1126/science.131.3410.1355](https://doi.org/10.1126/science.131.3410.1355)
