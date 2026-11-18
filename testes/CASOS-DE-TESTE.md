### CT01 — Busca válida

- Requisito: RF01
- Critério: CA01
- Data e horário: 16/11/2026, às [15:50].

- Pré-condições: site acessível, conexão com a internet e campo de busca disponível.
- Dados utilizados: termo de pesquisa “Dom Quixote - Nova Fronteira”.

- Passos executados:
  1. Acessar https://www.amazon.com.br/.
  2. Clicar no campo de busca.
  3. Digitar “Dom Quixote - Nova Fronteira”.
  4. Executar o botão de pesquisa.
  5. Verificar se há um resultado correspondente ao livro
     Dom Quixote, da editora Nova Fronteira.

- Resultado esperado: apresentar pelo menos um resultado
  correspondente ao livro Dom Quixote, da editora Nova Fronteira.

- Resultado obtido: preencher após executar a pesquisa.
- Status: 
- Evidência: Busca: https://www.amazon.com.br/s?k=DOM+QUIXOTE+-+NOVA+FRONTEIRA&__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=1MMDGYK264UOT&sprefix=dom+quixote+-+nova+fronteira%2Caps%2C239&ref=nb_sb_noss_2; Print: C:\Users\arqui\OneDrive\Desktop\LUIS SEMINÁRIO\EVIDENCIAS
- Issue, se houver: preencher caso seja identificado um defeito.
- print: evidencias/CA01.png

### CT02 — Busca sem correspondência

- Requisito: RF01
- Critério: CA02
- Pré-condições: site acessível, conexão com a internet e campo de busca disponível.
- Dados utilizados: termo de pesquisa “zzqvproduto987654321;”.

- Passos executados:
  1. Acessar https://www.amazon.com.br/.
  2. Clicar no campo de busca.
  3. Digitar “zzqvproduto987654321;”.
  4. Executar a pesquisa.
  5. Observar a mensagem apresentada e verificar se eventuais
     recomendações estão diferenciadas dos resultados da busca.

- Resultado esperado : a interface deve informar de forma
  compreensível que não existem resultados para o termo,
  sem apresentar recomendações como correspondências exatas.

-  Resultado obtido: o sistema apresentou a mensagem
  “Nenhum resultado para sua consulta de pesquisa” e orientou
  a verificar a ortografia ou usar termos mais genéricos.
  o Site Também exibiu recomendações em uma seção separada,
  identificada como relacionada ao histórico de navegação.

