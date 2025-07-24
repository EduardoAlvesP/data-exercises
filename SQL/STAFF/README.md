# Script de Exemplo: Manipulacao de Dados com Pandas e SQLite
---

Este script Python eh um exercicio que demonstra como ler dados de arquivos CSV, criar e popular tabelas em um banco de dados SQLite (STAFF.db), e realizar algumas consultas basicas usando a biblioteca `pandas`.

---

## Como Rodar
---

1.  **Pre-requisitos**: Certifique-se de ter Python e a biblioteca Pandas instalada (`pip install pandas`).

2.  **Arquivos CSV**: Coloque `INSTRUCTOR.csv` e `Departments.csv` no **mesmo diretorio** do script.
    * Eles devem ser **sem cabecalho**, com os seguintes formatos:
        * `INSTRUCTOR.csv`: `ID,FNAME,LNAME,CITY,CCODE`
        * `Departments.csv`: `DEPT_ID,DEP_NAME,MANAGER_ID,LOC_ID`

3.  **Caminhos (Colab/Online)**: Se estiver usando o Google Colab ou ambiente similar, os caminhos dos arquivos no script devem ser `/content/INSTRUCTOR.csv` e `/content/Departments.csv` apos o upload.

4.  **Execucao**: Abra o terminal no diretorio do script e execute:
    ```bash
    python seu_script.py
    ```
    (Substitua `seu_script.py` pelo nome do seu arquivo Python.)

---

## O que o Script Faz
---

* Cria um arquivo de banco de dados `STAFF.db`.
* Le `INSTRUCTOR.csv` e `Departments.csv` para DataFrames.
* Cria e popula as tabelas `INSTRUCTOR` e `Departments` no `STAFF.db`.
* Adiciona um registro de exemplo em cada tabela.
* Executa e mostra os resultados de algumas consultas SQL (`SELECT *`, `SELECT FNAME`, `SELECT COUNT(*)`).
* Fecha a conexao com o banco de dados.