# 1. előadás
## Kombinatorika  
**Permutáció**: *n* megkülönböztethető elemek rendezett sorozata  
$$P_n = n!$$  
**Ismétléses permutáció**:  
$$P_n^{k_1, k_2, ..., k_m} = \frac{n!}{k_1! \cdot k_2! \cdot \cdot \cdot k_m!} $$  
**Variáció**: Adott *n* elem *k* elemű részhalamzának rendezése  
$$V_n^k = \frac{n!}{n-k!} $$  
**Ismétléses variáció**:  
$$V_n^{k,r} = n^k $$  
**Kombináció**: Legyen *n* megkülönböztethető elemünk, *k* elemet választunk úgy, hogy minden egyes elem pontosan egyszer választható  
$$C_n^k = \binom{n}{k} = \frac{n!}{(n-k)!}$$  
**Ismétléses kombináció**:  
$$C_n^{k,r} = \binom{n+k-1}{k}$$  

---
# 2. előadás
## Valószínűségi mező  
**Definíció**: Egy K kisérlet eredményei, amelyeket nem tudunk felosztani kisebb részekre **elemi eseményeknek** nevezzük. Az elemi eseményeket ***ω*** jelölik. Az összes elemi esemény halmazát **mintatérnek** (valószínűségi térnek) nevezzük. Jelölése: ***Ω***

- **Példa**:  
  Érmedobás: $Ω = \{Fej,Írás\}$

---

## Relatív gyakoriság

**Definíció:** Ha egy kisérletet *n* alkalommal ismétlünk, és $A$ esemény $k_a$ alkalommal fordul elő akkor:  
$$\frac{k_a}{n}$$  
nevezzük **relatív gyakoriságnak**.

---

## Eloszlás  
$Ω = \{ω_1,...,ω_N\}$ mintatér esetén a $p_1,...,p_N$ értékeket eloszlásnak nevezünk.
Például eloszlás lesz  
$$p_1 = 0.2 \quad p_2 = 0.5 \quad p_3 = 0.3$$

### Jellemzői
- $p_i$ számok nem negatívak
- a valószínűségek összege 1
  $$\sum_{i=1}^Np_i = 1$$

---

## Klasszikus valószínűség
**Definíció:** ha egy kisérlet lehetséges kimenetelei egyenlően valószínűek akkor A esemény valószínűsége:  
$$P(A) = \frac{\text{kedvező esetek száma}} {\text{összes lehetséges eset száma}}$$

### A valószínűség geometriai kiszámítása

$$P(A) = \lambda(\text{pont})/\lambda(\text{összes})$$  
ahol $\lambda$ a hossz, terület vagy térfogat, ha egyenesen, síkon vagy térben vagyunk.

---

## Feltételes valószínűség  
**Definíció**:  
A feltételes valószínűség megmutatja $A$ valószínűségét, ha $B$ bekövetkezett:  
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$  

---

## Teljes valószínűség tétele  
**Definíció**: Legyen $B_1, B_2, ...$ teljes eseményrendszer. Ha $P(B_i)>0$ bármely $i$ esetén, akkor $A$:  
$$P(A) = \sum_{i=1}^n P(A|B_i) \cdot P(B_i)$$  

---

## Bayes tétel  
**Bayes formula**:  
$$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$$  
**Bayes tétel**:  
$$P(B_i|A) = \frac{P(A|B_i)P(B_i)}{\sum_{j=1}^\infty P(A|B_j)P(B_j)}$$  

---

## Eseményfüggetlenség  
**Definíció**: $A$ esemény független $B$ eseménytől, ha B bekövetkezése nincs hatással $A$ valószínűségére. Azaz:
$$P(A|B) = P(A)$$  
**Definíció**: Azt mondjuk hogy $A$ és $B$ **független**, ha:
$$P(A \cap B) = P(A) \cdot P(B)$$  

### Páronkénti függetlenség
**Definíció**: Azt mondjuk, hogy az $A_1, A_2, ...$ események **páronként** függetlenek, ha közülük bármely kettő független, azaz:
$$P(A_iA_j) = P(A_i)P(A_j), i\not ={j}$$

