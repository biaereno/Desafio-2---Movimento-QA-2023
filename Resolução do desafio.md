Bluesoft - Desafio 1

Beatriz Ereno

#C001 - Busca de solicitação de compra com filtro de loja

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja
- E clicar em "Buscar"
- Então todas as solicitações de compra da loja selecionada no filtro devem ser apresentadas na tela

#C002 - Busca de solicitação de compra com filtro de fornecedor/prestador de serviço

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar um fornecedor ou prestador de serviço
- E clicar em "Buscar"
- Então todas as solicitações de compra do fornecedor ou prestador de serviço selecionado no filtro devem ser apresentadas na tela

#C003 - Busca de solicitação de compra com filtro de status da solicitação “Pendente”

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar o status da solicitação “pendente”
- E clicar em "Buscar"
- Então todas as solicitações de compra pendentes devem ser apresentadas na tela

#C004 - Busca de solicitação de compra com filtro de status da solicitação “Aguardando aprovação”

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar o status da solicitação “Aguardando aprovação”
- E clicar em "Buscar"
- Então todas as solicitações de compra que aguardam aprovação devem ser apresentadas na tela

#C005 - Busca de solicitação de compra com filtro de status da solicitação “Aprovado”

● Dado que um usuário esteja logado no sistema

- Quando o usuário selecionar o status da solicitação “Aprovado”
- E clicar em "Buscar"
- Então todas as solicitações de compra aprovadas devem ser apresentadas na tela

#C006 - Busca de solicitação de compra com filtro de status da solicitação “Recusado”

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar o status da solicitação “Recusado”
- E clicar em "Buscar"
- Então todas as solicitações de compra recusadas devem ser apresentadas na tela

#C007 - Salvar solicitação de compra de produtos

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Produto"
- E pesquisar um produto cadastrado e selecioná-lo
- E informar a quantidade e valor unitário do produto
- E clicar em "Salvar"
- Então a solicitação de compra deve ser salva com status "pendente"

#C008 - Salvar solicitação de compra de patrimônio

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Patrimônio"
- E pesquisar um patrimônio cadastrado e selecioná-lo
- E informar a quantidade e valor unitário do patrimônio
- E clicar em "Salvar"
- Então a solicitação de compra deve ser salva com status "pendente"

#C009 - Salvar solicitação de compra com item sem cadastro

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Item sem Cadastro"
- E informar descrição, quantidade e valor unitário do item
- E clicar em "Salvar"
- Então a solicitação de compra deve ser salva com status "pendente"


#C010 - Salvar solicitação de compra com serviço

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Serviços"
- E informar a descrição, quantidade e valor unitário do serviço
- E clicar em "Salvar"
- Então a solicitação de compra deve ser salva com status "pendente"

#C011 - Inclusão de solicitação de compra de produtos

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Produto"
- E pesquisar um produto cadastrado e selecioná-lo
- E informar a quantidade e valor unitário do produto
- E clicar em "Finalizar"
- Então a solicitação de compra deve ser salva com status "Aguardando aprovação"

#C012 - Inclusão de solicitação de compra de patrimônio

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Patrimônio"
- E pesquisar um patrimônio cadastrado e selecioná-lo
- E informar a quantidade e valor unitário do patrimônio
- E clicar em "Finalizar"
- Então a solicitação de compra deve ser salva com status "Aguardando aprovação"

#C013 - Inclusão de solicitação de compra com item sem cadastro

- Dado que um usuário esteja logado no sistema
- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Item sem Cadastro"
- E informar descrição, quantidade e valor unitário do item
- E clicar em "Finalizar"
- Então a solicitação de compra deve ser salva com status "Aguardando aprovação"

#C014 - Inclusão de solicitação de compra com serviço

● Dado que um usuário esteja logado no sistema

- Quando o usuário selecionar uma loja, um fornecedor ou prestador de serviço e clicar no botão "Incluir item"
- E selecionar a opção "Serviços"
- E informar a descrição, quantidade e valor unitário do serviço
- E clicar em "Finalizar"
- Então a solicitação de compra deve ser salva com status "Aguardando aprovação"

#C015 - Aprovação de solicitação de compra

- Dado que um usuário com permissão para aprovar solicitação de compra esteja logado no sistema
- Quando o usuário visualizar uma solicitação de compra com status "aguardando aprovação"
- E clicar no botão "Aprovar solicitação"
- Então o status da solicitação deve ser alterado para "aprovada"

#C016 - Usuário sem permissão de aprovação não pode visualizar botão de aprovação

- Dado que o usuário está logado no sistema sem permissão para aprovação de solicitações
- E uma solicitação de compra foi criada e aguarda aprovação
- Quando o usuário visualiza a solicitação
- Então o sistema não exibe o botão de aprovação
- E o usuário não pode aprovar ou reprovar a solicitação

#C017 - Impressão de solicitação de compra

- Dado que o usuário está logado no sistema
- Quando o usuário visualizar uma solicitação de compra aprovada
- E clicar no botão "Imprimir solicitação"
- Então a solicitação de compra deve ser impressa com todos os dados informados, incluindo fornecedor/prestador, produto, quantidade, valor unitário e valor total

#C018 - Usuário tenta imprimir solicitação de compra pendente

- Dado que o usuário está logado no sistema
- Quando o usuário visualizar uma solicitação de compra pendente
- Então o sistema não exibe o botão de impressão
- E o usuário não pode imprimir a solicitação

#C019 - Usuário tenta imprimir solicitação de compra aguardando aprovação

- Dado que o usuário está logado no sistema
- Quando o usuário visualizar uma solicitação de compra aguardando aprovação
- Então o sistema não exibe o botão de impressão
- E o usuário não pode imprimir a solicitação

#C020 - Usuário tenta imprimir solicitação de compra recusada

- Dado que o usuário está logado no sistema
- Quando o usuário visualizar uma solicitação de compra recusada
- Então o sistema não exibe o botão de impressão
- E o usuário não pode imprimir a solicitação

