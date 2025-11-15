# Roteiro Detalhado para Gravação de Vídeos de Execução de Testes

**Objetivo:** Fornecer um guia passo a passo para a gravação dos vídeos de evidência, garantindo que todos os cenários de teste documentados (CRUD, Positivos e Negativos) sejam cobertos de forma clara e objetiva.

**Instruções de Gravação:**
1.  A gravação deve ser contínua para cada rotina, minimizando cortes.
2.  Utilizar um ponteiro do mouse visível ou destaque visual para indicar os campos e botões clicados.
3.  A voz (opcional) ou legendas devem descrever o ID do Cenário de Teste que está sendo executado e o resultado esperado/obtido.
4.  Certificar-se de que as mensagens de sucesso e erro do sistema estejam visíveis na gravação.

---

## 1. Rotina: Cadastro de Produtos (Inventário de Estoque)

| ID do Cenário | Tipo | Ação no Vídeo | Foco da Gravação |
| :--- | :--- | :--- | :--- |
| **PROD-C-001** | Positivo | **Criação de Produto com Dados Válidos** | Mostrar o preenchimento dos campos, o clique em "Salvar" e a mensagem de sucesso. **Evidenciar o produto criado na consulta.** |
| **PROD-C-002** | Negativo | **Criação de Produto com Campo Obrigatório Vazio** | Tentar salvar com o campo "Nome do Produto" vazio. **Focar na mensagem de erro do sistema.** |
| **PROD-C-003** | Negativo | **Criação de Produto com Código Duplicado** | Tentar salvar um novo produto com o mesmo código do PROD-C-001. **Focar na mensagem de erro de duplicidade.** |
| **PROD-R-001** | Positivo | **Consulta de Produto Existente** | Acessar a tela de consulta e pesquisar pelo produto criado (PROD-C-001). **Focar na exibição correta dos dados.** |
| **PROD-R-002** | Negativo | **Consulta de Produto Inexistente** | Pesquisar por um código/nome aleatório e inexistente. **Focar na lista vazia ou mensagem "Não Encontrado".** |
| **PROD-U-001** | Positivo | **Atualização de Preço de Venda** | Abrir o produto PROD-C-001, alterar o preço, salvar. **Focar na mensagem de sucesso e na confirmação do novo preço na consulta.** |
| **PROD-U-002** | Negativo | **Atualização com Campo Obrigatório Vazio** | Abrir o produto PROD-C-001, apagar o nome e tentar salvar. **Focar na mensagem de erro.** |
| **PROD-D-001** | Positivo | **Exclusão de Produto sem Vínculos** | Criar um produto temporário (sem vínculos) e excluí-lo. **Focar na confirmação da exclusão e na ausência do produto na consulta.** |
| **PROD-D-002** | Negativo | **Exclusão de Produto com Vínculos** | Tentar excluir o produto PROD-C-001 (que será usado em vendas). **Focar na mensagem de erro de vínculo.** |

---

## 2. Rotina: Cadastro de Clientes

| ID do Cenário | Tipo | Ação no Vídeo | Foco da Gravação |
| :--- | :--- | :--- | :--- |
| **CLI-C-001** | Positivo | **Criação de Cliente com Limite de Crédito** | Cadastrar um cliente e definir um limite de crédito (ex: R$ 100,00). **Focar no campo de limite e na mensagem de sucesso.** |
| **CLI-C-002** | Positivo | **Criação de Cliente com Dependente** | Acessar a aba "Dependentes" do cliente criado e cadastrar um dependente. **Focar na vinculação do dependente.** |
| **CLI-C-003** | Negativo | **Criação de Cliente com CPF Duplicado** | Tentar cadastrar um novo cliente usando o mesmo CPF do CLI-C-001. **Focar na mensagem de erro de duplicidade de CPF.** |
| **CLI-R-001** | Positivo | **Consulta de Cliente e Dependentes** | Consultar o cliente CLI-C-001 e navegar até a aba "Dependentes". **Focar na exibição dos dados do cliente e do dependente.** |
| **CLI-U-001** | Positivo | **Aumento do Limite de Crédito** | Abrir o cliente CLI-C-001 e aumentar o limite de crédito (ex: para R$ 200,00). **Focar na atualização do valor.** |
| **CLI-D-001** | Positivo | **Exclusão de Dependente** | Excluir o dependente cadastrado no CLI-C-002. **Focar na confirmação e na remoção do dependente da lista.** |
| **CLI-D-002** | Negativo | **Exclusão de Cliente com Vendas Vinculadas** | Tentar excluir o cliente CLI-C-001 (que será usado em vendas). **Focar na mensagem de erro de vínculo.** |

---

## 3. Rotina: Pedidos/Venda

| ID do Cenário | Tipo | Ação no Vídeo | Foco da Gravação |
| :--- | :--- | :--- | :--- |
| **VEN-C-001** | Positivo | **Venda Completa com Pagamento à Vista** | Iniciar venda, adicionar produto PROD-C-001, finalizar, selecionar pagamento à vista. **Focar na finalização e na baixa de estoque.** |
| **VEN-C-002** | Positivo | **Venda com Parcelamento (Contas a Pagar)** | Iniciar venda, adicionar produto, finalizar, selecionar pagamento parcelado (ex: 5x). **Focar na tela de parcelamento e na mensagem de sucesso.** |
| **VEN-C-003** | Negativo | **Venda com Produto sem Estoque** | Tentar adicionar um produto com estoque zero. **Focar no alerta de estoque insuficiente.** |
| **VEN-C-004** | Negativo | **Venda para Cliente com Limite Excedido** | Usar o cliente CLI-C-001 (limite R$ 200,00) e tentar finalizar uma venda a prazo de R$ 250,00. **Focar na mensagem de erro/alerta de limite excedido.** |
| **VEN-U-001** | Positivo | **Alteração de Quantidade de Item Antes de Finalizar** | Iniciar uma venda, adicionar um item, alterar a quantidade do item antes de finalizar. **Focar no recálculo do valor total.** |
| **VEN-D-001** | Positivo | **Cancelamento de Venda Não Finalizada** | Iniciar uma venda, adicionar itens e, antes de finalizar, cancelar/excluir o pedido. **Focar na confirmação do cancelamento.** |

---

## 4. Rotina: Contas a Pagar (Pagamento de Parcelas)

*Pré-condição: Utilizar as parcelas geradas pelo cenário **VEN-C-002**.*

| ID do Cenário | Tipo | Ação no Vídeo | Foco da Gravação |
| :--- | :--- | :--- | :--- |
| **PAG-U-001** | Positivo | **Pagamento Total de Parcela** | Acessar Contas a Pagar, selecionar a **primeira parcela** do VEN-C-002 e realizar o pagamento integral. **Focar na marcação da parcela como paga.** |
| **PAG-U-002** | Positivo | **Pagamento Parcial de Parcela** | Acessar Contas a Pagar, selecionar a **segunda parcela** do VEN-C-002 e realizar um pagamento parcial (ex: 50% do valor). **Focar na atualização do saldo devedor da parcela.** |

---

## 5. Rotina: Fechamento de Caixa

| ID do Cenário | Tipo | Ação no Vídeo | Foco da Gravação |
| :--- | :--- | :--- | :--- |
| **CAIXA-P-001** | Positivo | **Simulação de 3 Caixas Simultâneos** | Mostrar a abertura de 3 telas de "Front de Caixa" (simulando 3 usuários). Realizar uma venda em cada caixa. Mostrar o processo de fechamento de cada um dos 3 caixas. **Focar na consolidação individual e correta dos valores de cada caixa.** |
