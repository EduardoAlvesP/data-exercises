#ETL: Extração, Transformação e Carga de Dados de Veículos

Este repositório contém um script Python simples para demonstrar um processo de ETL (Extract, Transform, Load). O objetivo é coletar dados de veículos de diferentes formatos (CSV, JSON, XML), padronizá-los e, em seguida, salvá-los em um único arquivo CSV transformado, além de registrar o progresso da operação.

---

## Funcionalidades

O script realiza as seguintes etapas:

1.  **Extração (Extract):**
    * Lê dados de todos os arquivos `.csv`, `.json` e `.xml` presentes no mesmo diretório do script (exceto o arquivo de saída `transformed_data2.csv`).
    * Os dados são combinados em um único DataFrame Pandas.
    * Campos extraídos: `car_model`, `year_of_manufacture`, `price`, `fuel`.

2.  **Transformação (Transform):**
    * Arredonda a coluna `price` para duas casas decimais.

3.  **Carga (Load):**
    * Salva o DataFrame transformado em um novo arquivo CSV chamado `transformed_data2.csv`.

4.  **Log de Progresso:**
    * Registra o início e fim de cada fase do ETL (Extract, Transform, Load) em um arquivo de log (`log_file2.txt`), incluindo um timestamp para cada evento.

---

## Tecnologias Utilizadas

* **Python 3**
* **Pandas:** Para manipulação e análise de dados.
* **xml.etree.ElementTree:** Para parsing de arquivos XML.
* **glob:** Para encontrar arquivos por padrão no diretório.

---

## Como Executar

Para rodar este script, siga os passos abaixo:

1.  **Pré-requisitos:** Certifique-se de ter Python 3 e a biblioteca Pandas instalados. Se não tiver o Pandas, pode instalar via pip:
    ```bash
    pip install pandas
    ```

2.  **Prepare os dados de entrada:** Crie arquivos `.csv`, `.json` e `.xml` com dados de veículos no *mesmo diretório* onde o script Python está.
    * **Exemplo `cars.csv`:**
        ```csv
        car_model,year_of_manufacture,price,fuel
        Toyota Corolla,2020,25000.758,Gasoline
        Honda Civic,2019,22000.123,Gasoline
        ```
    * **Exemplo `cars.json`:**
        ```json
        {"car_model": "Ford Focus", "year_of_manufacture": "2021", "price": 28000.987, "fuel": "Gasoline"}
        {"car_model": "Chevrolet Onix", "year_of_manufacture": "2022", "price": 18000.456, "fuel": "Flex"}
        ```
    * **Exemplo `cars.xml`:**
        ```xml
        <collection>
            <car>
                <car_model>Volkswagen Golf</car_model>
                <year_of_manufacture>2018</year_of_manufacture>
                <price>19000.321</price>
                <fuel>Gasoline</fuel>
            </car>
            <car>
                <car_model>Fiat Mobi</car_model>
                <year_of_manufacture>2023</year_of_manufacture>
                <price>12000.678</price>
                <fuel>Flex</fuel>
            </car>
        </collection>
        ```

3.  **Execute o script:**
    Abra seu terminal ou prompt de comando, navegue até o diretório onde você salvou o script e os arquivos de dados, e execute:
    ```bash
    python seu_script_etl.py
    ```
    (Substitua `seu_script_etl.py` pelo nome do seu arquivo Python, por exemplo, `etl_pipeline.py`)

---

## Saídas Geradas

Após a execução bem-sucedida, dois novos arquivos serão gerados no mesmo diretório:

* `transformed_data2.csv`: Contém todos os dados extraídos de CSV, JSON e XML, com os preços arredondados para duas casas decimais.
* `log_file2.txt`: Registra os timestamps e mensagens de progresso de cada etapa do processo ETL.

---

