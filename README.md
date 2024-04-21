# NP-Problem

## SAT

**Gegeben**: Menge U von Variablen, Menge C von Klausel über U.

**Frage**: Existiert eine **Wahrheistbelegung** von U, sodass jede Klausel in C erfüllt wird?

### Instanz und Lösung

**Instanz(allgemein)**:

$$ Menge\ U\ von\ Varablen,\ Menge\ C\ von\ Klausel\ über\ U.$$

**Instanz(Beispiel)**:

$$ U= \\{x, y, z\\}, C = \\{x \lor y, x \lor z \\} $$

**Lösung(allgemein)**:

$$ Wahrheitsbelegung:$$

 $$f: U \longrightarrow \{true, false\},$$

$$
 sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.
$$

**Lösung(Beispiel)**:

$$
f(x)=f(y)=f(z)=true
$$