### Teljes függetlenség
**Definíció**: Azt mondjuk, hogy az $A_1, A_2, ...$ események **teljesen** függetlenek, ha bármely eseményszámra és bármely indexű eseményekre független, azaz:

$$P(A_{i_1}A_{i_2}...A_{i_k}) = P(A_{i_1})P(A_{i_2})...P(A_{i_k})$$

---

# 3. előadás
## Valószínűségi változó
**Definíció**: adott $\Omega$ eseménytér, $\mathcal{F}$ eseményhalmaz. A valószínűségi változó egy olyan függvény, amely az eseményhalmazból leképzést készít a valós számok egy megszámlálható halmazává. $X:\mathcal{F} → D$

---

## Diszkrét valószínűségi változó
**Definíció**: olyan valószínűségi változó, melynek értékkészlete megszámlálható  
Például kockadobás:
$$P(X = 1) = \frac{1}{6}$$  
$$P(X = 2) = \frac{1}{6}$$  
$$P(X = 3) = \frac{1}{6}$$  
$$P(X = 4) = \frac{1}{6}$$  
$$P(X = 5) = \frac{1}{6}$$  
$$P(X = 6) = \frac{1}{6}$$  

---

## Várható érték 

**Definíció**: Egy valószínűségi változó súlyozott átlaga.  
**Képlete**: $\sum_{k=1}^\infty p_kx_k$, ahol $p_k$ a valószínűség, $x_k$ az érték  
**Például**:  Kockadobások várható értéke: $\frac{1}{6}\cdot1+\frac{1}{6}\cdot2+\frac{1}{6}\cdot3+\frac{1}{6}\cdot4+\frac{1}{6}\cdot5+\frac{1}{6}\cdot6 =3.5$  
**Második momentum**: $EX^2 = \sum_{k=1}^\infty p_kx^2_k$  
**Jellemzői**:
  - Lineáris: 
    - $E(X+Y)=EX+EY$
    - $E(cX)=cE(X)$
  - Ha $X$ és $Y$ Független, akkor $E(XY) = E(X) \cdot E(Y)$  

---

## Szórásnégyzet (variancia)  
**Definíció**: A szórásnégyzet, más néven variancia megmutatja, hogy egy valószínűségi változó milyen mértékben szóródik a várható érték körül.  
$$D^2X = \text{Var}(X) = EX^2 - E^2X$$  
**Tulajdonságai**:
  - $\text{Var}(aX+b)=a^2\text{Var}X$

---

## Nevezetes diszkrét eloszlások  

1. **Hipergeometrikus eloszlás**:
   - $X \sim Hyper(N, M, n)$
   - **Jelentése:** Összesen $N$ golyó van a dobozban, benne $M$ piros golyó, $N-M$ fehér golyó. Ki szeretnénk húzni $n$ darabot belőlük **visszatevés nélkül**. 
   - **Képlete:**
   $$h_k = P(X = k) = \frac{\binom{M}{k}\binom{N-M}{n-k}}{\binom{N}{n}}$$
   ahol $k$ a kihúzni kívánt piros golyók száma.
   - **Várható értéke:** $E=\frac{Mn}{N}$

2. **Binomiális eloszlás**:  
   - $X \sim Binom(n, p)$
   - **Jelentése:** Összesen $N$ golyó van a dobozban, benne $M$ piros golyó, $N-M$ fehér golyó. Ki szeretnénk húzni $n$ darabot belőlük **visszatevéssel**. $p = \frac{M}{N}$, vagyis a piros golyók relatív valószínűsége.
   - **Képlete:** 
     $$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$  
   - **Várható értéke:** $E=n \cdot p$

3. **Poisson-eloszlás**:  
   - $X \sim Poisson(\lambda)$
   - **Jelentése:** Akkor használjuk, ha egy adott időintervallumon bekövetkező események számát szeretnénk jellemezni.  
   - **Például**: egy telefonközpontba átlagosan $\lambda=5$ hívás érkezik percenként. Mi annak a valószínűsége, hogy egy adott percben pontosan 3 hívás érkezik?
   - **Képlete**:  
     $$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$
   - **Várható értéke:** $E=\lambda$

