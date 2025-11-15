| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C04-CT01 | Cadastro de cliente. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter dados validos para cadastro. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** estamos na tela de "Cadastro/clientes"                   |
| **E** selecionamos "Novo"                                         |
| **E** preenchemos todos os dados corretamente                     |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** seremos redirecionados tela de cadastro                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O redirecionamento para tela de cadastro com os dados do novo cliente.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado sem erros | 
| **URL:** https://drive.google.com/file/d/14k7SNqChO_guyqb0IilHrRNllpbv5oCL/view?usp=drive_link | 

---

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C04-CT02 | Criação de Cliente com Limite de Crédito. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter dados validos para cadastro e acesso a configuração de crédito. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** estamos na tela de "Consultar/clientes"                  |
| **E** selecionamos o cliente que desejamos adicionar o limite de crédito |
| **E** preenchemos todos os dados corretamente                     |
| **E** selecionamos a aba "Dados Financeiros"                      |
| **E** selecionamos "Alterar"                                      |
| **E** editamos o valor do "limite de Crédito"                     |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** seremos redirecionados tela de cadastro                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
|  O cliente deve ser cadastrado com sucesso e o limite de crédito registrado.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado sem erros | 
| **URL:** https://drive.google.com/file/d/1WVinHgw1b-kgTwfri3TLEheWBZpr5XhK/view?usp=drive_link | 

--- 

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C04-CT03 | Edição de Cliente para adicionar dependentes. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter um cliente cadastrado e dados do dependente que será adicionado. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** estamos na tela de "Consultar/clientes"                  |
| **E** selecionamos o cliente que desejamos adicionar o limite de crédito |
| **E** preenchemos todos os dados corretamente                     |
| **E** selecionamos a aba "Dependentes"                            |
| **E** selecionamos "Alterar"                                      |
| **E** adcione os dados do dependente                              |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** seremos redirecionados tela de cadastro                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
|  O dependente deve ser vinculado ao cliente com sucesso.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado sem erros | 
| **URL:** https://drive.google.com/file/d/1K2-_NxNEp74bb5VxLvtEmHF_M73NwlGh/view?usp=drive_link | 

---
| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C04-CT04 | Criação de Cliente com CPF Duplicado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Um cliente com o mesmo CPF já existe no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** estamos na tela de "Cadastro/clientes"                   |
| **E** selecionamos "Novo"                                         |
| **E** preenchemos todos os dados corretamente mas utilizar CPF duplicado |
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** o sistema deve informar erro de duplicidade             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
|   O sistema deve exibir uma mensagem de erro indicando que o CPF já está em uso e não deve permitir o salvamento.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado sem erros | 
| **URL:** https://drive.google.com/file/d/1FCKVRSiZtWNODNRDR9ajO-Gqhf2o6W-H/view?usp=drive_link | 

### **2.2. Read (Consulta)**

*   **CLI-R-001** (Positivo): **Consulta de Cliente e Dependentes**
    *   **Pré-condição**: Cliente e dependente criados com sucesso (CLI-C-001 e CLI-C-002).
    *   **Passos**: 1. Acessar a tela de consulta de clientes. 2. Pesquisar pelo "Nome" ou "CPF" do cliente. 3. Acessar a aba "Dependentes".
    *   **Resultado Esperado**: O cliente deve ser exibido com seus dados corretos e o dependente deve estar listado na aba correspondente.

### **2.3. Update (Atualização)**

*   **CLI-U-001** (Positivo): **Aumento do Limite de Crédito**
    *   **Pré-condição**: Cliente criado com sucesso (CLI-C-001).
    *   **Passos**: 1. Consultar e abrir o cliente para edição. 2. Aumentar o valor do "Limite de Crédito". 3. Clicar em "Salvar".
    *   **Resultado Esperado**: O sistema deve exibir mensagem de sucesso e o novo limite deve ser registrado.

### **2.4. Delete (Exclusão)**

*   **CLI-D-001** (Positivo): **Exclusão de Dependente**
    *   **Pré-condição**: Cliente e dependente criados com sucesso (CLI-C-001 e CLI-C-002).
    *   **Passos**: 1. Consultar e abrir o cliente. 2. Acessar a aba "Dependentes". 3. Selecionar o dependente e clicar em "Excluir". 4. Confirmar a exclusão.
    *   **Resultado Esperado**: O sistema deve exibir mensagem de sucesso e o dependente não deve mais estar vinculado ao cliente.

*   **CLI-D-002** (Negativo): **Exclusão de Cliente com Vendas Vinculadas**
    *   **Pré-condição**: Cliente com histórico de vendas.
    *   **Passos**: 1. Consultar e selecionar o cliente. 2. Clicar em "Excluir". 3. Confirmar a exclusão.
    *   **Resultado Esperado**: O sistema deve exibir uma mensagem de erro indicando que o cliente possui vínculos e não pode ser excluído.

---

## 🛒 **Rotina 3: Pedidos/Venda**

**Descrição**: Esta rotina é o fluxo principal de vendas, incluindo a criação, adição de itens e finalização com pagamento.

