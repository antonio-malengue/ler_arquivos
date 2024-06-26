# Leitor de Arquivo CSV

Este é um pequeno script em Python que lê dados de um arquivo CSV e exibe seu conteúdo.

## Funcionalidades

- Lê dados de um arquivo CSV.
- Exibe os dados lidos do arquivo CSV.

## Como Usar

1. Faça o download ou clone este repositório em sua máquina local.
2. Certifique-se de ter o Python instalado em sua máquina.
3. Execute o script Python digitando `python nome_do_arquivo.py` e pressione Enter.
4. O script lerá os dados do arquivo CSV especificado e os exibirá no console.

## Exemplo de Uso

```python
import csv

# Caminho para o arquivo CSV
caminho_arquivo = 'arquivo.csv'

# Inicializa uma lista vazia para armazenar os dados
dados = []

# Usa o gerenciador de contexto `with` para abrir o arquivo
with open(caminho_arquivo, mode='r', encoding='utf-8') as arquivo:
    # Cria um objeto leitor de CSV
    leitor_csv = csv.DictReader(arquivo)
    
    # Itera sobre as linhas do arquivo CSV
    for linha in leitor_csv:
        # Adiciona cada linha (um dicionário) à lista de dados
        dados.append(linha)

# Exibe os dados lidos do arquivo CSV
for registro in dados:
    print(registro)
