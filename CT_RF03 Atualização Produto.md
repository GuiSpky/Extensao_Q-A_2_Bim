## Cenário 03: Atualização de Produto.
---
| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT01 | Atualização de preço de venda dos produtos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter um produto ja cadastrado no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que temos acesso ao sistema                              |
| **E** acessamos "consultas/Produtos/Completa"                     |
| **E** preenchemos o campo "Nome Produto"                          |
| **E** clicarmos no botão "Executar"                               |
| **E** abrimos produto que deseja editar                           |
| **E** Clicamos em "Alterar"                                       |
| **E** na aba "Preços" alteramos o valor do "Preço de venda 1"     |
| **QUANDO** clicamos em "Salvar"                                   |
| **ENTÃO** seremos redirecionados tela inicial de Cadastro de Produto|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O redirecionamento para a tela inicial de Cadastro de Produto.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado sem erros | 
| **URL:** https://drive.google.com/file/d/1KDckXsgZ_VUjSyGERs_2xf0SdNjk6D7n/view?usp=drive_link |

---
| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT02 | Atualização com Campo Obrigatório Vazio. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter um produto ja cadastrado no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que temos acesso ao sistema                              |
| **E** acessamos "consultas/Produtos/Completa"                     |
| **E** preenchemos o campo "Nome Produto"                          |
| **E** clicarmos no botão "Executar"                               |
| **E** abrimos produto que deseja editar                           |
| **E** Clicamos em "Alterar"                                       |
| **E** apagar nome do produto                                      |
| **QUANDO** clicamos em "Salvar"                                   |
| **ENTÃO** o sistema deve informar o erro de campo vazio           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir uma mensagem de erro.                     |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado, sistema não permitiu salvar o produto. | 
| **URL:** https://drive.google.com/file/d/1A7Te0RtLP_vCN_b6Pu0ACP5wI0yaRYIT/view?usp=drive_link |

---

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C03-CT03 | Exclusão de Produto sem Vínculos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter um produto ja cadastrado no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que temos acesso ao sistema                              |
| **E** acessamos "consultas/Produtos/Completa"                     |
| **E** preenchemos o campo "Nome Produto"                          |
| **E** clicarmos no botão "Executar"                               |
| **E** abrimos produto que deseja excluir                          |
| **E** Clicamos em "Excluir" e confirmar                           |
| **QUANDO** clicamos em "Salvar"                                   |
| **ENTÃO** o sistema deve informar que o produto foi exluido       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve apagar o item e remover da lista.                |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado, sistema excluiu item. | 
| **URL:** https://drive.google.com/file/d/1p1TFt400EhUmW71Kq1hsKe6VlkxaYMcM/view?usp=drive_link |
