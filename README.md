# projeto-.py

# ==========================================
# 1. Nosso Primeiro Programa
# ==========================================
print("hello world")


# ==========================================
# 2. Criando Variáveis de Tipos Diferentes
# ==========================================
x = 10
nome = 'Anderson'
nota = 8.75
fez_inscricao = True

print(x)
print(nome)
print(nota)
print(fez_inscricao)

print(type(x))
print(type(nome))
print(type(nota))
print(type(fez_inscricao))


# ==========================================
# 3. Entrada de Dados e Cálculo de Média
# ==========================================
nome = input('Digite seu nome: ')
print(f"Olá {nome}, bem-vindo à disciplina de programação!")

NOTA_1 = int(input('DIGITE A NOTA 1: '))
NOTA_2 = int(input('DIGITE A NOTA 2: '))
NOTA_3 = int(input('DIGITE A NOTA 3: '))
NOTA_4 = int(input('DIGITE A NOTA 4: '))

media = (NOTA_1 + NOTA_2 + NOTA_3 + NOTA_4) / 4
print(f"Sua média é: {media}")

if media >= 7:
    situacao = "Aprovado"
else:
    situacao = "Reprovado"

print(f"Situação: {situacao}")


# ==========================================
# 4. Operadores Comparativos e Lógicos
# ==========================================
print(10 > 5)
print(5 > 10)
print(7 == 7)
print(7 != 7)

# Guardando informações booleanas
idade = 18
e_maior_de_idade = idade >= 18
print(f"É maior de idade? {e_maior_de_idade}")

print(True and True)
print(True and False)


# ==========================================
# 5. Estruturas Condicionais (if / elif / else)
# ==========================================
idade_usuario = int(input('Digite sua idade: '))

if idade_usuario < 18:
    print('Menor de idade')
elif idade_usuario >= 18 and idade_usuario < 60:
    print('Maior de idade')
else:
    print('Idoso')


idade_filme = int(input('Digite a sua idade para recomendação de filme: '))

if idade_filme < 12:
    print('Recomendamos o filme infantil 1')
elif 12 <= idade_filme < 18:
    print('Recomendamos o filme infantil 2')
else:
    print('Recomendamos o filme infantil 3')


quantidade_de_ingresso = 10
if quantidade_de_ingresso > 0:
    print('Pode comprar ingresso')
else:
    print('Não temos ingressos')


# ==========================================
# 6. Estruturas de Repetição (for e while)
# ==========================================
numeros = [1, 2, 3, 4, 5, 6, 7]

for n in numeros:
    print(f'Camisetas: {n}')

print(type(numeros))


# Loop para verificar se números são pares ou ímpares
numero = int(input('Digite um número para verificar (ou 0 para sair): '))

while numero != 0:
    if numero % 2 == 0:
        print('O número é par')
    else:
        print('O número é ímpar')
    numero = int(input('Digite um número (ou 0 para sair): '))


# Laço com range
for x in range(1, 15, 3):
    print(f"Valor do range: {x}")


# Classificação de filmes
filmes = ["Filme 1", "Filme 2", "Filme 3", "Filme 4", "Filme 5"]

print("\n--- Bem-vindo à classificação de filmes ---")
print("Você tem cinco filmes para classificar.")
print("Digite '0' a qualquer momento para parar.\n")

for item_filme in filmes:
    classificacao = input(f"Como você classifica '{item_filme}' de 1 a 5 (ou 0 para parar): ")

    if classificacao == '0':
        print("Que pena que interrompeu!")
        break

    classificacao_int = int(classificacao)
    if classificacao_int < 1 or classificacao_int > 5:
        print("Nota inválida! Tente com notas entre 1 e 5.")
    else:
        print(f"Você classificou '{item_filme}' com {classificacao_int} estrelas.\n")

print("Obrigado por avaliar!")


# ==========================================
# 7. Listas e Funções
# ==========================================
lista_numeros = [1, 2, 3, 4, 5]
comprimento = len(lista_numeros)
print(f"Comprimento da lista: {comprimento}")


def soma(a, b):
    resultado = a + b
    return resultado


resultado_soma = soma(5, 6)
print(f"Resultado da soma: {resultado_soma}")


def e_par(num):
    return num % 2 == 0


numero_longo = 6544312790909776675344343
teste = e_par(numero_longo)
print(f"O número longo é par? {teste}")


# Função Lambda
media_valor = 8.7741212358909766455546564
arredondar_media = lambda val: round(val, 2)

media_arredondada = arredondar_media(media_valor)
print(f"Média arredondada: {media_arredondada}")
