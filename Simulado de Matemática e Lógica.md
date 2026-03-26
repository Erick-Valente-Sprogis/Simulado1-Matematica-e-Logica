
> Explicações detalhadas para cada questão, do jeito mais simples possível.
---

## Questão 1 — Quantas soluções tem x + y + z = 7?

**O que a questão pede?** Quantas formas diferentes existem de escolher 3 números (x, y, z) que, somados, dão 7? Os números precisam ser inteiros não negativos (0, 1, 2, 3...).

**Pensa assim:** Imagina que você tem **7 bolinhas** e **3 caixinhas** (x, y, z). Você precisa distribuir essas 7 bolinhas entre as 3 caixinhas. Uma caixinha pode ficar vazia (por isso "não negativo" — pode ser zero).

**O truque das divisórias:** Para contar essas distribuições, usamos um macete matemático: imagina as 7 bolinhas em fila, e você coloca **2 divisórias** entre elas para separar em 3 grupos.

```
Ex: O O | O O O | O O  → x=2, y=3, z=2
    O O O O O O O | |  → x=7, y=0, z=0
```

Você tem 7 bolinhas + 2 divisórias = **9 objetos no total**. A pergunta vira: de quantas formas posso escolher **2 posições** entre 9 para colocar as divisórias?

Isso é uma **combinação**: C(9,2)

**Calculando C(9,2):**

```
C(9,2) = 9! / (2! × 7!)
       = (9 × 8) / (2 × 1)
       = 72 / 2
       = 36
```

### Por que o fatorial "virou" só 9 × 8 e 2 × 1?

Fatorial é só multiplicar o número por todos os inteiros menores até chegar no 1:

```
7! = 7 × 6 × 5 × 4 × 3 × 2 × 1
9! = 9 × 8 × 7 × 6 × 5 × 4 × 3 × 2 × 1
2! = 2 × 1
```

Agora olha o que acontece na conta completa:

```
        9 × 8 × 7 × 6 × 5 × 4 × 3 × 2 × 1
       ─────────────────────────────────────
       (2 × 1) × (7 × 6 × 5 × 4 × 3 × 2 × 1)
```

O **7!** aparece tanto em cima quanto embaixo — então ele se **cancela**, como qualquer número dividido por ele mesmo (que sempre dá 1).

O que sobra depois do cancelamento:

```
9 × 8
───── = 72 / 2 = 36
2 × 1
```

> **Resumindo:** o 7! sumiu porque estava igual em cima e embaixo da fração. Esse cancelamento é justamente o motivo pelo qual a fórmula da combinação foi inventada assim — ela sempre gera esse corte, tornando a conta muito mais fácil!

✅ **Resposta: C — 36**

---

## Questão 2 — Mega Sena com 20 números

**O que a questão pede?** Na Mega Sena normal tem 60 números. A questão pergunta: se em vez de 60, só tivesse números de 1 a 20, quantas apostas diferentes seriam possíveis?

**Conceito importante — Combinação vs Arranjo:**

- **Arranjo** → a ordem **importa** (1,2,3 é diferente de 3,2,1)
- **Combinação** → a ordem **não importa** (1,2,3 é igual a 3,2,1)

**Na Mega Sena, a ordem importa?** Não! Se você apostou 5, 12, 33... não importa em que ordem os números saem. Por isso usamos **Combinação**.

Você está escolhendo **6 números** de um total de **20**. Isso se escreve como: **C₆²⁰** (lê-se: combinação de 20, 6 a 6)

### Como funciona o C₆²⁰ na prática?

A fórmula da combinação é sempre:

```
        n!
Ck^n = ────────────
       k! × (n-k)!
```

Onde:

- **n** = total de opções (20 números disponíveis)
- **k** = quantos você vai escolher (6 números)

Aplicando na questão:

```
         20!            20!
C6^20 = ───────────── = ───────────
        6! × (20-6)!   6! × 14!
```

O **14!** aparece em cima (no final do 20!) e embaixo — então ele se **cancela**, igual ao que aconteceu na Questão 1. Sobra:

```
20 × 19 × 18 × 17 × 16 × 15
────────────────────────────
    6 × 5 × 4 × 3 × 2 × 1
```

Calculando em cima:

```
20 × 19 = 380
380 × 18 = 6.840
6.840 × 17 = 116.280
116.280 × 16 = 1.860.480
1.860.480 × 15 = 27.907.200
```

Calculando embaixo:

```
6! = 6 × 5 × 4 × 3 × 2 × 1 = 720
```

Resultado final:

```
27.907.200 ÷ 720 = 38.760 apostas possíveis
```

