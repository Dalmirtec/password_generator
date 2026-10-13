# Gerador de Senhas Aleatórias em Python

Este é um simples gerador de senhas desenvolvido em Python. Ele cria senhas aleatórias com letras, números e símbolos, com comprimento personalizável.

## Funcionalidades

- Geração de senhas aleatórias.
- Inclui letras (maiúsculas e minúsculas), números e pontuações.
- Pode ser adaptado para garantir ao menos um de cada tipo de caractere.

## Como usar

1. Certifique-se de ter o Python instalado em seu sistema.
2. Salve o código abaixo em um arquivo, por exemplo `gerador_senha.py`:

```python
import string
import random

def gerar_senha(comprimento):
    caracteres = string.ascii_letters + string.digits + string.punctuation
    senha = []
    for i in range(comprimento):
        caractere = random.choice(caracteres)
        senha.append(caractere)
    
    return ''.join(senha)

senha = gerar_senha(6)
print(senha)
