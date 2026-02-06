# Lei de Hick-Hyman

## Conceito
Relaciona o tempo que leva para uma pessoa tomar sua decisão com base em um número de possíveis escolhas que ela possui (Hick, 1952; Hyman, 1953)[[1]](#ref-hick-hyman).

## Anotações

### Fórmulas:
O tempo médio T necessário para escolher dentre N opções, onde k é empiricamente determinado, pode ser calculado aproximademente por:

$$T = k \times \log_2(N + 1)$$, caso as opções tenham igual probabilidade;

ou

$$T = k \times \sum p_i \log_2\left(1 + \frac{1}{p_i}\right)$$, onde pi é a probabilidade da alternativa i, caso as N opções tenham probabilidades diferentes;

> Em geral, assume que k ~ 150ms.

---

- Em geral, a lei indica que uma pessoa subdivide o conjunto total de opções em categorias, eliminando aproximadamente metade das opções a cada passo, ao invés de considerar todas as escolhas que existem, uma a uma (requer um gasto enorme de tempo, tempo linear);

- Essa lei pode ser utilizada para fazer uma estimativa de quanto tempo uma pessoa levará para encontrar uma opção dentre diversas disponíveis dentro de uma interface;

> ** ATENÇÃO!**: caso não haja um princípio de organização das opções que permita o usuário eliminar metade delas rapidamente, essa lei não se aplica, pois a busca binária não pode ser realizada!

## Referências e citações
<a id="ref-hick-hyman"></a>
[1] Hick, W. E. (1952). On the rate of gain of information. Quarterly Journal of Experimental Psychology,
4(1):11--26.

## Relações

> Links para outros conceitos, capítulos ou autores.