> A questão só pede como se **escreve** essa conta, não o resultado final — por isso a resposta é **C₆²⁰**. Mas agora você sabe calcular também! 😊

✅ **Resposta: C — C₆²⁰**

---

## Questão 3 — União dos conjuntos A e B

**O que a questão pede?** Dados dois conjuntos de números em uma reta, encontrar a união (A ∪ B), ou seja, **tudo que está em A, em B, ou nos dois**.

**Primeiro, entende a notação:**

- Colchete `[` ou `]` = o número **está incluído** (ponto cheio ●)
- Chave invertida `]` ou `[` = o número **não está incluído** (ponto vazio ○)

**Visualizando na reta numérica:**

```
A = ]1; 3/2[  →  vai de 1 até 1,5   (sem incluir nenhum dos dois)
B = [-1; 5/3] →  vai de -1 até 1,67 (incluindo os dois)
```

Desenhando na reta:

```
    -1         1    1,5  1,67
     [----B---------●----]
               (----A---)
```

**A união é tudo que aparece em pelo menos um dos dois:**

```
    -1                  1,67
     [--------A∪B--------]
```

A união começa em **-1** (incluído, veio do B) e vai até **5/3** (incluído, veio do B).

✅ **Resposta: A — [-1; 5/3]**

---

## Questão 4 — 8 pessoas em fila, 2 devem ficar juntas

**O que a questão pede?** De quantas formas 8 pessoas podem se organizar em fila, desde que 2 pessoas específicas fiquem sempre lado a lado?

**Passo 1 — Junta as duas pessoas num "bloco":** Se Ana e Bia sempre ficam juntas, trata elas como **uma pessoa só** (um bloco). Agora você tem: **7 "pessoas"** para organizar (o bloco + as outras 6).

**Passo 2 — Quantas filas com 7 "pessoas"?** 7 pessoas em fila = 7! (lê-se "7 fatorial")

```
7! = 7 × 6 × 5 × 4 × 3 × 2 × 1 = 5.040
```

**Passo 3 — E dentro do bloco?** Ana e Bia podem se organizar de 2 formas:

- Ana à esquerda, Bia à direita
- Bia à esquerda, Ana à direita

Então multiplica por **2**.

**Total:**

```
5.040 × 2 = 10.080
```

✅ **Resposta: C — 10.080**

---

## Questão 5 — Verdadeiro ou Falso sobre o plano cartesiano

**Revisando os quadrantes:**

```
        y
        |
2º(−,+) | 1º(+,+)
--------O--------→ x
3º(−,−) | 4º(+,−)
        |
```

- No eixo x: y = 0
- No eixo y: x = 0

### Como funciona o (x, y)?

Todo ponto é escrito como **(x, y)** — sempre nessa ordem. O **primeiro número é sempre x** e o **segundo é sempre y**. Isso nunca muda!

Pensa no plano cartesiano como uma cidade com ruas:

- O **eixo x** é a **rua horizontal** (vai para os lados)
- O **eixo y** é a **rua vertical** (vai para cima e para baixo)

```
        y
        |
    1   ● ← (0,1): fica NA rua vertical
  ──────O──────────────→ x
             1
             ● ← (1,0): fica NA rua horizontal
```

> Quando **x = 0**, o ponto está em cima do **eixo y** (rua vertical). Quando **y = 0**, o ponto está em cima do **eixo x** (rua horizontal).

|Ponto|x|y|Onde fica?|
|---|---|---|---|
|(0,1)|0|1|Anda 0 para o lado, sobe 1 → **no eixo y**|
|(1,0)|1|0|Anda 1 para o lado, sobe 0 → **no eixo x**|

São pontos em lugares **completamente diferentes** — por isso a ordem do (x, y) sempre importa!

---

**Analisando cada sentença:**

**I. (0,1) = (1,0)?** O ponto (0,1) fica no **eixo y** (x=0, y=1). O ponto (1,0) fica no **eixo x** (x=1, y=0). São pontos completamente diferentes! → ❌ **FALSO**

**J. (-1, 4) está no 3º quadrante?** O 3º quadrante precisa de x negativo **E** y negativo. Aqui x=-1 (negativo ✓) mas y=4 (positivo ✗). Esse ponto está no **2º quadrante**! → ❌ **FALSO**

**K. (2, 0) está no eixo y?** Para estar no eixo y, precisaria ter x=0. Mas x=2 ≠ 0. Esse ponto está no **eixo x**! → ❌ **FALSO**

**L. (-3, -2) está no 3º quadrante?** x=-3 (negativo ✓) e y=-2 (negativo ✓). Dois negativos = 3º quadrante! → ✅ **VERDADEIRO**

