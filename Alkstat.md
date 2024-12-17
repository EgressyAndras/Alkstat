### Kombinatorika  
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

### Valószínűségi mező  
**Definíció**: Egy K kisérlet eredményei, amelyeket nem tudunk felosztani kisebb részekre **elemi eseményeknek** nevezzük. Az elemi eseményeket ***ω*** jelölik. Az összes elemi esemény halmazát **mintatérnek** (valószínűségi térnek) nevezzük. Jelölése: ***Ω***

- **Példa**:  
  Érmedobás: $Ω = \{Fej,Írás\}$

---

### Relatív gyakoriság

**Definíció:** Ha egy kisérletet *n* alkalommal ismétlünk, és $A$ esemény $k_a$ alkalommal fordul elő akkor:
$$\frac{k_a}{n}$$
nevezzük **relatív gyakoriságnak**.

---

### Eloszlás  
Ω = {$ω_1, ..., ω_N$} mintatér esetén a $p_1,...,p_N$ értékeket eloszlásnak nevezünk.
Például eloszlás lesz  
$$p_1 = 0.2 \quad p_2 = 0.5 \quad p_3 = 0.3$$

### Jellemzői
- $p_i$ számok nem negatívak
- a valószínűségek összege 1
  $$\sum_{i=1}^Np_i = 1$$

---

### Klasszikus valószínűség
**Definíció:** ha egy kisérlet lehetséges kimenetelei egyenlően valószínűek akkor A esemény valószínűsége:
$$P(A) = \frac{\text{kedvező esetek száma}} {\text{összes lehetséges eset száma}}$$

---

### Diszkrét eloszlás
$$\sum_{i=1}^\infin p_i = 1$$

---

### A valószínűség geometriai kiszámítása

$$P(A) = \lambda(\text{pont})/\lambda(\text{összes})$$
ahol $\lambda$ a hossz, terület vagy térfogat, ha egyenesen, síkon vagy térben vagyunk.

---

### Feltételes valószínűség  
**Definíció**:  
A feltételes valószínűség megmutatja $A$ valószínűségét, ha $B$ bekövetkezett:  
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$  

---

### Teljes valószínűség tétele  
**Definíció**:  
Legyen $B_1, B_2, ...$ teljes eseményrendszer. Ha $P(B_i)>0$ bármely $i$ esetén, akkor $A$:  
$$P(A) = \sum_{i=1}^n P(A|B_i) \cdot P(B_i)$$  

---

### Bayes tétel  
**Bayes formula**:  
$$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$$  
**Bayes tétel**:
$$P(B_i|A) = \frac{P(A|B_i)P(B_i)}{\sum_{j=1}^\infin P(A|B_j)P(B_j)}$$  

---

### Eseményfüggetlenség  
**Definíció**: $A$ esemény független $B$ eseménytől, ha B bekövetkezése nincs hatással $A$ valószínűségére. Azaz:  
$$P(A|B) = P(A)$$
**Definíció**: Azt mondjuk hogy $A$ és $B$ **független**, ha:
$$P(A \cap B) = P(A) \cdot P(B)$$  

---

### Páronkénti függetlenség
**Definíció**: Azt mondjuk, hogy az $A_1, A_2, ...$ események **páronként** függetlenek, ha közülük bármely kettő független, azaz:
$$P(A_iA_j) = P(A_i)P(A_j), i\not ={j}$$

**Definíció**: Azt mondjuk, hogy az $A_1, A_2, ...$ események **teljesen** függetlenek, ha bármely eseményszámra és bármely indexű eseményekre független, azaz:

$$P(A_{i_1}A_{i_2}...A_{i_k}) = P(A_{i_1})P(A_{i_2})...P(A_{i_k})$$

---
### Diszkrét eloszlások
#### Várható érték  
**Definíció**: Egy valószínűségi változó súlyozott átlaga.  
$$E(X) = \sum_{x \in X} x \cdot P(X = x)$$  

#### Szórásnégyzet (variancia)  
**Definíció**: A várható értéktől való eltérések négyzetének várható értéke.  
$$\text{Var}(X) = E(X^2) - (E(X))^2$$  

---

### Nevezetes diszkrét eloszlások  

1. **Binomiális eloszlás**:  
   - Képlete:  
     $$P(X = k) = \binom{n}{k} p^k (1-p)^{n-k}$$  
     ahol \( n \) a kísérletek száma, \( p \) az esemény bekövetkezésének valószínűsége.  
   - Várható érték: $$E(X) = n \cdot p$$  

2. **Poisson-eloszlás**:  
   - Képlete:  
     $$P(X = k) = \frac{\lambda^k e^{-\lambda}}{k!}$$  
     ahol \( \lambda \) az esemény várható értéke.  
   - Várható érték: $$E(X) = \lambda$$  

3. **Geometrikus eloszlás**:  
   - Képlete:  
     $$P(X = k) = (1-p)^{k-1} \cdot p$$  
     ahol \( p \) az esemény valószínűsége.  
   - Várható érték: $$E(X) = \frac{1}{p}$$  

---


### Eloszlásfüggvény  
**Definíció**: $$F(x) = P(X \leq x)$$  

#### Tulajdonságai:  
- Monoton növekvő.  
- $$\lim_{x \to -\infty} F(x) = 0$$, $$\lim_{x \to +\infty} F(x) = 1$$  

---

### Abszolút folytonos eloszlások  

#### Eloszlásfüggvény tulajdonságai  
$$F(b) - F(a)$$: Az érték \( [a, b] \) intervallumba esésének valószínűsége.  

#### Sűrűségfüggvény  
**Definíció**: Deriváltja az eloszlásfüggvénynek:  
$$f(x) = \frac{d}{dx} F(x)$$  

---

### Nagy számok törvénye  
**Tartalom**: Egy minta átlaga nagy mintaszám esetén közelít a várható értékhez.

---

### Mintavételi módszerek  
- **Véletlenszerű mintavétel**: Minden elemnek azonos esélye van bekerülni.  

#### Mintátlag  
- $$\bar{X}$$: Mintában szereplő elemek átlaga.  
- Tulajdonság: Mintanagyság növelésével $$\bar{X}$$ közeledik \( E(X) \)-hez.  

#### Medián  
Az az érték, amelynél a minta elemeinek fele kisebb, fele nagyobb.  

#### Kvantilis  
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

- **Sűrűségfüggvény**:  
  $$f(x) = 
  \begin{cases} 
  \frac{1}{b-a}, & \text{ha } x \in [a, b] \\
  0, & \text{egyébként} 
  \end{cases}$$  

- **Eloszlásfüggvény**:  
  $$F(x) = 
  \begin{cases} 
  0, & \text{ha } x < a \\
  \frac{x-a}{b-a}, & \text{ha } x \in [a, b] \\
  1, & \text{ha } x > b 
  \end{cases}$$  

- **Várható érték**:  
  $$E(X) = \frac{a+b}{2}$$  

- **Szórásnégyzet**:  
  $$\text{Var}(X) = \frac{(b-a)^2}{12}$$  

---

#### Normális eloszlás  
**Definíció**: Folytonos eloszlás, amelyet a \( \mu \) várható érték és a \( \sigma^2 \) szórásnégyzet paraméterez.  

- **Sűrűségfüggvény**:  
  $$f(x) = \frac{1}{\sqrt{2\pi\sigma^2}} e^{-\frac{(x-\mu)^2}{2\sigma^2}}$$  

- **Várható érték**:  
  $$E(X) = \mu$$  

- **Szórásnégyzet**:  
  $$\text{Var}(X) = \sigma^2$$  

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

