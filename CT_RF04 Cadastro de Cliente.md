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