**Conclusão:** I, J, K são falsas e L é verdadeira.

✅ **Resposta: A — (I);(J);(K) são falsas e (L) é verdadeira**

---

## Questão 6 — Quantas vezes o nível atingiu 40m?

**O que a questão pede?** Olhando o gráfico do nível de água da barragem, quantas vezes a linha do gráfico passou pelo valor 40?

**Como pensar:** Imagina que você desenha uma linha horizontal no valor 40. Toda vez que o gráfico **cruza** essa linha, conta um.

O gráfico mostra que a água:

1. Começa alto (~100m)
2. **Desce** passando por 40 → **1ª vez**
3. Chega perto de 10m (mínimo)
4. **Sobe** passando por 40 novamente → **2ª vez**
5. Volta a subir para ~90m

A linha de 40m foi cruzada **2 vezes**.

✅ **Resposta: B — 2**

---

## Questão 7 — Vagas fechadas no 1º semestre

**O que a questão pede?** Baseado no gráfico, qual afirmativa sobre a indústria paulista em 1998 é **correta**?

**Lendo o gráfico mês a mês (aproximado):**

```
Jan: ~25.000
Fev: ~20.000
Mar: ~15.000
Abr: ~12.000
Mai: ~8.000
Jun: ~5.000
```

**Verificando a alternativa C:** "No primeiro semestre, foram fechadas mais de 62.000 vagas."

Somando:

```
25.000 + 20.000 + 15.000 + 12.000 + 8.000 + 5.000 = 85.000
```

85.000 > 62.000 ✅

> As outras alternativas falam em "desempregados" — mas o gráfico mostra vagas **fechadas**, não desempregados diretamente. Isso as torna incorretas.

✅ **Resposta: C — No primeiro semestre, foram fechadas mais de 62.000 vagas**

---

## Questão 8 — Domínio de f(x) = 1/(x−2)

**O que é domínio?** É o conjunto de todos os valores de x que você **pode** colocar na função sem dar erro.

**Qual é o "erro" aqui?** Divisão por zero! Em matemática, dividir por zero é **impossível**.

**Quando o denominador vira zero?**

```
x - 2 = 0
x = 2
```

Quando x=2, a função fica 1/0 → impossível! ❌

### Por que f(x) = 1/0 quando x = 2?

A função é **f(x) = 1/(x − 2)**. O **x** é só um "espaço em branco" esperando um número. Quando você coloca x = 2, é como substituir esse espaço em branco pelo número 2:

```
f(x) = 1 / (x  − 2)
            ↓
f(2) = 1 / (2  − 2)
            ↓
f(2) = 1 / (0)
            ↓
f(2) = 1/0  → impossível! ❌
```

O **x − 2** é a conta que fica no denominador (embaixo da fração). Quando x = 2, essa conta vira **2 − 2 = 0**, e aí o denominador fica zero.

> **Por que dividir por zero é impossível?** Pensa: 6 ÷ 2 = 3 porque 3 × 2 = 6. Agora tenta 1 ÷ 0 = ? Para isso funcionar, precisaria existir um número que multiplicado por 0 desse 1. Mas **qualquer número × 0 = 0**. Não existe nenhum número que resolva isso — por isso é impossível!

---

### O x − 2 "desaparece" quando encontramos x = 2?

Não! São duas etapas separadas:

**Etapa 1** — Resolver x − 2 = 0 só para **descobrir** qual valor causa o problema:

```
x - 2 = 0
x = 2        ← "o problema acontece quando x for 2"
```

**Etapa 2** — Substituir esse valor na função original para **confirmar**:

```
f(x) = 1 / (x - 2)
f(2) = 1 / (2 - 2)   ← o (x - 2) continua lá inteiro!
f(2) = 1 / 0         ← confirma o problema
```

O x − 2 **nunca desaparece** — ele é parte da função para sempre!

---

### De onde vem o +2 usado para resolver x − 2 = 0?

O -2 que está em **(x - 2)** veio da **função original** — ele sempre esteve lá. Para descobrir o x, precisamos **deixá-lo sozinho**. Como tem um -2 atrapalhando, somamos **+2 nos dois lados** para cancelar:

```
x - 2     = 0
x - 2 + 2 = 0 + 2    ← somamos +2 nos dois lados
x + 0     = 2
x         = 2
```

O -2 e o +2 se encontram e **se cancelam** (−2 + 2 = 0), deixando o x sozinho. Não é o mesmo -2 sendo reutilizado — é um +2 novo criado justamente para eliminar o -2 que já estava lá.

