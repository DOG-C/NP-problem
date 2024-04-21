# Problem

> [!NOTE]
> **Problem $\mathbf{\Pi}$** ist gegben durch:
>
> 1. eine allgemeine Beschreibung aller vorkommende Parameter
> 2. eine genaue Beschreibung der Eigenschaften, die Lösung haben soll.

> [!NOTE]
> Eine **Instanz *I*** von $\mathbf{\Pi}$ erhalten wir, indem wir die Parameter von $\mathbf{\Pi}$ festlegen.

> [!NOTE]
> $\mathbf{D_{\Pi}}$ ist eine Familie/Klasse von Instanzen von einem Entscheidungsprblem $\mathbf{\Pi}$

## P Probleme

## NP/NP-vollständige Probleme

> [!NOTE]
> Ein Problem $\Pi \in NP$:
>
> Es existiert eine TM mit polynomialer Zeitkompexitätsfunktion, die in $q_{J}$ hält bei **Ja-Instanz**.
>
> $\Rightarrow$ Konstruire eine OTM mit polynomialer Überprüfungsphase

> [!NOTE]
> Ein Problem $\Pi$ ist NP-vollständig
>
> - $\Pi \in NP$
> - ${\Pi}' \propto \Pi$ für alle ${\Pi}' \in NP$ **oder**
> - ${\Pi}' \propto \Pi$ für ein bekanntes NP-vollständiges ${\Pi}'$

### SAT(Das erste NP-vollständige Problem)

> [!IMPORTANT]
> **Gegeben**: Menge U von Variablen, Menge C von Klausel über U.
>
> **Frage**: Existiert eine **Wahrheistbelegung** von U, sodass jede Klausel in C erfüllt wird?

#### Instanz und Lösung

---
**Instanz(allgemein)**:

eine allgemeine Beschreibung aller vorkommende Parameter

```math
 Menge\ U\ von\ Varablen,\ Menge\ C\ von\ Klausel\ über\ U.
 ```

**Instanz(Beispiel)**:

```math
U= \left \{x, y, z\right \}, C = \left \{x \lor y, x \lor z \right \}
```

---
**Lösung(allgemein)**:

eine genaue Beschreibung der Eigenschaften, die Lösung haben soll(ohne Beschreibung von Instanz)

$Wahrheitsbelegung:$

```math
f: U \longrightarrow \left \{true, false \right \},
```

$sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.$

**Lösung(Beispiel)**:

$$
f(x)=f(y)=f(z)=true
$$

---
**Ja-Instanz**:

Soll bestehen aus:

 1. konkrete Beschreibung einer **SAT**-Instanz
 2. konkrete Beschreibung von der **Wahrheitsbelegung**, bei der jede Klausel in C wahr ist.

Eine Beispiel für Ja-Instanz von **SAT**:

```math
U = \left\{ x, y, z \right\}, C = \left\{ x \lor y, x \lor z\right\}
```

$$Eine\ Lösung\ f(x)=f(y)=f(z)=true$$

**Nein-Instanz**:

Es gibt keine Wahrheitsbelegung, sodass jede Klausel in C wahr ist.

Eine Beispiel für Nein-Instanz von **SAT**:

```math
U = \left\{x, y, z\right\},\ C = \left\{ \bar{x},\ \bar{z},\ x \lor y,\ \bar{y} \lor z \right\}
\\
```

|  x  |  y  |  z  | $\mathbf{\bar{x}}$ | $\mathbf{\bar{y}}$ | $\mathbf{\bar{z}}$ | $\mathbf{x \lor y}$ | $\mathbf{\bar{y} \lor z}$|erfüllt?|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|0|0|0|**1**|1|**1**|**0**|**1**|Nein|
|0|0|1|**1**|1|**0**|**0**|**1**|Nein|
|0|1|0|**1**|0|**1**|**1**|**0**|Nein|
|0|1|1|**1**|0|**0**|**1**|**1**|Nein|
|1|0|0|**0**|1|**1**|**1**|**1**|Nein|
|1|0|1|**0**|1|**0**|**1**|**1**|Nein|
|1|1|0|**0**|0|**1**|**1**|**0**|Nein|
|1|1|1|**0**|0|**0**|**1**|**1**|Nein|

