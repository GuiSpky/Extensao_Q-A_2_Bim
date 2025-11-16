| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C02-CT01 | Consulta de produtos será realizada. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter produtos criados e cadastrados no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página inicial do sistema                 |
| **E** temos acesso a tela "Consultas/produtos/completa"           |
| **E** preenchemos o campo "Nome Produto"                          |
| **QUANDO** clicarmos no botão "Executar"                          |
| **ENTÃO** o sistema mostrará a lista de itens com o nome cadastrado.|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| aparecer todos os produtos com o nome da busca.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| * Teste realizado sem erros | 
| * **URL:** https://drive.google.com/file/d/1qtRcg_0Ws-EOwDCQsF6efI_gx0z7a0af/view?usp=drive_link | 

---
### Caso de Teste 02: Consulta de Produto Inexistente.

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C02-CT01 | Consulta de produtos não será realizada. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| ter nenhum produto com o nome da busca no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na página inicial do sistema                 |
| **E** temos acesso a tela "Consultas/produtos/completa"           |
| **E** preenchemos o campo "Nome Produto" com um produto não cadastrado|                         |
| **QUANDO** clicarmos no botão "Executar"                          |
| **ENTÃO** o sistema deve informar que não tem produto com o nome da busca.|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve retornar uma lista vazia ou uma mensagem indicando que o produto não foi encontrado.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| *  Teste realizado, sistema retornou uma lista em branco| 
| * **URL:** https://drive.google.com/file/d/1JTBxn07v3DkhakIzQckvPeiZWa96Gx2g/view?usp=drive_link | 