4. **Negatív binomiális eloszlás**:  
   - $X \sim NB(r, p)$
   - **Jelentése**: Addig figyeljük a sorozatot, amíg $r$ siker nem következik be. Egy siker valószínűsége $p$.
   - **Például**: Addig dobunk dobókockával, amíg 2 darab 6-ost nem dobunk. Itt $p=1/6, r=2$.
     - **Részesete**: Ha $r=1$, akkor **geometrikus eloszlás**ról beszélünk
     - **Képlete**: $P(X = 1+k) = p(1-p)^k$
   - **Várható értéke:** $E=\frac{r}{p}$

---

## Poisson eloszlás várható értékének levezetése (5-ért)

1. Felírjuk a várható érték képletét a Poisson eloszlásra  
   $$EX = \sum_{k=0}^\infty k\cdot\frac{\lambda^k}{k!}e^{-\lambda}$$
2. $k = 0$ szorzó elhagyható, lehet egyszerűsíteni a $k$-val, tehát:  
   $$EX = \sum_{k=1}^\infty\frac{\lambda^k}{(k-1)!}e^{-\lambda}$$  
3. $k-1$ helyére írjunk $l$-t, tehát:
   $$EX = \sum_{l=0}^\infty\frac{\lambda^{l+1}}{l!}e^{-\lambda}$$  
4. Kiemelünk egy $\lambda$-t a számlálóból, kihozzuk a szumma elé, és kiemeljük az $e^{-\lambda}$  
   $$EX = \lambda e^{-\lambda} \sum_{l=0}^\infty\frac{\lambda^{l}}{l!}$$  
5. $\sum_{l=0}^\infty\frac{\lambda^{l}}{l!} = e^\lambda$ Taylor-sort felhasználva, ebből következik  
   $$EX = \lambda e^{-\lambda} e^\lambda$$
6. $e^\lambda \cdot \frac{1}{e^\lambda} = 1$, tehát:  
   $$EX = \lambda$$

---

## Eloszlásfüggvény  
**Definíció**: Megadja, hogy a valószínűségi változó egy adott értékig bezárólag mekkora valószínűséggel vesz fel értéket. Diszkrét eloszlásfüggvénynél ez egy lépcsős függvény.  
$F_X(x)=P(X<x)$

![diszkret eloszlas](/diszkel.jpg)
### Diszkrét eloszlásfüggvény tulajdonságai:  
- A függvény monoton növekvő.  
- A függvény bal-folytonos. 
- $\lim_{x→\infty}F(x) = 1, \lim_{x→-\infty}F(x) = 0$  

---

# 4. előadás
## Abszolút folytonos eloszlásfüggvény tulajdonságai  
$F(b)-F(a)$: Az érték [a, b] intervallumba esésének valószínűsége.  
![abszolut folytonos eloszlas](/fbfa.jpg)

---

## Sűrűségfüggvény  
**Definíció**: Deriváltja az eloszlásfüggvénynek:  
Legyen $f$ a sűrűségfüggvény, $F$ az eloszlásfüggvény
$$f(x) = F'(x)$$  
$$F(x) = \int_{-\infty}^xf(x)dx$$  
**Tulajdonságai:**
  - $\lim_{x→-\infty}f(x) = 0$
  - $\lim_{x→\infty}f(x) = 1$
  - $\int_{-\infty}^\infty f(x)dx = 1$  

---

## Várható érték
Itt nem alkalmazható a diszkrét várható érték képletet, mert megszámláhatatlan sok valószínűségi változó van.  
**Képlete:** 
$$EX = \int_{-\infty}^{+\infty} xf(x)dx$$
**Tulajdonságai:**
  - Lineáris
  - Ha $X\geq 0$, akkor $EX\geq 0$
  - Ha $X\geq Y$, akkor $EX\geq Y$
  - Ha $X\geq 0$ és $EX = 0$, akkor $P(X=0)=1$

---

