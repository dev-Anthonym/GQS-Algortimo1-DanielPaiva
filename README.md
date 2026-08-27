# Missão README

## Nível 1 - O Básico da Investigação

### Propósito do código
Esse código *`"DesafioLogica.py"`* tem como propósito principal, identificar se as seguintes frases: ***"A sacada da casa de cadasa"*** e ***"Socorram-me, subi no ônibus em Marrocos"***, são ou não um palíndromo.

### Como executar
Para executar o código *`"DesafioLogica.py"`*, siga os seguintes passos:
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

```
Teste 1: False
Teste 2: True
```

## Nível 2 - Engenharia Reversa e Análise de Comportamento

### Desvendando os método

#### Papel do bloco principal (`if __name__ == "__main__":`)
   - O trecho *`if __name__ == "__main__":`* funciona como o ponto de entrada do programa, sendo executado quando o arquivo é iniciado diretamente. Dentro dele, são definidas as duas frases de teste *`(texto1`* e *`texto2)`*, a função *`analisar()`* é chamada para cada uma delas e o resultado (*`True`* ou *`False`*) é exibido no console por meio do *`print()`*.
   
#### O que a função `analisar(entrada)` faz, linha por linha
   - **1. Verificação de entrada nula**
```python
if entrada is None:
    return False
```
Antes de processar qualquer coisa, a função verifica se *`entrada`* é *`None`* (ou seja, se não existe nenhum valor). Se for o caso, ela já retorna *`False`* imediatamente, evitando erros ao tentar processar um valor inexistente.

   - **2. Limpeza da string com expressão regular**
```python
limpa = re.sub(r'[^a-zA-Z0-9]', '', entrada).lower()
```
A função `re.sub()` substitui, em toda a string, qualquer trecho que corresponda a um padrão de expressão regular. O padrão `[^a-zA-Z0-9]` significa "qualquer caractere que **não** seja letra (a-z, A-Z) nem número (0-9)" — o `^` dentro dos colchetes indica negação.

Na prática, isso remove espaços, vírgulas, hífens e acentos (como "ô" e "ã"), substituindo-os por uma string vazia `''`. Em seguida, `.lower()` converte todo o texto restante para minúsculas, garantindo que "A" e "a" sejam tratados como o mesmo caractere na comparação final.

*Exemplo:* a frase `"Socorram-me, subi no ônibus em Marrocos"` se torna `"socorrammesubinoonibusemmarrocos"` após essa etapa.

   - **3. Inversão da string com slicing**
```python
invertida = limpa[::-1]
```
Aqui é usado o **slicing** (fatiamento), um recurso do Python para "recortar" partes de uma string. A notação *`[::-1]`* percorre todos os caracteres da string, mas de trás para frente, criando uma nova string invertida.

*Exemplo:* *`"socorrammesubinoonibusemmarrocos"`* invertida continua sendo *`"socorrammesubinoonibusemmarrocos"`* — o que já indica que é um palíndromo.

   - **4. Comparação final**
```python
return limpa == invertida
```
A função compara a string limpa com sua versão invertida:
   - Se forem **exatamente iguais** → retorna *`True`* (é um palíndromo).
   - Se forem **diferentes** → retorna *`False`* (não é um palíndromo).

### O Mistério dos Testes
| Teste   | Frase                                          | Resultado | É palíndromo? |
|---------|------------------------------------------------|-----------|----------------|
| Teste 1 | "A sacada da casa de cadasa"                   | `False`   | Não            |
| Teste 2 | "Socorram-me, subi no ônibus em Marrocos"      | `True`    | Sim            |
   - **Teste 1** usa a frase `"A sacada da casa de cadasa"`. Ao remover espaços/pontuação e comparar com sua versão invertida, o resultado não é igual, portanto o retorno é `False` (não é um palíndromo).
   - **Teste 2** usa a frase `"Socorram-me, subi no ônibus em Marrocos"`, um palíndromo clássico da língua portuguesa. Mesmo removendo a pontuação, os espaços e ignorando acentuação, a versão limpa da frase é idêntica à sua forma invertida, portanto o retorno é `True`.


## Sobre o Autor
Documentação e fork realizados por **Anthony Magalhães** como parte da atividade "Missão README", com o objetivo de investigar, executar e documentar o funcionamento do código *`DesafioLogica.py`*.
🔗 [GitHub](https://github.com/dev-Anthonym)
