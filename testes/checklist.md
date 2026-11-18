- [ x ] A busca válida apresenta o produto procurado.
- [ x ] A busca sem correspondência apresenta resposta compreensível.
- [ x ] A página de detalhes identifica a oferta selecionada.
- [ x ] O item correto é adicionado ao carrinho.
- [ x ] A quantidade pode ser alterada de 1 para 2.
- [ x ] O limite inferior de quantidade é respeitado.
- [ x ] O subtotal corresponde aos itens selecionados.
- [ x ] O carrinho mantém seu estado após atualizar a página.
- [ x ] A exclusão remove o item e atualiza o carrinho.
- [ x ] O checkout exige identificação quando necessário.
- [ x ] O endereço incompleto gera indicação de campo obrigatório.
- [ x ] As informações acessíveis no checkout são consistentes.

| Verificação | Caso relacionado | Resultado | Evidência / observação |

| Busca válida | CT01 | A confirmar | Foi definido o termo “Dom Quixote Nova Fronteira”, mas o resultado da execução não foi apresentado nesta conversa. |
| Busca sem correspondência | CT02 | PASS | A aplicação exibiu “Nenhum resultado para sua consulta de pesquisa” e apresentou recomendações em seção separada. |
| Detalhes do produto | CT03 | PASS | A página identificou o Box — Dom Quixote, de Miguel de Cervantes, editora Nova Fronteira, capa dura, com preço e condições da oferta. |
| Inclusão no carrinho | CT04 | PASS | A aplicação confirmou a inclusão. Capturas posteriores mostraram o Box — Dom Quixote, capa dura, com uma unidade no carrinho. |
| Alteração da quantidade | CT05 | PASS | O produto alternativo Caixa Dom Quixote, capa comum, apresentou duas unidades. A tentativa com o Box de capa dura foi impedida por estoque de apenas 	uma unidade, com mensagem explicativa. |
| Limite mínimo de quantidade | CT06 | PASS | Com uma unidade, a interface apresentou uma lixeira no lugar do botão de diminuir, oferecendo exclusão em vez de quantidade inferior ao mínimo. |
| Cálculo do subtotal | CT07 | PASS | Duas unidades de Caixa Dom Quixote a R$ 86,54 totalizaram R$ 173,08, exatamente o subtotal exibido. O Box de capa dura já havia sido removido. |
| Persistência após atualizar | CT08 | A confirmar | Falta registrar o resultado da atualização da página e comparar os itens e quantidades antes e depois. |
| Remoção do carrinho | CT09 | Parcialmente comprovado | A captura do CT07 exibiu a mensagem de remoção do Box — Dom Quixote. A remoção foi comprovada, mas o cenário de carrinho vazio ainda 	não foi demonstrado, pois outro produto permaneceu nele. |
| Autenticação no checkout | CT10 | A confirmar | O procedimento em janela anônima foi orientado, mas não foi apresentada a tela ou confirmação do resultado observado. |
| Campo obrigatório do endereço | CT11 | A confirmar | O procedimento foi orientado, mas falta registrar o campo deixado vazio, a mensagem exibida e o impedimento de aceitar o endereço 	incompleto. |
| Consistência no checkout | CT12 | PASS | A revisão apresentou uma unidade do Box — Dom Quixote por R$ 201,92, frete de R$ 23,02 e total de R$ 224,94, consistente com o cálculo manual. |