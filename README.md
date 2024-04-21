# NP-Problem

## SAT

**Gegeben**: Menge U von Variablen, Menge C von Klausel über U.

**Frage**: Existiert eine **Wahrheistbelegung** von U, sodass jede Klausel in C erfüllt wird?

### Instanz und Lösung

**Instanz(allgemein)**:

$$
\text{Menge U von Variablen, Menge C von Klausel über U.}
$$
**Instanz(Beispiel)**:

$$ U= \\{x, y, z\\}, C = \\{x \lor y, x \lor z \\} $$

**Lösung(allgemein)**:

$$
\text{Wahrheitsbelegung:} \\
f: U \longrightarrow \{ \text{true}, \text{false} \}, \\
\text{sodass in jede Klausel } c \in C \text{ mindestens ein Literal wahr ist.}
$$


**Lösung(Beispiel)**:

$$
f(x)=f(y)=f(z)=true
$$