# Testes e Validação de Requisitos — Amazon Shopping

Projeto acadêmico desenvolvido para o Seminário 2 da disciplina de Engenharia de Software, do curso de Sistemas de Informação do IF Goiano — Campus Catalão.

O trabalho analisa o fluxo de busca de produtos até a revisão do checkout na Amazon Brasil. A avaliação foi realizada pela interface disponível ao usuário, sem acesso ao código interno e sem confirmação de compras.

## Informações do trabalho

| Informação | Descrição |
|---|---|
| Disciplina | Engenharia de Software — 2026/2 |
| Professor | Luís Felipe Schons Silva |
| Integrante(s) | [João Henrique do Nascimento Filho] |
| Aplicação | Amazon Shopping — versão web |
| Endereço | https://www.amazon.com.br/ |
| Data dos testes | 16/11/2026 |
| Dispositivo | PC |
| Sistema operacional | [Windows Home 11] |
| Navegador | [Versão 158.0.8127.37 (Versão oficial) 64 bits] |

## Objetivo

Verificar se o usuário em uma situação normal, (considerando internet, e hardware) consegue localizar um produto, consultar suas informações, gerenciar o carrinho e acessar o checkout com dados consistentes.

A análise considera os comportamentos esperados definidos nos requisitos e critérios de aceitação, incluindo situações alternativas, validações e limites de quantidade.

## Escopo

O fluxo analisado foi:

Busca → detalhes do produto → carrinho → checkout → revisão anterior à confirmação do pedido.

Foram incluídas as seguintes verificações:

- Pesquisa com termo válido e sem correspondência.
- Identificação do produto e de sua oferta.
- Inclusão, alteração de quantidade e remoção de itens.
- Limites de quantidade apresentados na interface.
- Cálculo do subtotal.
- Persistência do carrinho após atualizar a página.
- Solicitação de autenticação no checkout.
- Validação de campo obrigatório do endereço.
- Consistência dos itens, frete e total no checkout.

Não fazem parte do escopo a confirmação do pedido, o processamento de pagamentos, a entrega, o pós-venda, a administração da aplicação e os testes de segurança ou carga.

O detalhamento está em [Escopo do projeto](docs/escopo.md).

## Requisitos analisados

Os requisitos foram definidos para orientar a avaliação acadêmica a partir do comportamento esperado do fluxo. Eles não representam documentação interna oficial da Amazon.

| ID | Comportamento esperado |

| RF01 | Permitir pesquisar produtos e apresentar uma resposta compreensível para a busca. |
| RF02 | Permitir consultar os detalhes e adicionar ao carrinho a oferta selecionada. |
| RF03 | Permitir alterar quantidades e remover itens, respeitando os limites apresentados. |
| RF04 | Calcular corretamente o subtotal e preservar o estado do carrinho após atualizar a página na mesma sessão. |
| RF05 | Exigir autenticação antes do acesso às etapas pessoais do checkout. |
| RF06 | Validar dados obrigatórios de entrega e apresentar informações consistentes no checkout. |

Cada requisito está associado a critérios de aceitação e casos de teste:

- [Requisitos](docs/requisitos.md)
- [Critérios de aceitação](docs/Criterios-aceitacao.md)
- [Rastreabilidade](testes/rastreabilidade.md)

## Estratégia de testes

A abordagem adotada foi o teste manual de caixa-preta. As ações foram realizadas como um usuário comum: pesquisar, abrir produtos, alterar o carrinho e conferir as respostas da interface.

O planejamento combina cenários de funcionamento esperado com situações capazes de revelar problemas:

| Técnica | Aplicação no projeto |
|
| Particionamento de equivalência | Busca válida e sem correspondência; endereço com preenchimento válido e campo obrigatório vazio. |
| Análise de valor-limite | Verificação do controle de quantidade ao atingir uma unidade. |
| Transição de estados | Inclusão e remoção de itens, alteração de quantidade e avanço de uma sessão sem login para a solicitação de identificação. |

Também foi observada a restrição de estoque ao tentar aumentar a quantidade de uma oferta com apenas uma unidade disponível.

O [Plano de testes](testes/plano-de-testes.md) apresenta o ambiente, os dados utilizados e os critérios de conclusão.

## Produtos utilizados

| Produto | Formato | Utilização |
|---|---|---|
| Box — Dom Quixote, de Miguel de Cervantes, editora Nova Fronteira | Capa dura | Consulta de detalhes, inclusão no carrinho, verificação do limite mínimo e revisão do checkout. |
| Caixa Dom Quixote, de Miguel de Cervantes | Capa comum | Alteração para duas unidades e conferência do subtotal. |

A oferta do Box de capa dura apresentava apenas uma unidade em estoque. Por isso, foi utilizado um produto alternativo com disponibilidade suficiente para executar o cenário de alteração de uma para duas unidades.

Essa mudança foi registrada no CT05. O impedimento inicial por falta de estoque não foi classificado como defeito, pois a aplicação informou a restrição e manteve a quantidade disponível.

## Casos de teste

Foram planejados 12 casos:

| Caso | Verificação | Critério |
|---|---|---|
| CT01 | Busca válida | CA01 |
| CT02 | Busca sem correspondência | CA02 |
| CT03 | Detalhes do produto | CA03 |
| CT04 | Inclusão no carrinho | CA04 |
| CT05 | Alteração da quantidade | CA05 |
| CT06 | Limite mínimo de quantidade | CA06 |
| CT07 | Cálculo do subtotal | CA08 |
| CT08 | Persistência após atualizar a página | CA09 |
| CT09 | Remoção do carrinho | CA07 |
| CT10 | Autenticação no checkout | CA10 |
| CT11 | Campo obrigatório do endereço | CA11 |
| CT12 | Consistência no checkout | CA12 |

Os passos, dados, resultados obtidos e evidências estão em [Casos de teste](testes/casos-de-teste.md).

O [Checklist](testes/checklist.md) reúne as verificações do fluxo para consulta rápida.

## Resultados documentados

A tabela apresenta o estado de consolidação dos resultados. Os registros pendentes devem ser atualizados conforme a execução e as evidências disponíveis.

| Caso | Resultado | Constatação |
|---|---|---|
| CT01 | A confirmar | Falta consolidar o resultado observado na busca válida. |
| CT02 | PASS | A aplicação informou a ausência de resultados e diferenciou as recomendações da resposta à busca. |
| CT03 | PASS | A página apresentou identificação do livro, formato, editora, preço e condições da oferta. |
| CT04 | PASS | A inclusão foi confirmada e o produto apareceu no carrinho com uma unidade. |
| CT05 | PASS | O produto alternativo permitiu alterar a quantidade para duas unidades. |
| CT06 | PASS | Na quantidade de uma unidade, o controle apresentou uma lixeira em vez da opção de diminuir. |
| CT07 | PASS | Duas unidades de R$ 86,54 resultaram no subtotal correto de R$ 173,08. |
| CT08 | A confirmar | Falta consolidar a comparação do carrinho antes e depois da atualização. |
| CT09 | Parcialmente comprovado | A remoção do Box foi demonstrada; o cenário planejado de carrinho vazio ainda precisa ser consolidado. |
| CT10 | A confirmar | Falta consolidar o resultado da tentativa de checkout sem autenticação. |
| CT11 | A confirmar | Falta consolidar a mensagem e o impedimento apresentados para o endereço incompleto. |
| CT12 | PASS | Uma unidade de R$ 201,92, acrescida de R$ 23,02 de frete, resultou no total correto de R$ 224,94. |

Até esta consolidação, há **7 casos com PASS, 1 parcialmente comprovado e 4 a confirmar**. Não foi constatado FAIL nos resultados confirmados.

“A confirmar” e “Parcialmente comprovado” indicam pendências de documentação ou verificação. Não equivalem a aprovação nem a defeito da aplicação.

### Classificação dos resultados

- **PASS:** o comportamento observado atende ao resultado esperado.
- **FAIL:** o comportamento observado diverge do critério de aceitação.
- **BLOQUEADO:** uma condição impede executar o cenário planejado.
- **NÃO EXECUTADO:** o caso ainda não foi realizado.

Um teste com entrada inválida pode receber PASS quando a aplicação rejeita a entrada corretamente. Da mesma forma, uma restrição informada de estoque não caracteriza falha por si só.

## Evidências e defeitos

As capturas estão organizadas na pasta [evidencias](evidencias/), identificadas pelo número do caso de teste.

As imagens devem preservar as informações necessárias à análise e ocultar dados pessoais, endereço e informações de pagamento.

Caso um teste apresente FAIL e a divergência seja confirmada, o defeito deverá ser registrado na área **Issues** deste repositório, contendo:

- Ambiente e pré-condições.
- Passos para reprodução.
- Resultado esperado e obtido.
- Evidência disponível.
- Severidade.
- Referência ao requisito, critério e caso de teste.

Não é obrigatório encontrar defeitos. A avaliação depende da relevância dos cenários e da fidelidade dos registros.

## Organização do repositório

| Caminho | Conteúdo |
|---|---|
| `README.md` | Visão geral, estratégia e resultados consolidados. |
| `docs/escopo.md` | Aplicação, fluxo e limites da análise. |
| `docs/requisitos.md` | Requisitos definidos para o projeto. |
| `docs/criterios-aceitacao.md` | Condições utilizadas para avaliar os comportamentos. |
| `testes/plano-de-testes.md` | Planejamento da execução. |
| `testes/checklist.md` | Lista de verificações e resultados. |
| `testes/casos-de-teste.md` | Procedimentos e registros de cada caso. |
| `testes/rastreabilidade.md` | Relação entre requisitos, critérios e casos. |
| `evidencias/` | Capturas utilizadas para demonstrar os resultados. |

## Conclusão

Os resultados confirmados indicam que os cenários avaliados de busca sem correspondência, identificação do produto, gerenciamento de quantidade e cálculo de valores atenderam aos critérios definidos.

A aplicação também apresentou uma mensagem ao impedir o aumento da quantidade de uma oferta com estoque insuficiente. O cenário de alteração para duas unidades foi executado com outro produto, preservando o objetivo do teste.

Na revisão do checkout, o valor dos itens e o frete corresponderam ao total apresentado. A análise foi encerrada antes da confirmação do pedido.

A conclusão permanece limitada aos casos efetivamente verificados. As pendências precisam ser consolidadas antes do encerramento do trabalho, e os resultados não permitem afirmar que toda a aplicação está livre de defeitos. Pagamento, entrega e pós-venda não foram avaliados.
