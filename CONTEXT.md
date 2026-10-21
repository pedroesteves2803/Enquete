# Enquetes

Este contexto permite criar enquetes públicas, coletar votos e publicar seu resultado após o encerramento.

## Language

**Criador**:
Qualquer pessoa que acessa a rota pública de criação e gera uma Enquete. Não pressupõe uma conta autenticada.
_Avoid_: Admin, usuário autenticado

**Enquete**:
Uma consulta pública, limitada no tempo, que apresenta alternativas para receber uma escolha de cada votante.
_Avoid_: Pesquisa, formulário

**Votante**:
Pessoa que registra uma escolha em uma Enquete pública. É identificada apenas por um identificador persistente do navegador, que reduz votos casuais repetidos sem constituir proteção antifraude.
_Avoid_: Usuário autenticado, eleitor verificado

**Voto**:
A escolha única de uma Alternativa por um Votante em uma Enquete.
_Avoid_: Resposta

**Alternativa**:
Uma opção de escolha apresentada por uma Enquete. Uma Enquete tem pelo menos duas Alternativas, cujos textos são distintos e não mudam depois do primeiro Voto.
_Avoid_: Opção, resposta

**Encerramento**:
O instante em que uma Enquete deixa de aceitar Votos, seja ao alcançar a data definida em horário de São Paulo, seja por encerramento antecipado e irreversível do Criador. O servidor recusa o Voto mesmo que o Votante tenha aberto a página antes desse instante.
_Avoid_: Prazo flexível

**Resultado**:
A apuração final dos Votos por Alternativa, pública do Encerramento até a exclusão da Enquete ao fim da Retenção.
_Avoid_: Parcial, placar ao vivo

**Link de Administração**:
Link não adivinhável, entregue ao Criador uma única vez, que permite administrar uma Enquete sem exigir conta. Expira dois dias após o Encerramento.
_Avoid_: Login, painel público

**Retenção**:
Período de dois dias após o Encerramento em que a Enquete e seu Resultado permanecem acessíveis. Ao fim do período, todos os dados da Enquete, suas Alternativas e seus Votos são excluídos e deixam de ser acessíveis.
_Avoid_: Arquivamento, histórico permanente
