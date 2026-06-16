# Desafio: Processamento e Validação de Transações Financeiras

## 🚀 Sobre o Projeto
Este projeto foi desenvolvido como um desafio técnico para processamento de dados utilizando Python. O fluxo consiste em criar uma massa de dados, realizar a limpeza e validação de registros (tratando erros silenciosamente) e gerar um relatório gerencial mensal.

O projeto foi construído e testado no **Google Colab**, utilizando módulos nativos do Python para garantir portabilidade.

## 📂 Estrutura do Notebook (`.ipynb`)
O notebook está organizado de forma modular, facilitando a execução passo a passo:

1. **Geração de Dados**: Criação automática do arquivo `transacoes.csv` com dados válidos e inválidos (IDs corrompidos, tipos errados, etc.).
2. **Leitura e Validação**: Utilização de `csv.DictReader` com tratamento de exceções para filtrar apenas transações íntegras.
3. **Processamento (Regras de Negócio)**: Agrupamento mensal, cálculo de métricas (saldo, média, picos) e identificação de transações suspeitas (> R$ 10.000,00).
4. **Exibição**: Relatório formatado em console seguindo o padrão monetário brasileiro.

## 🛠 Tecnologias
* **Ambiente**: Google Colab (Jupyter Notebook)
* **Linguagem**: Python 3.x
* **Bibliotecas**: `csv`, `datetime`, `os` (Todas nativas)

## ⚙️ Como executar no Colab
1. Abra o arquivo `.ipynb` no seu [Google Colab](https://colab.research.google.com/).
2. Execute as células sequencialmente.
3. O script gerará automaticamente o arquivo `transacoes.csv` no sistema de arquivos do Colab (barra lateral esquerda, ícone de pasta).
4. O relatório final será exibido logo abaixo da última célula de processamento.

## 📊 Exemplo de Saída
O relatório é gerado dinamicamente para todos os meses presentes nos dados:

```text
===== RELATÓRIO MENSAL =====
Mês: 2026-01
  Transações: 2
  Total crédito: R$ 3.500,00
  Total débito:  R$ 180,50
  Saldo:         R$ 3.319,50
  Média:         R$ 1.840,25
  Maior valor:   R$ 3.500,00
  Menor valor:   R$ 180,50
