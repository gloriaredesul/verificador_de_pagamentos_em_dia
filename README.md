
# 📊 Análise de Pagamentos em Dia

Este notebook foi criado para **automatizar a conferência das datas de pagamento de boletos**, com o objetivo de verificar se o cliente manteve seu benefício ativo naquele período.

## 🧾 Contexto

Em muitas empresas, especialmente nas áreas de **saúde, educação, seguros ou programas de fidelidade**, a manutenção de um **benefício ou acesso a serviços** está condicionada ao pagamento **em dia** de uma cobrança.

Contudo, em alguns casos, o que define esse pagamento “em dia” **não é a data exata do vencimento**, mas sim o **mês em que o pagamento foi realizado**.

📌 **Regra de negócio aplicada**:  
> Se o pagamento for realizado **dentro do mesmo mês e ano** do vencimento do boleto, o cliente ainda é considerado **adimplente**, mesmo que tenha pago com alguns dias de atraso.  
Isso significa que o benefício permanece **ativo no mês da cobrança**.

## 🛠️ O que o notebook faz

Este notebook permite:

1. Fazer upload de uma planilha `.xlsx` ou `.csv` com as colunas:
   - `Vencimento`: data original do boleto
   - `Pagamento`: data em que o boleto foi efetivamente pago

2. O código processa os dados e **compara o mês e o ano** do vencimento com os do pagamento.

3. Gera uma nova coluna chamada `pagamento_em_dia`, com valores `True` ou `False`.

4. Exibe apenas os pagamentos considerados **em dia** de acordo com a regra descrita.

## 📂 Exemplo de planilha

| Vencimento | Pagamento   |
|------------|-------------|
| 2024-03-05 | 2024-03-10  |
| 2024-04-10 | 2024-05-01  |
| 2024-05-15 | 2024-05-25  |

Neste exemplo, o segundo registro seria considerado **fora do prazo**, pois o pagamento foi feito **em outro mês**.

## 🧠 Benefícios da automação

- Evita análise manual e repetitiva de datas;
- Reduz erros operacionais;
- Garante a aplicação correta de regras de negócio;
- Facilita a geração de relatórios de adimplência.

## 🚀 Como usar

1. Abra o notebook no Google Colab;
2. Faça o upload da planilha;
3. O notebook exibirá os registros considerados em dia segundo os critérios definidos.

---

Desenvolvido para auxiliar equipes de atendimento, financeiro, suporte e análise de dados na **verificação rápida e segura da adimplência de clientes**.

```

