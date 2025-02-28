# primeiro-digito-de-cpf
Criei um algoritmo que valida o primeiro digito de um cpf baseado no algoritmo da legislação brasileira.
""" Gerar o primeiro digito do CPF"""

# Passo 1: pedir ao usuário que digite seu CPF

cpf = '80245473092'

# Passo 1.1: fatiar CPF do 0 ao 9
cpf_zeroanove = cpf[:9] #fatiamento de string


#passo 2: fazer a contagem

contador_regressivo_1 = 10
resultado = 0
for digito_1 in cpf_zeroanove: #aparecerá cada número do cpf de 0 a nove
    int_digito = int(digito_1)
    resultado += int_digito * contador_regressivo_1 
    contador_regressivo_1 -= 1
    digito_1 = (resultado * 10) % 11

#passo 3: validar o primeir digito
digito_1 = digito_1 if digito_1 <= 9 else 0 

print(digito_1)
