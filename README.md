# Calculadora e Visualizador de Derivadas Polinomiais

Este projeto é uma aplicação em Python que calcula a derivada de polinômios recebendo apenas os coeficientes como entrada. O programa realiza o cálculo simbólico manualmente (sem usar bibliotecas prontas para isso), exibe a função na forma algébrica e gera um gráfico comparativo.

## Funcionalidades

* **Entrada Flexível:** Aceita polinômios de qualquer grau através de uma lista de coeficientes.
* **Cálculo Manual:** Implementação pura da lógica de derivação ($nx^{n-1}$), sem uso de `SymPy` ou funções prontas.
* **Formatação Algébrica:** Converte a lista de números em uma string legível (ex: `2x^3 - 5x + 7`).
* **Visualização Gráfica:** Plota o polinômio original e sua derivada no mesmo gráfico para análise de comportamento (máximos, mínimos e inclinação).

## Tecnologias Utilizadas

* **Python 3.x**
* **Matplotlib:** Para a plotagem dos gráficos.
* **NumPy:** Apenas para a geração de vetores numéricos para o eixo X (plotagem).

## Pré-requisitos e Instalação

Você precisará ter o Python instalado. Em seguida, instale as dependências necessárias executando:

```bash
pip install matplotlib numpy
```

## Como Usar

1.  Execute o script principal
2.  Quando solicitado, digite os coeficientes do polinômio separados por espaço, começando do maior grau para o menor (termo independente).

### Exemplos de Entrada

| Polinômio Desejado | Entrada no Console |
| :--- | :--- |
| $2x^3 - 5x + 7$ | `2 0 -5 7` |
| $x^2 - 4x + 4$ | `1 -4 4` |
| $-3x + 2$ | `-3 2` |
| $x^4 - 10$ | `1 0 0 0 -10` |

## Lógica Implementada

O núcleo do projeto baseia-se na **Regra do Tombo** (Power Rule):
Dada uma função $f(x) = ax^n$, sua derivada é $f'(x) = a \cdot n \cdot x^{n-1}$.

O algoritmo percorre a lista de coeficientes:

1.  Identifica o grau atual baseado na posição do índice.
2.  Multiplica o coeficiente pelo grau atual.
3.  Reduz o grau em 1 para o próximo termo.
4.  Ignora o termo independente (onde grau = 0), pois a derivada de constante é zero.

## 📷 Exemplo de Saída

**Terminal:**

```text
=== Calculadora de Derivada de Polinômios ===
Digite os coeficientes separados por espaço.
Coeficientes: 2 0 -5 7
------------------------------
Polinômio Original: f(x) = 2x^3 - 5x + 7
Derivada Calculada: f'(x) = 6x^2 - 5
------------------------------
```

**Gráfico Gerado:**
O programa abrirá uma janela contendo:

  * **Linha Azul:** A curva do polinômio original.
  * **Linha Tracejada Vermelha:** A curva da derivada.

## 📝 Autor

### Aluno: Natan S. Rodrigues

Desenvolvido para fins educacionais, demonstrando a intersecção entre Álgebra Computacional e Programação.

