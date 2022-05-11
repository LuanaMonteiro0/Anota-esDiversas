# python - matrizes
# matriz é uma lista com outra lista dentro, pode ser escrita:
1matriz = [[a0, b0], [a1, b1], [a2, b2]]
# onde [a0, b0] é a primeira "lista" - A primeira linha da matriz, referida como "0"
# "a" se refere a coluna a da matriz
# Para endereçar um item nessa matriz pode se usar: 1matriz[1][1] e a resposta será "b1"
# Segue um exemplo comentado do uso de matrizes

matriz = []  # define a lista "primaria" onde será definida a matriz
opcao = -1
print(f"===MENU===\n"
      f"1- Cadastrar produtos\n"
      f"2- Listar Produtos \n"
      f"3- Listar detalhes dos produtos\n"
      f"4- Encontrar o preço medio dos produtos\n"
      f"5- Determine o produto mais caro\n"
      f"6- Listar fabricantes cadastrados (sem repetição)\n"
      f"7- Atualizar preços")  # print usando format pra definir o "menu"
      
while opcao != 0:  # loop para fazer o codigo rodar (tudo deve estar dentro do loop)
    opcao = int(input("Digite a opcao desejada: "))
    
    if opcao == 1:
        nome = input("Digite o nome: ")
        preco = float(input("Digite o preço: "))
        fabricante = input("Digite o fabricante: ")
        produto = []  # define a segunda lista (que vai compor cada linha da matriz acima) - a lista é zerada toda vez que 1 é selecionado
        produto.append(nome)
        produto.append(preco)
        produto.append(fabricante)
        print(produto)  # a resposta será as atribuições das variaveis nas posições: [nome, preço, fabricante]
        matriz.append(produto)  # vai colocar a lista "produto" dentro da lista "matriz"
        
    elif opcao == 2:
        for i in range(len(matriz)):  # usado para percorrer todos os itens na lista - no caso percorre todas as linhas da matriz
            print(matriz[i])

    elif opcao == 3:
        for i in range(len(matriz)):
            print(f"Produto #{i+1}\n"  # mostra um numero correspondente ao item na matriz (i+1 para começar por 1 - mais facil para entender a resposta)
                  f"Nome: {matriz[i][0]}\n"  # escreve na tela o item na posição que corresponde a linha i coluna 0
                  f"Preço: {matriz [i][1]}\n"  # escreve na tela o item na posição que corresponde a linha i coluna 1
                  f"Fabricante: {matriz [i][2]}\n\n")  # escreve na tela o item na posição que corresponde a linha i coluna 2
                  
    elif opcao == 4:
        soma = 0
        for i in range(len(matriz)):
            soma += matriz[i][1]  # soma os itens na linha i coluna 2

        if len(matriz) > 0:
            media = soma/len(matriz)
            print(f"A media dos valores é: R${media}")
        else:
            print("Não existem produtos cadastrados ")

    elif opcao == 5:
        caro = -1
        nomeCaro = "ajhsdi"
        for i in range(len(matriz)):
            if caro < matriz[i][1]:
                caro = matriz[i][1]
                nomeCaro = matriz[i][0]
        print(f"O produto mais caro é: {nomeCaro} custando R${caro}")

    elif opcao == 6:
        listaFab = []
        for i in range(len(matriz)):
            existe = False
            for j in range(len(listaFab)):
                if listaFab[j] == matriz[i][2]:
                    existe = True
            if existe == False:
                listaFab.append(matriz[i][2])

        print(f"Os fabricantes cadastrados foram:\n"
              f"{listaFab}\n")

    elif opcao ==  7:
        produto = input("Digite o produto que será atualizado? ")
        entrei = False
        for i in range(len(matriz)):
            if produto == matriz[i][0]:
                novoPreco = float(input("Digite o novo preço: "))
                matriz[i][1] = novoPreco
                entrei = True
        if entrei == False:
            print(f"Produto não cadastrado, utilize a opção 1 do menu")
