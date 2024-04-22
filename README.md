> [!NOTE]
> **Problem $\mathbf{\Pi}$** ist gegben durch:
>
> 1. eine allgemeine Beschreibung aller vorkommende Parameter
> 2. eine genaue Beschreibung der Eigenschaften, die Lösung haben soll.

> [!NOTE]
> Eine **Instanz *I*** von $\mathbf{\Pi}$ erhalten wir, indem wir die Parameter von $\mathbf{\Pi}$ festlegen.

> [!NOTE]
> $\mathbf{D_{\Pi}}$ ist eine Familie/Klasse von Instanzen von einem Entscheidungsproblem $\mathbf{\Pi}$

# P Probleme
## 2SAT
> [!IMPORTANT]
> **Gegeben**:
> Menge U von Variablen,
> Menge C von Klausel über U,
> wobei jede Klausel genau **zwei** Literale enthält.
>
> **Frage**: Existiert eine erfüllende **Wahrheitsbelegung t** für C?
>
> **Kürz**: $(U, C, t)$

# NP/NP-vollständige Probleme

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

## SAT: das erste NP-vollständige Problem

> [!IMPORTANT]
> **Gegeben**: Menge U von Variablen, Menge C von Klausel über U.
>
> **Frage**: Existiert eine **Wahrheitsbelegung t** von U, sodass jede Klausel in C erfüllt wird?
>
> **Kürz**: $(U, C, t)$

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

---
**Lösung(allgemein)**:

eine genaue Beschreibung der Eigenschaften, die Lösung haben soll(ohne Beschreibung von Instanz)

$Wahrheitsbelegung:$

```math
t: U \longrightarrow \left \{true, false \right \},
```

$sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.$

**Lösung(Beispiel)**:

$$
t(x)=t(y)=t(z)=true
$$

---
**Ja-Instanz**:

Soll bestehen aus:

 1. konkrete Beschreibung einer **SAT**-Instanz
 2. konkrete Beschreibung von der **Wahrheitsbelegung**, bei der jede Klausel in C wahr ist $\Rightarrow$ **Wahrheitsbelegung t** ist erfüllbar

Eine Beispiel für Ja-Instanz von **SAT**:

```math
U = \left\{ x, y, z \right\}, C = \left\{ x \lor y, x \lor z\right\}
```

$$Eine\ Lösung:\ t(x)=t(y)=t(z)=true$$

**Nein-Instanz**:

Es gibt keine Wahrheitsbelegung, sodass jede Klausel in C wahr ist

$\Rightarrow$ **Wahrheitsbelegung t** ist nicht erfüllbar

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

### Beweise NP-vollständigkeit von SAT

später

## 3SAT

> [!IMPORTANT]
> **Gegeben**:
> Menge U von Variablen,
> Menge C von Klausel über U,
> wobei jede Klausel genau **drei** Literale enthält.
>
> **Frage**: Existiert eine erfüllende **Wahrheitsbelegung t** für C?
>
> **Kürz**: $(U, C, t)$

### Instanz und Lösung

**Instanz(allgemein)**:

```math
 Menge\ U\ von\ Varablen,\ Menge\ C\ von\ Klausel\ über\ U,\ wobei\ jede\ Klausel\ genau\ drei\ Literale\ enthält.
 ```

**Instanz(Beispiel)**:

```math
U= \left \{x, y, z\right \}, C = \left \{x \lor y \lor z, x \lor \bar{y} \lor z \right \}
```

---
**Lösung(allgemein)**:

$Wahrheitsbelegung:$

```math
t: U \longrightarrow \left \{true, false \right \},
```

$sodass\ in\ jede\ Klausel\ c \in C\ mindestens\ ein\ Literal\ wahr\ ist.$

**Lösung(Beispiel)**:

$$
t(x)=t(y)=t(z)=true
$$

---
**Ja-Instanz**:

**Wahrheitsbelegung t** ist erfüllbar

Eine Beispiel für Ja-Instanz von **3SAT**:

```math
U= \left \{x, y, z\right \}, C = \left \{x \lor y \lor z, x \lor \bar{y} \lor z \right \}
```

$$Eine\ Lösung:\ t(x)=t(y)=t(z)=true$$

### Beweis

**I. 3SAT $\in$ NP**

(Es existiert eine TM mit polynomialer Zeitkompexitätsfunktion, die in $q_{J}$ hält bei **Ja-Instanz**)
- Konstruiere eine OTM mit polynomialer Überprüfungsphase
   - **Das Orakel** ist eine Wahrheitsbelegung $t: U \longrightarrow \\{true, false \\}$
   - **Die endliche Kontrolle** überprüft, ob jede Klausel in C **durch t** erfüllt ist
   - Wenn alle Klauseln erfüllt sind, gehe in $q_{J}$
   - Wenn mindestens eine Klausel nicht erfüllt ist, gehe in $q_{N}$
- Für eine feste Wahrheitsbelegung t kann in polynomialer Zeit $O(|C|)$ (also linear), ob alle Klauseln aus C durch t erfüllt sind.

**II. SAT $\propto$ 3SAT**

