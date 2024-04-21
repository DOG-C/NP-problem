# NP-Problem

## SAT

**Gegeben**: Menge U von Variablen, Menge C von Klausel über U.

**Frage**: Existiert eine **Wahrheistbelegung** von U, sodass jede Klausel in C erfüllt wird?

### Instanz und Lösung

**Instanz(allgemein)**:

```math
 Menge\ U\ von\ Varablen,\ Menge\ C\ von\ Klausel\ über\ U.
 ```

**Instanz(Beispiel)**:

```math
U= \left \{x, y, z\right \}, C = \left \{x \lor y, x \lor z \right \}
```

**Lösung(allgemein)**:

$$ Wahrheitsbelegung:$$

$$f: U \longrightarrow \left \{true, false\right \},$$

$$
 sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.
$$

**Lösung(Beispiel)**:

$$
f(x)=f(y)=f(z)=true
$$