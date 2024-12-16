### Valószínűség-változó  
**Definíció**: Egy valószínűség-változó olyan függvény, amely a kísérlet kimeneteleinek halmazából a valós számok halmazába képez.  

- **Példa**:  
  Érmedobás esetén a kimenetelek \( \{Fej, Írás\} \), a valószínűség-változó hozzárendelhet:  
  \( X(Fej) = 1 \), \( X(Írás) = 0 \).  

---

### Diszkrét valószínűségi változó  
**Definíció**: Olyan valószínűségi változó, amelynek értékkészlete megszámlálható.  

- **Példa**: Egy dobókocka eredményei \( X \in \{1, 2, 3, 4, 5, 6\} \).  

---

### Eloszlás  
**Definíció**: Egy valószínűségi változó lehetséges értékeihez rendel valószínűségeket.  

#### Jellemzői:  
- **Értékkészlet**: A változó által felvehető értékek halmaza.  
- **Valószínűségeloszlás**: Az értékekhez rendelt valószínűségek.  
- **Várható érték**:  
  $$E(X) = \sum_{i} x_i \cdot P(X = x_i)$$  
- **Szórásnégyzet/variancia**:  
  $$\text{Var}(X) = E\left[(X - E(X))^2\right]$$  
- **Eloszlásfüggvény**: $$F(x) = P(X \leq x)$$  

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

### Feltételes valószínűség  
**Definíció**:  
A \( B \) esemény bekövetkezése mellett \( A \) esemény valószínűsége:  
$$P(A|B) = \frac{P(A \cap B)}{P(B)}$$  
ahol \( P(B) > 0 \).  

---

### Teljes valószínűség tétele  
**Definíció**:  
Ha az \( B_1, B_2, \dots, B_n \) események páronként kizárják egymást, és együttesen lefedik az eseménytér minden elemét:  
$$P(A) = \sum_{i=1}^n P(A|B_i) \cdot P(B_i)$$  

---

### Bayes-tétel  
**Definíció**:  
$$P(B|A) = \frac{P(A|B) \cdot P(B)}{P(A)}$$  
ahol \( P(A) > 0 \).  

---

### Eseményfüggetlenség  
**Definíció**: Két esemény független, ha:  
$$P(A \cap B) = P(A) \cdot P(B)$$  

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