### **3.1. Create (Criação)**

*   **VEN-C-001** (Positivo): **Venda Completa com Pagamento à Vista**
    *   **Pré-condição**: Produto e Cliente cadastrados.
    *   **Passos**: 1. Iniciar nova venda. 2. Informar Cliente e Funcionário. 3. Adicionar um ou mais produtos com quantidade em estoque. 4. Clicar em "Finalizar". 5. Informar pagamento à vista e salvar.
    *   **Resultado Esperado**: A venda deve ser finalizada com sucesso, o estoque dos produtos deve ser baixado e o financeiro registrado.

*   **VEN-C-002** (Positivo): **Venda com Parcelamento (Contas a Pagar)**
    *   **Pré-condição**: Produto e Cliente cadastrados.
    *   **Passos**: 1. Iniciar nova venda. 2. Adicionar produtos. 3. Clicar em "Finalizar". 4. Informar pagamento parcelado (ex: 5x) e salvar.
    *   **Resultado Esperado**: A venda deve ser finalizada com sucesso, o estoque baixado e as 5 parcelas devem ser geradas no Contas a Pagar.

*   **VEN-C-003** (Negativo): **Venda com Produto sem Estoque**
    *   **Pré-condição**: Produto cadastrado com estoque zero.
    *   **Passos**: 1. Iniciar nova venda. 2. Tentar adicionar o produto com estoque zero.
    *   **Resultado Esperado**: O sistema deve exibir um alerta de estoque insuficiente e não permitir a adição do item ou a finalização da venda.

*   **VEN-C-004** (Negativo): **Venda para Cliente com Limite Excedido**
    *   **Pré-condição**: Cliente com limite de crédito de R$ 100,00 e valor da venda de R$ 150,00.
    *   **Passos**: 1. Iniciar nova venda. 2. Informar o cliente com limite. 3. Adicionar produtos totalizando R$ 150,00. 4. Tentar finalizar a venda a prazo.
    *   **Resultado Esperado**: O sistema deve exibir uma mensagem de erro/alerta de limite de crédito excedido e não permitir a finalização a prazo.

### **3.2. Update (Atualização/Alteração)**

*   **VEN-U-001** (Positivo): **Alteração de Quantidade de Item Antes de Finalizar**
    *   **Pré-condição**: Venda iniciada com itens adicionados.
    *   **Passos**: 1. Acessar a venda em andamento. 2. Alterar a quantidade de um item. 3. Clicar em "Salvar" (do item).
    *   **Resultado Esperado**: O valor total da venda deve ser recalculado corretamente.

### **3.3. Delete (Exclusão/Cancelamento)**

*   **VEN-D-001** (Positivo): **Cancelamento de Venda Não Finalizada**
    *   **Pré-condição**: Venda iniciada, mas sem finalização.
    *   **Passos**: 1. Acessar a venda em andamento. 2. Clicar em "Excluir" ou "Cancelar". 3. Confirmar o cancelamento.
    *   **Resultado Esperado**: A venda deve ser removida do sistema e o estoque não deve ser afetado.

---

## 💰 **Rotina 4: Contas a Pagar (Pagamento de Parcelas)**

**Descrição**: Esta rotina foca na gestão e pagamento das parcelas geradas por vendas a prazo.

### **4.1. Update (Pagamento)**

*   **PAG-U-001** (Positivo): **Pagamento Total de Parcela**
    *   **Pré-condição**: Parcela gerada por venda a prazo (VEN-C-002).
    *   **Passos**: 1. Acessar o Contas a Pagar. 2. Selecionar a primeira parcela. 3. Realizar o pagamento do valor total.
    *   **Resultado Esperado**: A parcela deve ser marcada como paga, e o valor do caixa/banco deve ser atualizado.

*   **PAG-U-002** (Positivo): **Pagamento Parcial de Parcela**
    *   **Pré-condição**: Parcela gerada por venda a prazo (VEN-C-002).
    *   **Passos**: 1. Acessar o Contas a Pagar. 2. Selecionar a segunda parcela. 3. Realizar o pagamento de um valor menor que o total.
    *   **Resultado Esperado**: A parcela deve ter seu saldo devedor atualizado, e o valor pago deve ser registrado no caixa/banco. A parcela deve permanecer em aberto com o saldo restante.

---

## 💵 **Rotina 5: Fechamento de Caixa**

**Descrição**: Esta rotina simula a operação de múltiplos caixas.

### **5.1. Positivos**

*   **CAIXA-P-001** (Positivo): **Simulação de 3 Caixas Simultâneos**
    *   **Pré-condição**: 3 usuários/terminais com acesso ao sistema.
    *   **Passos**: 1. Abrir 3 sessões de "Front de Caixa" simultaneamente. 2. Realizar vendas em cada um dos 3 caixas. 3. Realizar o fechamento de cada caixa.
    *   **Resultado Esperado**: As vendas devem ser registradas corretamente em cada caixa, e o fechamento deve consolidar os valores de forma independente e correta.
