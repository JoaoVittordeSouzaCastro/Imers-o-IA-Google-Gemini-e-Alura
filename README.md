# trazendo a biblioteca capaz de realizar requiosoções
import requests
import random

# criei uma variavel url que armazena o endereço com as info que desejo buscar
url = 'https://raw.githubusercontent.com/guilhermeonrails/api-imersao-ia/main/words.json'
# Faço a requisição e armazeno uma variavel chamada resposta 
resposta = requests.get(url)
# transforma a resposta em um Json
data = resposta.json()
#exibir as informações 
print(data)
# vendo como podemos acessar cada uma das informações 
# Toda lista em python começa em 0
data[0]
# criou uma variavel chamada valor secreto que armazena uma technologia aleatoria 
valor_secreto = random.choice (data)
palavra_secreta = valor_secreto ['palavra']
dica = valor_secreto ['dica']
# o f é capaz de juntar palavras e variaveis
print (f'A palavra secreta tem {len(palavra_secreta)} letras -> {dica}')