> **Analogia:** imagina que você deve R$2 (o -2). Para ficar zerado, alguém te dá R$2 (o +2). Os dois se cancelam e você fica sem dívida. O R$2 que pagou veio de fora, não era o mesmo da dívida! 💸

---

**Portanto:** x pode ser qualquer número real, **exceto 2**.

Isso se escreve como: **ℝ \ {2}** (lê-se: "reais menos o conjunto {2}")

✅ **Resposta: B — ℝ \ {2}**

---

## Questão 9 — Domínio do modelo de lucro

**O que a questão pede?** A empresa disse que o modelo só funciona quando:

- Unidades vendidas **≥ 100** (maior ou **igual** a 100 — inclui o 100)
- Unidades vendidas **< 500** (menor que 500 — **não** inclui o 500)

**Traduzindo para intervalo:**

```
100 ≤ unidades < 500
```

Na notação de intervalos: **[100, 500)**

- O `[` antes do 100 = **inclui** o 100
- O `)` depois do 500 = **não inclui** o 500

Isso é exatamente o que a alternativa C diz: _"entre 100 e 500, incluindo 100, mas não incluindo 500."_

✅ **Resposta: C**

---

## Questão 10 — Imagem de uma função definida por partes

**O que é imagem?** São todos os **resultados possíveis** que a função pode produzir.

**O que é uma função definida por partes?** É uma função que tem **regras diferentes dependendo do valor de x**. Imagina um estacionamento:

- Até 1 hora: paga R$5
- De 1h a 3h: paga R$10
- Acima de 3h: paga R$15

Cada faixa tem sua própria regra. Essa questão funciona igual!

---

As 3 regras da função:

```
         ┌  −x − 1,    se x ≤ −1        (Regra 1)
f(x) =   │  −x² + 1,   se −1 < x < 1   (Regra 2)
         └  x − 1,     se x ≥ 1         (Regra 3)
```

---

### Regra 1 — f(x) = −x − 1, para x ≤ −1

Essa regra só vale quando x é **−1 ou menor** (−1, −2, −3...).

|x|Conta|f(x)|
|---|---|---|
|−1|−(−1) − 1 = 1 − 1|**0**|
|−2|−(−2) − 1 = 2 − 1|**1**|
|−3|−(−3) − 1 = 3 − 1|**2**|
|−10|−(−10) − 1 = 10 − 1|**9**|

Quanto mais negativo o x, **maior** o resultado. O menor resultado possível é **0** (quando x = −1).

→ Imagem da Regra 1: **[0, +∞)**

---

### Regra 2 — f(x) = −x² + 1, para −1 < x < 1

Essa regra só vale quando x está **entre −1 e 1**, sem incluir os dois extremos. (ou seja: −0.9, −0.5, 0, 0.5, 0.9... mas nunca −1 ou 1 exatos)

|x|Conta|f(x)|
|---|---|---|
|0|−(0²) + 1 = 0 + 1|**1** ← maior valor!|
|0.5|−(0.25) + 1|**0.75**|
|−0.5|−(0.25) + 1|**0.75**|
|0.9|−(0.81) + 1|**0.19**|
|−0.9|−(0.81) + 1|**0.19**|

O **maior valor é 1** (quando x = 0) e vai chegando perto de 0 nas bordas, mas **nunca chega em 0** de fato (porque −1 e 1 não estão incluídos).

→ Imagem da Regra 2: **(0, 1]**

---

### Regra 3 — f(x) = x − 1, para x ≥ 1

Essa regra só vale quando x é **1 ou maior** (1, 2, 3...).

|x|Conta|f(x)|
|---|---|---|
|1|1 − 1|**0**|
|2|2 − 1|**1**|
|3|3 − 1|**2**|
|10|10 − 1|**9**|

O menor resultado é **0** (quando x = 1) e vai crescendo sem parar.

→ Imagem da Regra 3: **[0, +∞)**

---

### Juntando tudo (união das 3 imagens):

```
Regra 1 →  [0, +∞)   =  0, 1, 2, 3, 4... até infinito
Regra 2 →  (0, 1]    =  0.1, 0.5, 0.9, 1  (o 0 não entra)
Regra 3 →  [0, +∞)   =  0, 1, 2, 3, 4... até infinito
```

Como a Regra 1 e a Regra 3 já cobrem **[0, +∞)**, a Regra 2 não acrescenta nada novo.

```
[0,+∞) ∪ (0,1] ∪ [0,+∞) = [0, +∞)
```

Todos os valores a partir de 0 (incluindo) até infinito.

✅ **Resposta: C — [0, +∞)**

---

_Documento gerado como material de estudo e revisão._