## Nagy számok törvénye  
**Definíció**: Egy minta átlaga nagy mintaszám esetén közelít a várható értékhez.

---

## Nevezetes abszolút folytonos eloszlások
  1. **Egyenletes eloszlás**  
     ![eloszlas](egyenletes.png)
     ![suruseg](egyenletessur.png)  
     - **Eloszlásfüggvény**:  
      ![eloszlasfuggveny](egyenleteseloszfv.png)  
     - **Sűrűségfüggvény**:  
      ![surusegfuggveny](egyenletessurusegfv.png)  
     - **Várható érték**:  
       $$E(X) = \frac{a+b}{2}$$  
     - **Szórásnégyzet**:  
       $$\text{Var}(X) = \frac{(b-a)^2}{12}$$  
  2. **Normális eloszlás**  
     ![eloszlas](norm.png)
     ![suruseg](normsur.png)
     - **Sűrűségfüggvény (csak 5ért)**  
       $$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$
       ahol $\sigma$ a szórás, $\mu$ pedig a várható érték
     - **Standardizálás**  
     **Definíció:** Mivel minden normális eloszlás a standard normális egy transzformáltjával egyenlő, bármely x pont átalakítható egy vele azonos standard normális-beli z ponttá.
     $$z = \frac{x-\mu}{\sigma}$$

## Központ határeloszlás tétele
**Definició:** egy elég nagy mintaméretű független és azonos eloszlású valószínűségi változók összege (vagy átlag) közelítőleg normális eloszlást követ, még akkor is, ha az eredeti változók eloszlása nem normális.

# 5. előadás
## Mintavételi módszerek  
- **Véletlenszerű mintavétel**: Minden elemnek azonos esélye van bekerülni.  

### Mintátlag  
- $$\bar{X}$$: Mintában szereplő elemek átlaga.  
- Tulajdonság: Mintanagyság növelésével $$\bar{X}$$ közeledik \( E(X) \)-hez.  

### Medián  
Az az érték, amelynél a minta elemeinek fele kisebb, fele nagyobb.  

### Kvantilis  
Az \( q \)-adik kvantilis az az érték, amelynél az elemek \( q \)-ad része kisebb.  

---

### Illeszkedésvizsgálat  
- **Próbastatisztika**:  
  $$\chi^2 = \sum \frac{(O_i - E_i)^2}{E_i}$$  
  ahol \( O_i \) a megfigyelt, \( E_i \) a várható gyakoriság.  
- Mindig jobboldali próba.  

---

### Függetlenségvizsgálat  
- **Kontingenciatáblázat**: Sor- és oszlopgyakoriságok.  
- Függetlenség, ha a peremeloszlások szorzata adja az együttes valószínűségeket.

---

### Nevezetes eloszlások

#### Egyenletes eloszlás  
**Definíció**: Az \( [a, b] \) intervallumban minden érték azonos valószínűséggel fordul elő.  

---

### Kontingencia táblázat  

**Definíció**: Többváltozós adatok elemzésére használt tábla, amely sorokban és oszlopokban gyakoriságokat vagy relatív gyakoriságokat mutat.  

- **Marginalis (peremeloszlások)**:  
  A sorok és oszlopok összegzett értékei, amelyek az egyes változók eloszlását adják.  

#### Példa:  
|       | B1 | B2 | Összesen |  
|-------|----|----|----------|  
| A1    | 10 | 20 | 30       |  
| A2    | 15 | 25 | 40       |  
| Össz. | 25 | 45 | 70       |  

---

### Függetlenség  
**Definíció**: Két változó független, ha az együttes eloszlásuk a peremeloszlások szorzataként írható fel:  
$$P(A \cap B) = P(A) \cdot P(B)$$  

#### Példa:  
- Ha a fenti kontingencia táblában:  
  $$P(A1, B1) = \frac{10}{70}, \quad P(A1) \cdot P(B1) = \frac{30}{70} \cdot \frac{25}{70}$$  
  és ezek egyenlők, akkor \( A \) és \( B \) függetlenek.

---

