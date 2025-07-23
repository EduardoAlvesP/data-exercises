Script de Extração de Dados de Filmes (Top 25)
Este script em Python realiza web scraping para extrair informações dos 25 filmes mais bem ranqueados de uma página web, organiza esses dados em um DataFrame do Pandas e, em seguida, os salva em um arquivo CSV e em um banco de dados SQLite. Ele também demonstra a filtragem de filmes lançados a partir do ano 2000.

🚀 Como Usar
Para rodar este código, você precisará ter o Python instalado e as bibliotecas listadas nos requisitos.

Baixe o Código:
Salve o arquivo webscaping_movies.py (ou o nome que você deu ao seu script) no seu computador.

Instale as Dependências:
Abra seu terminal ou prompt de comando e execute o seguinte comando para instalar as bibliotecas necessárias:

Bash

pip install requests pandas beautifulsoup4
Execute o Script:
No seu terminal, navegue até o diretório onde você salvou o arquivo e execute-o:

Bash

python3 webscaping_movies.py
✨ Funcionalidades
Extração de Dados: Coleta os 25 primeiros filmes de uma tabela específica em uma página da Everybodywiki.

Processamento com Pandas: Organiza os dados extraídos em um DataFrame do Pandas para fácil manipulação e análise.

Limpeza de Dados: Converte a coluna 'Year' (Ano) para um formato numérico, tratando possíveis erros e garantindo a integridade dos dados para operações matemáticas.

Filtragem: Demonstra como filtrar o DataFrame para exibir apenas os filmes lançados no ano 2000 ou posterior.

Armazenamento:

Salva o DataFrame completo em um arquivo CSV (top_25_films.csv).

Armazena os dados em um banco de dados SQLite (Movies.db), criando ou substituindo uma tabela chamada Top_25.

📊 Estrutura dos Dados
O DataFrame gerado e os dados salvos contêm as seguintes colunas:

Average Rank: A classificação média do filme.

Film: O título do filme.

Year: O ano de lançamento do filme (convertido para número inteiro).

Rotten Tomatoes' Top 100: A classificação do filme na lista Top 100 do Rotten Tomatoes.

⚠️ Observações Importantes
Ambientes em Nuvem (Google Colab, etc.): Se estiver rodando o código em um ambiente como o Google Colab, certifique-se de ajustar o csv_path para um diretório acessível (ex: /content/) e lembre-se que os arquivos gerados são temporários e precisarão ser baixados se quiser guardá-los.

🛠️ Tecnologias Utilizadas
Python 3

Requests: Para fazer requisições HTTP e obter o conteúdo da página web.

BeautifulSoup4: Para parsear o HTML e extrair os dados.

Pandas: Para manipulação e análise de dados tabulares (DataFrames).

SQLite3: Para armazenar os dados em um banco de dados local.