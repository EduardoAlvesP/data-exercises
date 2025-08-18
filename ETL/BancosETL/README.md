# ETL de Capitalização de Mercado de Bancos Globais

## Visão Geral

Este projeto Python implementa um pipeline de **ETL (Extract, Transform, Load)** para processar dados sobre os maiores bancos do mundo. O script extrai dados de uma página da Wikipédia, transforma os valores de capitalização de mercado em várias moedas (Libras Esterlinas, Euros e Rúpias Indianas) e carrega o resultado em um arquivo CSV e em um banco de dados SQLite. O projeto utiliza bibliotecas populares como `pandas`, `requests` e `BeautifulSoup` para a manipulação dos dados.

## Funcionalidades

- **Extração (`Extract`):** Coleta informações de bancos e suas respectivas capitalizações de mercado em USD de uma página da Wikipédia.
- **Transformação (`Transform`):** Converte a capitalização de mercado de USD para GBP, EUR e INR usando taxas de câmbio de um arquivo CSV.
- **Carregamento (`Load`):** Salva o DataFrame final em um arquivo CSV e em um banco de dados SQLite.
- **Registro (`Logging`):** Acompanha o progresso da execução do pipeline em um arquivo de log, registrando o início e o fim de cada etapa.
- **Consultas SQL:** Executa e exibe o resultado de consultas SQL no banco de dados para verificar os dados carregados.

---

## Estrutura do Projeto

- `etl_project.py`: O script principal que contém as funções de ETL e a lógica de execução.
- `exchange_rate.csv`: Arquivo CSV com as taxas de câmbio para a transformação dos dados.
- `code_log.txt`: Arquivo de log gerado pelo script.
- `Largest_banks_data.csv`: Arquivo CSV de saída com os dados transformados.
- `Banks.db`: Banco de dados SQLite de saída com a tabela `Largest_banks`.

---

## Pré-requisitos

Para rodar este projeto, você precisará ter as seguintes bibliotecas Python instaladas. Você pode instalá-las usando o `pip`:

```bash
pip install pandas requests beautifulsoup4 numpy