### Együttes eloszlásfüggvény  
**Definíció**: Két változó (\(X\) és \(Y\)) együttes eloszlása:  
$$F_{X,Y}(x, y) = P(X \leq x, Y \leq y)$$  

- Tulajdonságok:  
  - Monoton növekvő mindkét változó szerint.  
  - Határértékek:  
    $$F_{X,Y}(\infty, y) = F_Y(y), \quad F_{X,Y}(x, \infty) = F_X(x)$$  

---

### Együttes sűrűségfüggvény  
**Definíció**: Ha \( X \) és \( Y \) folytonos valószínűségi változók:  
$$f_{X,Y}(x, y) = \frac{\partial^2}{\partial x \partial y} F_{X,Y}(x, y)$$  

- Tulajdonságok:  
  - \( f_{X,Y}(x, y) \geq 0 \).  
  - A teljes valószínűség integrálja:  
    $$\int_{-\infty}^\infty \int_{-\infty}^\infty f_{X,Y}(x, y) \,dx\,dy = 1$$  

---

### Kovariancia  
**Definíció**: Két változó közötti lineáris kapcsolat mértéke.  
$$\text{Cov}(X, Y) = E[(X - E(X))(Y - E(Y))]$$  

- **Tulajdonságai**:  
  - Ha \( \text{Cov}(X, Y) > 0 \), akkor \( X \) és \( Y \) pozitív lineáris kapcsolatban állnak.  
  - Ha \( \text{Cov}(X, Y) < 0 \), akkor \( X \) és \( Y \) negatív lineáris kapcsolatban állnak.  
  - Ha \( \text{Cov}(X, Y) = 0 \), akkor \( X \) és \( Y \) lineárisan függetlenek lehetnek.  

---

### Korreláció  
**Definíció**: A kovariancia és a szórások hányadosa, amely normált mértékét adja a lineáris kapcsolatnak.  
$$\rho_{X,Y} = \frac{\text{Cov}(X, Y)}{\sigma_X \cdot \sigma_Y}$$  

- **Tulajdonságai**:  
  - \( \rho_{X,Y} \in [-1, 1] \).  
  - Ha \( \rho_{X,Y} = 1 \), akkor \( X \) és \( Y \) teljesen pozitív lineáris kapcsolatban állnak.  
  - Ha \( \rho_{X,Y} = -1 \), akkor \( X \) és \( Y \) teljesen negatív lineáris kapcsolatban állnak.  
  - Ha \( \rho_{X,Y} = 0 \), akkor nincs lineáris kapcsolat \( X \) és \( Y \) között.  

---

### Minta definíciója  
**Definíció**: Egy minta egy populációból véletlenszerűen kiválasztott elemek halmaza, amelyeket a populáció tulajdonságainak vizsgálatára használunk.

---

### Empirikus eloszlásfüggvény  
**Definíció**: Az empirikus eloszlásfüggvény a minta kumulatív gyakoriságát írja le.  

- **Képlet**:  
  $$F_n(x) = \frac{1}{n} \sum_{i=1}^n \mathbb{1}_{X_i \leq x}$$  
  ahol \( \mathbb{1}_{X_i \leq x} \) az indikátorfüggvény, amely 1, ha \( X_i \leq x \), és 0, különben.

---

### Hisztogram  
**Különbség a gyakorisági és sűrűségi hisztogram között**:  
- **Gyakorisági hisztogram**: A mintában előforduló értékek gyakoriságát ábrázolja.  
- **Sűrűségi hisztogram**: A mintabeli gyakoriságokat a csoport szélességével normalizálja, így területe 1.  

---

### Mintátlag és várható érték  
- **Mintátlag**:  
  $$\bar{X} = \frac{1}{n} \sum_{i=1}^n X_i$$  
- **Tulajdonság**: A mintaméret (\(n\)) növelésével a mintátlag közelít a várható értékhez (\(E(X)\)).  

---

### Empirikus szórásnégyzet  
- **Képlet**:  
  $$S^2 = \frac{1}{n-1} \sum_{i=1}^n (X_i - \bar{X})^2$$  
  Ez egy becslés a populáció szórásnégyzetére.  

