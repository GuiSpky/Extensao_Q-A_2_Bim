| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C06-CT01 | Cadastrar novo fornecedor. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter um produto ja cadastrado no sistema. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que temos acesso ao sistema                              |
| **E** acessamos "consultas/Produtos/Completa"                     |
| **E** selecionamos "novo"                                         |
| **E** no campo fornecedor preenchemos com o nome do fornecedor e clicamos em "salvar"    |
| **E** adicionamos os produtos que serão comprados e suas quantidades|
| **E** Clicamos em "Finalizar" e definimos o pagamento             |
| **QUANDO** clicamos em "Salvar"                                   |
| **ENTÃO** o sistema deve redirecionar para pagina de compra com status confirmado|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| o sistema deve redirecionar para pagina de compra com status confirmado.                |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado, sistema excluiu item. | 
| **URL:** https://drive.google.com/file/d/1TgjILneg34c5QodLNRvccJm9YXcq2rpe/view?usp=drive_link |

---

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C06-CT02 |  Confirmar atualização de estoque apenas para itens recebidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Ter compra e fornecedor cadastrados. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que temos acesso ao sistema                              |
| **E** estamos na tela "Consulta/Produto/Estoque"                  |
| **E** selecionamos "Consulta por nome"                            |
| **E** digitamos o nome dos produtos comprados                     |
| **QUANDO** clicamos em "executar"                                 |
| **ENTÃO**  o sistema deve apresentar quantidade de itens do produto |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| o sistema deve apresentar quantidade de itens do produto.       |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| Teste realizado, sistema excluiu item. | 
| **URL:** https://drive.google.com/file/d/1ljRl11hWbXfzpKyQGsJGy0c6qyAI7Q8I/view?usp=drive_link |
