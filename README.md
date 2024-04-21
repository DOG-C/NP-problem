# NP-Problem

> [!NOTE]
> **Problem $\mathbf{\Pi}$** ist gegben durch:
>
> 1. eine allgemeine Beschreibung aller vorkommende Parameter
> 2. eine genaue Beschreibung der Eigenschaften, die Lösung haben soll.

> [!NOTE]
> Eine **Instanz *I*** von $\mathbf{\Pi}$ erhalten wir, indem wir die Parameter von $\mathbf{\Pi}$ festlegen.

> [!NOTE]
> $\mathbf{D_{\Pi}}$ ist eine Familie/Klasse von Instanzen von einem Entscheidungsprblem $\mathbf{\Pi}$

## SAT

> [!IMPORTANT]
> **Gegeben**: Menge U von Variablen, Menge C von Klausel über U.
> 
> **Frage**: Existiert eine **Wahrheistbelegung** von U, sodass jede Klausel in C erfüllt wird?

### Instanz und Lösung

**Instanz(allgemein)**:

eine allgemeine Beschreibung aller vorkommende Parameter

```math
 Menge\ U\ von\ Varablen,\ Menge\ C\ von\ Klausel\ über\ U.
 ```

**Instanz(Beispiel)**:

```math
U= \left \{x, y, z\right \}, C = \left \{x \lor y, x \lor z \right \}
```

**Lösung(allgemein)**:

eine genaue Beschreibung der Eigenschaften, die Lösung haben soll

$$ Wahrheitsbelegung:$$

```math
f: U \longrightarrow \left \{true, false \right \},
```

$$
 sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.
$$

**Lösung(Beispiel)**:

$$
f(x)=f(y)=f(z)=true
$$

**Ja-Instanz**:

Instanz mit einer Lösung:

eine Menge von Variablen, also $U= \{ x, y, z \}$ and eine Menge von Klausel über U, also $C = \{ x \lor y, x \lor z \}$

eine Lösung $f(x)=f(y)=f(z)=true$

**Nein-Instanz**:

Instanz ohne Lösung