---

### Medián, Kvantilis, Kvartilis  
- **Medián**: Az az érték, amelynél a minta fele kisebb, fele nagyobb.  
- **Kvantilis**: Az \( q \)-adik kvantilis az az érték, amelynél a megfigyelések \( q \)-ad része kisebb vagy egyenlő.  
- **Kvartilisok**: Az alsó és felső kvartilis az első (25%) és harmadik (75%) kvantilis.  

- **Képlet**:  
  - Medián (\( Q_2 \)): Ha \( n \) páros:  
    $$Q_2 = \frac{X_{(n/2)} + X_{(n/2 + 1)}}{2}$$  
    Ha \( n \) páratlan:  
    $$Q_2 = X_{((n+1)/2)}$$  
  - Alsó kvartilis (\( Q_1 \)):  
    $$Q_1 = F^{-1}(0.25)$$  
  - Felső kvartilis (\( Q_3 \)):  
    $$Q_3 = F^{-1}(0.75)$$  

---

### Dobozábra  
**Összetevői**:  
1. Minimum.  
2. Alsó kvartilis (\( Q_1 \)).  
3. Medián (\( Q_2 \)).  
4. Felső kvartilis (\( Q_3 \)).  
5. Maximum.  
6. Szélsőséges értékek (outlierek), ha vannak.  

---

### Maximum likelihood (ML) módszer  
**Definíció**: A maximum likelihood becslés az a paraméterérték, amely maximális valószínűséget biztosít a megfigyelt mintára.  

- **Formális megfogalmazás**:  
  Keressük azt a \( \theta \)-t, amely maximalizálja a likelihood függvényt:  
  $$L(\theta) = \prod_{i=1}^n f(X_i \mid \theta)$$  
  ahol \( f(X_i \mid \theta) \) a sűrűségfüggvény.  

- **Log-likelihood**: Gyakran egyszerűbb a logaritmált likelihood-dal dolgozni:  
  $$\ell(\theta) = \log L(\theta) = \sum_{i=1}^n \log f(X_i \mid \theta)$$  

---

### Z-próba  
**Definíció**: Olyan statisztikai próba, amelyet általában nagy minták esetén alkalmazunk, amikor a populáció szórásnégyzete ismert.  

- **Próbastatisztika**:  
  $$Z = \frac{\bar{X} - \mu_0}{\sigma / \sqrt{n}}$$  
  ahol:  
  - \( \bar{X} \): mintátlag,  
  - \( \mu_0 \): nullhipotézis szerinti várható érték,  
  - \( \sigma \): ismert populáció szórása,  
  - \( n \): minta nagysága.  

- **Döntési szabály**:  
  Ha \( |Z| > Z_\text{kritikus} \), elutasítjuk a nullhipotézist.  

---

### T-próba  
**Definíció**: A t-próbát akkor használjuk, ha a populáció szórása nem ismert, és a minta kicsi (\(n < 30\)).  

- **Próbastatisztika**:  
  $$T = \frac{\bar{X} - \mu_0}{S / \sqrt{n}}$$  
  ahol \( S \) a minta szórása.  

- **Egy mintás T-próba**:  
  Vizsgálja, hogy a minta átlaga megegyezik-e egy adott értékkel.  

- **Kétmintás T-próba (nem kell)**.  

- **Döntési szabály**:  
  A kritikus érték alapján hasonlítjuk össze a számított \( T \)-t.  

---

### Illeszkedésvizsgálat  
**Definíció**: Megvizsgálja, hogy egy minta adott eloszlásból származik-e.  

- **Próbastatisztika**:  
  $$\chi^2 = \sum_{i=1}^k \frac{(O_i - E_i)^2}{E_i}$$  
  ahol:  
  - \( O_i \): megfigyelt gyakoriság,  
  - \( E_i \): várható gyakoriság,  
  - \( k \): osztályok száma.  

- **Döntési szabály**:  
  Ha \( \chi^2 > \chi^2_\text{kritikus} \), elutasítjuk a nullhipotézist.  

---

