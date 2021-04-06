# Backend Engineer Test

Este repositório serve como case para avaliação técnica para a posição de backend

## Case

Na Monis nós trabalhamos com _user story_ para definir as melhorias do nosso produto; Este case é um exemplo de um card com uma "nova feature" para o nosso produto. Você reescreverá "parte" do nosso sistema 😁

### Story #: Criar uma API para calculo de saldo dos usuários Monis

**Notas**:

- Nossos usuários possuem assinaturas que são debitadas semanalmente de seus cartões de crédito;
- Essas assinaturas são armazenadas como _transações_ em nosso banco de dados;
- Todas as transações rendem 100% do [CDI](https://www.infomoney.com.br/guias/cdi/) (Este link leva à um artigo explicando sobre CDI);
- Cada transação começa a render assim que ela é concluída até a data atual;
- Os rendimentos são diários;
- Existe uma API do [Banco Central](https://api.bcb.gov.br/dados/serie/bcdata.sgs.11/dados?formato=json) para pegar as taxas de cada dia;

**Critérios de Aceite**

- Não se preocupar com autenticação, foque apenas na regra de negócio (Calcular o saldo atual);
- Deve haver um endpoint para "calcular" o saldo atual do usuário;
- O endpoint de calculo deve trazer em detalhes: saldo atual (total em transações + rendimentos), total em transações e somente rendimento;
- Deve haver um endpoint para "calcular" o rendimento de apenas uma transação;
- Cada transação deve render desda data em que foi criada até a data de hoje;
- Utilizar `transactions.json` como referência de banco de dados de transação;