- Status: PASS
- Evidência: ![https://www.amazon.com.br/s?k=zzqvproduto987654321%3B&__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2P915X7DCRXEA&sprefix=zzqvproduto987654321+%2Caps%2C301&ref=nb_sb_noss]
C:\Users\arqui\OneDrive\Desktop\LUIS SEMINÁRIO\EVIDENCIAS
- Issue, se houver: não se aplica.
- Evidencia: evidencias/CA02.png

### CT03 — Detalhes do produto

- Requisito: RF02
- Critério: CA03
- Pré-condições: pesquisa por “Dom Quixote Nova Fronteira”
  realizada e produto apresentado nos resultados.

- Dados utilizados:
  - Produto: Box — Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Editora: Nova Fronteira.
  - Formato: capa dura.
  - ISBN-13: 978-8520923092.
  - URL: [https://www.amazon.com.br/Dom-Quixote-Caixa-Miguel-Cervantes/dp/8520923097/ref=sr_1_1?crid=DYGXN664C1TK&dib=eyJ2IjoiMSJ9.rX8I_hMYmQzptNC7VMjL8edId7sBySHfucnTxx6V2CK1TOs-bfX8hCPmj09cn823aF6aZ6DfDg4U9SPBww7HcD5D-8b8zPnh8KLoHpjjhCJnznL5xrJr2Zlf4PvWSQD4eNQ1vb9YyoVj7hNyYs7pew.YH6BWNPWuIn_Pg483MCifsLDtxotO603gakyqP_3uxY&dib_tag=se&keywords=dom+quixote+-+nova+fronteira&qid=1795031570&sprefix=%2Caps%2C200&sr=8-1&ufe=app_do%3Aamzn1.fos.fcd6d665-32ba-4479-9f21-b774e276a678]


-  Passos executados :
  1. Localizar o produto nos resultados da pesquisa.
  2. Clicar no anúncio do Box — Dom Quixote.
  3. Conferir o título, o autor, a editora e o formato.
  4. Verificar o preço e as condições da oferta apresentada.

- Resultado esperado: a página deve corresponder ao produto
  selecionado e permitir identificar o livro, sua oferta
  e o preço apresentado.

- Resultado obtido: a página apresentou o Box — Dom Quixote,
  de Miguel de Cervantes, da editora Nova Fronteira,
  no formato capa dura, com ISBN-13 978-8520923092.
  Foram exibidos o preço de R$ 201,92 e a oferta de
  R$ 191,82 à vista, com desconto de 5% no Pix e NuPay,
  nas condições indicadas na página.

- Status: PASS

- Evidência: C:\Users\arqui\OneDrive\Desktop\LUIS SEMINÁRIO\EVIDENCIAS
- evidencias/CA03.png
- Issue, se houver: não se aplica.

- Observações: a oferta apresentaVA somente uma unidade
  em estoque no momento de teste, condição que deverá ser considerada nos
  testes de alteração de quantidade.

### CT04 — Inclusão do produto no carrinho

- Requisito: RF02
- Critério: CA04

- Pré-condições:
  - Página do Box — Dom Quixote aberta.
  - Oferta disponível para compra.
  - Produto de teste ausente do carrinho.

- Dados utilizados:
  - Produto: Box — Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Editora: Nova Fronteira.
  - Formato: capa dura.
  - Quantidade solicitada: 1 unidade.
  - Preço apresentado: R$ 201,92.
  - URL: https://www.amazon.com.br/cart?ref_=sw_gtc.

- Passos:
  1. Acessar a página do produto.
  2. Conferir o produto e o formato capa dura.
  3. Adicionar uma unidade ao carrinho.
  4. Observar a confirmação de inclusão.
  5. Clicar em “Ir para o carrinho”.
  6. Conferir o produto, o formato e a quantidade registrada.

- Resultado esperado: o carrinho deve apresentar o
  Box — Dom Quixote, no formato capa dura, com uma unidade,
  correspondendo ao produto selecionado.

- Resultado obtido: a aplicação apresentou a mensagem
  “Adicionado ao carrinho”, com indicação do formato capa dura
  e subtotal de R$ 201,92 para um produto.
  [Completar com o que foi observado ao abrir o carrinho.]

- Status: EM EXECUÇÃO — falta registrar a conferência
  do produto e da quantidade dentro do carrinho.

- Evidências:
C:\Users\arqui\OneDrive\Desktop\LUIS SEMINÁRIO\EVIDENCIAS
Prints:
evidencias/CA04-PT1.png
evidencias/CA04-PT2.png
evidencias/CA04-PT3.png

- Issue, se houver: nenhuma identificada até esta etapa.


### CT05 — Alteração da quantidade no carrinho

- Requisito: RF03
- Critério: CA05

- Pré-condições:
  - Produto alternativo adicionado ao carrinho com uma unidade.
  - Estoque suficiente para aumentar a quantidade para duas unidades.

- Dados utilizados:
  - Produto: Caixa Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Formato: capa comum.
  - Quantidade inicial: 1 unidade.
  - Quantidade solicitada: 2 unidades.
  - Estoque informado na interface: 4 unidades.
  - URL: [colar o endereço do produto alternativo].

. Passos executados :
  1. Acessar o carrinho com o produto Caixa Dom Quixote,
     no formato capa comum, com uma unidade.
  2. Clicar no botão “+” do controle de quantidade desse produto.
  3. Aguardar a atualização.
  4. Conferir a quantidade apresentada no carrinho.

- Resultado esperado: o sistema deve alterar a quantidade
  do produto de uma para duas unidades.

- Resultado obtido:O Produto dom Quixote de capa dura, por apresentar apenas 1 unidade, foi bloqueado pelo sistema da amazona de aumentar a sua capacidade, sendo que no sistema constava que no estoque se tinha apenas 1 livro disponível. Ja o produto Caixa Dom Quixote, no formato
  capa comum, passou a apresentar duas unidades no carrinho
	.

- Status: PASS

- Evidência: ![Alteração de quantidade] C:\Users\arqui\OneDrive\Desktop\LUIS SEMINÁRIO\EVIDENCIAS

- Issue, se houver: não se aplica.

- Obs: a tentativa inicial com o Box  Dom Quixote,
  capa dura, fOI impedida após constatar haver apenas uma unidade
  em estoque. Para executar o cenário planejado, foi utilizado
  o produto alternativo Caixa Dom Quixote, capa comum,
  com disponibilidade suficiente. O produto original
  permaneceu com uma unidade e apresentou a mensagem
  “No momento há apenas 1 em estoque”.

  evidencias/CA05.png
  evidencias/CA05-PT2.png


### CT06 — Limite mínimo de quantidade no carrinho

- Requisito: RF03
- Critério: CA06



- Pré-condições:
  - Carrinho acessível.
  - Produto Box — Dom Quixote adicionado com uma unidade.

- Dados utilizados:
  - Produto: Box — Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Formato: capa dura.
  - Quantidade no carrinho: 1 unidade.
  - Limite mínimo para manter o item no carrinho: 1 unidade.

- Passos executados:
  1. Acessar o carrinho de compras.
  2. Localizar o produto Box — Dom Quixote.
  3. Conferir a quantidade de uma unidade.
  4. Inspecionar o controle disponível à esquerda da quantidade.
  5. Verificar se existe opção de diminuir a quantidade
     abaixo de uma unidade mantendo o item no carrinho.

- Resultado esperado: ao atingir uma unidade, o controle
  deve impedir quantidade inferior ao mínimo ou oferecer
  a exclusão do item de forma coerente com a interface.

- Resultado obtido: com uma unidade no carrinho, a interface
  apresentou uma lixeira à esquerda da quantidade, em vez
  do botão de diminuir. O controle oferece a exclusão do item
  e não disponibiliza redução para quantidade inferior a um.

- Status: PASS

- Evidência: ![Limite mínimo de quantidade](../evidencias/CT06-limite-minimo.png)

- Issue, se houver: não se aplica.

  Prints: 
  evidencias/CA06.png

- Observações: neste caso foi verificado o controle no limite
  mínimo. A execução da exclusão será avaliada no CT09.

### CT07 — Cálculo do subtotal do carrinho

- Requisito: RF04
- Critério: CA08


- Pré-condições:
  - Carrinho acessível.
  - Produto Caixa Dom Quixote, capa comum, com duas unidades.
  - Apenas esse produto selecionado no carrinho.

- Dados utilizados:
  - Produto: Caixa Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Formato: capa comum.
  - Quantidade: 2 unidades.
  - Preço unitário da oferta: R$ 86,54.
  - Outros itens selecionados: nenhum.
  - Subtotal apresentado: R$ 173,08.

- Passos executados:
  1. Acessar o carrinho de compras.
  2. Conferir o produto selecionado e a quantidade de duas unidades.
  3. Registrar o preço unitário de R$ 86,54.
  4. Multiplicar o preço unitário pela quantidade.
  5. Comparar o resultado com o subtotal apresentado pela aplicação.

- Resultado esperado: o subtotal deve corresponder ao preço
  unitário da oferta multiplicado pela quantidade selecionada,
  totalizando R$ 173,08.

- Cálculo realizado:
  - R$ 86,54 × 2 unidades = R$ 173,08.
  - Subtotal esperado: R$ 173,08.
  - Subtotal apresentado: R$ 173,08.

- Resultado obtido: o sistema apresentou o subtotal de
  R$ 173,08 para duas unidades do produto Caixa Dom Quixote.
  O valor corresponde ao cálculo realizado.

- Status: PASS

- Evidência: ![Cálculo do subtotal](../evidencias/CT07-subtotal.png)

- Issue, se houver: não se aplica.

- Observações: o produto Box — Dom Quixote, capa dura,
  havia sido removido e não compôs o subtotal.
  O preço utilizado no cálculo foi o valor vigente da oferta,
  de R$ 86,54 por unidade.

  evidencias/CA07.png

### CT08 — Persistência do carrinho após atualizar a página

- Requisito: RF04
- Critério: CA09
  site Amazon Brasil.

- Pré-condições:
  - Produto Caixa Dom Quixote, capa comum, no carrinho.
  - Quantidade de duas unidades.
  - Subtotal inicial de R$ 173,08.

- Dados utilizados:
  - Produto: Caixa Dom Quixote.
  - Formato: capa comum.
  - Quantidade inicial: 2 unidades.
  - Preço unitário inicial: R$ 86,54.
  - Subtotal inicial: R$ 173,08.

- Passos:
  1. Acessar o carrinho de compras.
  2. Registrar o produto, a quantidade e o subtotal.
  3. Capturar a tela antes da atualização.
  4. Atualizar a página pelo navegador.
  5. Conferir se o produto e a quantidade foram preservados.
  6. Verificar o subtotal e eventuais avisos de alteração.
  7. Capturar a tela após a atualização.

- Resultado esperado: o produto e as duas unidades devem
  permanecer no carrinho após atualizar a página na mesma
  sessão. Sem alterações de preço ou estoque informadas,
  o subtotal deve permanecer em R$ 173,08.

- Resultado obtido: [descrever o estado do carrinho após
  atualizar a página].

- Status: [PASS / FAIL / NÃO EXECUTADO]

- Evidências:
  - ![Antes da atualização](../evidencias/CT08-antes.png)
  - ![Depois da atualização](../evidencias/CT08-depois.png)

- Issue, se houver: [informar o link ou “não se aplica”].
	evidencias/CA08ANTES.png
	evidencias/CA08DEPOIS.png

### CT09 — Remoção de produto do carrinho

- Requisito: RF03
- Critério: CA07
- Pré-condições:
  - Carrinho acessível.
  - Apenas o produto escolhido para este teste presente
    no carrinho ativo.

- Dados utilizados:
  - Produto removido: [informar o nome].
  - Formato: [informar].
  - Quantidade antes da exclusão: [informar].

- Passos:
  1. Acessar o carrinho.
  2. Conferir o produto e sua quantidade.
  3. Clicar em “Excluir” ou no ícone de lixeira.
  4. Aguardar a atualização.
  5. Verificar se o produto foi removido.
  6. Conferir o estado vazio do carrinho e seu subtotal.

- Resultado esperado: o produto deve deixar de compor
  o carrinho ativo e seu subtotal. Como era o único produto,
  o carrinho deve ficar vazio, com subtotal zero ou sem
  subtotal de compra apresentado.

- Resultado obtido: [descrever a mensagem de remoção,
  o estado do carrinho e o subtotal observado].

- Status: [PASS / FAIL / NÃO EXECUTADO]

- Evidência: ![Remoção do produto](../evidencias/CT09-remocao.png)

- Issue, se houver: [informar o link ou “não se aplica”].
- Prints: evidencias/CA09.png

- Observações: se outros produtos permaneceram no carrinho,
  registrar essa diferença na pré-condição e conferir
  a retirada do valor do item excluído do subtotal.


### CT10 — Solicitação de autenticação no checkout

- Requisito: RF05
- Critério: CA10


- Pré-condições:
  - Sessão sem usuário autenticado.
  - Produto disponível para inclusão no carrinho.

- Dados utilizados:
  - Produto: [informar o produto utilizado].
  - Quantidade: 1 unidade.
  - Estado da sessão: sem login.

- Passos:
  1. Abrir uma janela anônima/privativa.
  2. Acessar https://www.amazon.com.br/.
  3. Conferir se a sessão está sem login.
  4. Pesquisar o produto.
  5. Adicionar uma unidade ao carrinho.
  6. Abrir o carrinho.
  7. Acionar o botão para avançar ao checkout.
  8. Observar se a aplicação solicita identificação antes
     do acesso às etapas pessoais.
  9. Encerrar o teste sem realizar login.

- Resultado esperado: o sistema deve solicitar identificação
  antes de permitir acesso às etapas pessoais do checkout.

- Resultado obtido: [informar a tela e a solicitação
  efetivamente apresentadas].

- Status: [PASS / FAIL / NÃO EXECUTADO]

- Evidência: evidencias/CA10.png

- Issue, se houver: [informar o link ou “não se aplica”].


### CT11 — Validação de campo obrigatório do endereço

- Requisito: RF06
- Critério: CA11
  janela normal, site Amazon Brasil.

- Pré-condições:
  - Usuário autenticado em conta própria.
  - Produto presente no carrinho.
  - Formulário de novo endereço acessível pelo checkout.

- Dados utilizados:
  - Campo obrigatório deixado vazio: [informar o campo].
  - Demais campos obrigatórios preenchidos com dados válidos.
  - Nenhum endereço salvo foi editado.

- Passos:
  1. Acessar o carrinho com a conta conectada.
  2. Avançar ao checkout.
  3. Abrir a opção de adicionar novo endereço.
  4. Preencher os demais campos obrigatórios.
  5. Deixar vazio o campo obrigatório escolhido.
  6. Tentar salvar ou utilizar o endereço.
  7. Observar a mensagem e o impedimento apresentado.

- Resultado esperado: o sistema deve identificar a pendência
  e impedir a aceitação do endereço incompleto.

- Resultado obtido: [informar o campo testado, a mensagem
  exibida e se o endereço incompleto foi impedido de ser aceito].

- Status: PASS

- Evidência: ![Validação de campo obrigatório](../evidencias/CT11-campo-obrigatorio.png)

- Issue, se houver: não se aplica

- Observações: ocultar dados pessoais na evidência.
  Nenhum pedido deve ser confirmado.
evidencias/CA11.png

### CT12 — Consistência das informações no checkout

- Requisito: RF06
- Critério: CA12


- Pré-condições:
  - Usuário autenticado em conta própria.
  - Uma unidade do Box — Dom Quixote selecionada para compra.
  - Endereço válido disponível.
  - Acesso à revisão anterior à confirmação do pedido.

- Dados utilizados:
  - Produto: Box — Dom Quixote.
  - Autor: Miguel de Cervantes.
  - Formato selecionado: capa dura.
  - Quantidade: 1 unidade.
  - Vendedor: O Antiquário.
  - Valor dos itens: R$ 201,92.
  - Frete: R$ 23,02.
  - Total apresentado: R$ 224,94.
  - Previsão de entrega exibida: de 2 a 4 de dezembro de 2026.

- Passos executados:
  1. Acessar o checkout com uma unidade do produto selecionado.
  2. Conferir as informações de entrega e os valores apresentados.
  3. Acessar a revisão anterior à confirmação do pedido.
  4. Conferir o produto e a quantidade.
  5. Conferir o valor dos itens, o frete e o total.
  6. Comparar o total apresentado com o cálculo manual.
  7. Registrar as evidências sem acionar o botão
     de confirmação do pedido.

- Resultado esperado: as informações do produto selecionado
  e da quantidade devem permanecer consistentes no checkout.
  O total deve corresponder ao valor dos itens acrescido
  do frete e de outros ajustes explicitamente apresentados.

- Cálculo realizado:
  - Itens: R$ 201,92 × 1 = R$ 201,92.
  - Frete: R$ 23,02.
  - Total esperado: R$ 201,92 + R$ 23,02 = R$ 224,94.
  - Total apresentado: R$ 224,94.

- Resultado obtido: o checkout apresentou uma unidade do
  Box — Dom Quixote, de Miguel de Cervantes, vendido por
  O Antiquário, com valor de R$ 201,92.
  O frete apresentado foi de R$ 23,02 e o total de R$ 224,94,
  correspondente ao cálculo manual.

- Status: PASS

- Evidências:
  evidencias/CA12.png

- Issue, se houver: não se aplica.

- Observações:
  - Neste teste foi utilizada uma unidade do Box — Dom Quixote,
    capa dura, diferentemente das duas unidades de capa comum
    utilizadas no CT07.
  - O teste encerra na revisão, antes da confirmação da compra.
  - Ocultar dados pessoais e informações do cartão nas evidências.
