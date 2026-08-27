# Missão README

## Nível 1 - O Básico da Investigação

### Propósito da classe
Essa classe *`"DesafioLogica.py"`* tem como propósito principal, identificar se as seguintes frases: ***"A sacada da casa de cadasa"*** e ***"Socorram-me, subi no ônibus em Marrocos"***, são ou não um palíndromo.

### Como executar
Para executar o código da classe *`"DesafioLogica.py"`*, siga os seguintes passos:
1. Certifique-se de ter o Python 3 instalado na sua máquina.
   - Verifique com o comando:
   - *`python3 --version`*

2. Clone o repositório:
   - Exemplo: *"git clone [https://github.com/dev-Anthonym/gqs-algoritmo-01-py.git](https://github.com/dev-Anthonym/gqs-algoritmo-01-py.git)"*

3. Acesse a pasta do projeto:
   - cd gqs-algoritmo-01-py

4. Execute o script:
   - python3 DesafioLogica.py

### Exemplo de saída
Ao executar o comando *`python DesafioLogica.py`*, o console exibe o seguinte resultado:

\`\`\`
Teste 1: False
Teste 2: True
\`\`\`

**Explicação dos resultados:**

- **Teste 1** usa a frase *`"A sacada da casa de cadasa"`*. Ao remover
  espaços/pontuação e comparar com sua versão invertida, o resultado
  não é igual, portanto o retorno é *`False`* (não é um palíndromo).

- **Teste 2** usa a frase *`"Socorram-me, subi no ônibus em Marrocos"`*,
  um palíndromo clássico da língua portuguesa. Mesmo removendo a
  pontuação, os espaços e ignorando acentuação, a versão limpa da
  frase é idêntica à sua forma invertida, portanto o retorno é *`True`*.
