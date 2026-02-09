# Lei de Fitts

## Conceito
Relaciona o tempo que leva para uma pessoa apontar para algo com o tamanho do objeto-alvo e com a distância entre a mão da pessoa e esse objeto-alvo. (Hick, 1952; Hyman, 1953)[[1]](#ref-fitts).

## Anotações

### Fórmulas:
O tempo médio necessário para apontar para um alvo pode ser calculado por:

$$
T = k \times \log_2\left(\frac{D}{S} + 0.5\right)
$$

**Onde:**
- $T$ = tempo
- $k$ = constante
- $D$ = distância
- $S$ = tamanho

Variações da fórmula (utilizadas para modelar o tempo que leva para um mouse ou outro dispositivo de entrada semelhante atingir um objetivo numa tela):

$$
T = a + b \cdot \log_2\left(\frac{2D}{S}\right)
$$

e

$$
T = a + b \cdot \log_2\left(\frac{D}{S} + 1\right)
$$

onde $a$ e $b$ são constantes determinadas empiricamente.

> Assume que k ~ 100ms, pode variar conforme o tipo de dispositivo de entrada utilizado.

---

- Esta lei é importante para aplicações em que o desempenho é crítico;

- Ajuda na decisão de tamanhos e localização de elementos de interface para interação do usuário com o sistema.

## Referências e citações
<a id="ref-fitts"></a>
[1] Fitts, Paul M. (1954). The information capacity of the human motor system in controlling the amplitude
of movement. Journal of Experimental Psychology, 47(6):381--391.

## Relações

> Links para outros conceitos, capítulos ou autores.