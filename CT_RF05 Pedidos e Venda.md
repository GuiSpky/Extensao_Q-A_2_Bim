| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C05-CT01 | Venda Completa com Pagamento à Vista. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Produto e Cliente cadastrados. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela "Pedidos/Venda"                      |
| **E** selecionamos "Nova"                                         |
| **E** preenchemos os campos clientes e vendedor                   |
| **E** selecionamos os produtos da venda                           |
| **E** selecionamos "Finalizar"                                    |
| **E** selecionamos a "condição de venda" como "VISTA" e o status como confirmado|
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** seremos redirecionados para tela de venda com o status confirmado|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| redirecionados para tela de venda com o status confirmado.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| * Teste realizado sem erros | 
| * **URL:** https://drive.google.com/file/d/1qPtiSJdLE6Dng_1MRngc_LCKbQj7lgIP/view?usp=drive_link | 

--- 

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C05-CT02 | Finalizar venda com pagamento misto. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Produto e Cliente cadastrados. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela "Pedidos/Venda"                      |
| **E** selecionamos "Nova"                                         |
| **E** preenchemos os campos clientes e vendedor                   |
| **E** selecionamos os produtos da venda                           |
| **E** selecionamos "Finalizar"                                    |
| **E** selecionamos a "condição de venda" como "VISTA" e o status como confirmado|
| **E** selecionamos "entrada de pagamento" como "dinheiro" e definimos o valor que será pago|
| **E** adicionamos uma nova "entrada de pagamento" como "crédito" e o valor que será pago|
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** seremos redirecionados para tela de venda com o status confirmado|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| redirecionados para tela de venda com o status confirmado.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| * Teste realizado sem erros | 
| * **URL:** https://drive.google.com/file/d/1eqB8GGGHtFw97Bu9EccGN347q9PQNLe3/view?usp=drive_link | 

---

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C05-CT03 | Venda com Parcelamento (Contas a Pagar). |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Produto e Cliente cadastrados. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela "Financeiro/Contas a pagar"          |
| **E** selecionamos "Busca"                                        |
| **E** selecionamos a canta que será parcelada                     |
| **E** clicamos com o botão direito do mouse para abrir opções em cima da fatura desejada|
| **E** selecionamos "Pagar parcela"                                |
| **E** informamos o documento do tipo de pagamento e o valor       |
| **QUANDO** clicarmos no botão "confirmar"                         |
| **ENTÃO** seremos redirecionados para tela anterior e a fatura aparecera como paga|

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| redirecionados para tela anterior e a fatura aparecera como paga.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| * Teste realizado sem erros | 
| * **URL:** https://drive.google.com/file/d/1C-5YTjCfpgjPRI322j62AKr5emTboe4K/view?usp=drive_link | 

--- 

| ID       | Descrição                                                |
| :------- | :------------------------------------------------------- |
| C05-CT03 | Venda com Produto sem Estoque. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Produto cadastrado com estoque zero. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que estamos na tela "Pedidos/Venda"                      |
| **E** selecionamos "Nova"                                         |
| **E** preenchemos os campos clientes e vendedor                   |
| **E** selecionamos um produto com estoque zerado para venda       |
| **E** selecionamos "Finalizar"                                    |
| **E** selecionamos a "condição de venda" como "VISTA" e o status como confirmado|
| **QUANDO** clicarmos no botão "Salvar"                            |
| **ENTÃO** o sistema deve informar que não tem item em estoque     |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| o sistema deve informar que não tem item em estoque.  |

| Resultado |
| :---------------------------------------------------------------- |
| Teste realizado | 
| * Teste realizado, sistema realiza a venda e subtrai item do estoque, ficando netativo | 
| * **URL:** https://drive.google.com/file/d/1jx2TZ8D0Di5OI_pALG_QmCG-TSo9YrdD/view?usp=drive_link | 
