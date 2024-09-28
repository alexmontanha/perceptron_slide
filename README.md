# Perceptron Slide

Este repositório contém um exemplo simples de um perceptron implementado em Python.

## Descrição

O código neste repositório demonstra uma implementação básica de um perceptron, incluindo funções para calcular a entrada e a saída do perceptron. O perceptron é um tipo de rede neural artificial usada para classificação binária.

## Código

```python
def main():
    print("Hello, World!")
    print("This is the main file.")
    print("The result of the perceptron input is: ", perceptron_input([1, 2, 3], [0.1, 0.2, 0.3], 0.4))

def perceptron_input(inputs, weights, bias):
    """
    Calculate the perceptron input.

    :param inputs: List of input values
    :param weights: List of weights corresponding to the inputs
    :param bias: Bias value
    :return: The result of the weighted sum of inputs plus the bias
    """
    weighted_sum = sum(i * w for i, w in zip(inputs, weights))
    return weighted_sum + bias

def perceptron_output(inputs, weights, bias):
    """
    Calculate the perceptron output.

    :param inputs: List of input values
    :param weights: List of weights corresponding to the inputs
    :param bias: Bias value
    :return: The output of the perceptron
    """
    return 1 if perceptron_input(inputs, weights, bias) >= 0 else 0

if __name__ == "__main__":
    main()
```

## Funções

### `perceptron_input(inputs, weights, bias)`

Calcula a entrada do perceptron.

- **Parâmetros:**
  - `inputs`: Lista de valores de entrada.
  - `weights`: Lista de pesos correspondentes às entradas.
  - `bias`: Valor do bias.

- **Retorno:** A soma ponderada das entradas mais o bias.

### `perceptron_output(inputs, weights, bias)`

Calcula a saída do perceptron.

- **Parâmetros:**
  - `inputs`: Lista de valores de entrada.
  - `weights`: Lista de pesos correspondentes às entradas.
  - `bias`: Valor do bias.

- **Retorno:** 1 se a entrada do perceptron for maior ou igual a 0, caso contrário, 0.

## Execução

Para executar o código, basta rodar o arquivo principal:

```bash
python main.py
```

## Licença

Este projeto está licenciado sob os termos da licença MIT.
