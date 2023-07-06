# TesteBeAnalytic
Repositório destinado à solução do desafio da vaga de engenheiro de dados JR na BeAnalytic

# Resumo do código Python
Este código foi feito em 2 partes. São elas, Extração, integração. Abaixo uma breve descrição de cada fase do processo.


# Extração de dados
Bibliotecas - Para a realização da tarefa, foram utilizadas as bibliotecas Pandas, BS4 e Requests.

Ao tentar consultar os dados da url enviada no teste (https://steamdb.info/sales/), percebi que a variavel que deveria conter o HTML da página veio em branco. Para compreender melhor a situação, emulei o google chrome via Selenium e vi que o CloudFlare estava bloqueando meu acesso aos dados da página. Estudando a fundo o site, ví que eles não permitiam nenhuma espécie de scrap. Então resolví buscar maneiras de acessar a página como se fosse um usuário, a primeira coisa que veio a mente foi usar os mesmos headers que eu passo quando faço a requisição para ver a página. Uma vez que isso foi feito, conseguí extrair o HTML da página e assim extrair os dados desejados.


# Integração dos dados
Bibliotecas - Foram utilizadas as bibliotecas  google-cloud-bigquery e pandas-gbq.

Para Integrar os dados, optei por fazer diretamente em código. Criando minhas credenciais através de um arquivo de credenciais do próprio google big query (GBQ). Uma vez que a credencial é aceita, basta especificar a area de trabalho e a base de dados que desejo integrar, e aguardar*.

*: Devido à falta de tempo, tive um problema de autenticação com o GBQ e não consegui resolver. Então optei por salvar o Data Frame como CSV e importar manualmente via interface do GBQ.


# Link para o Sheets
  https://docs.google.com/spreadsheets/d/1zIuL62Bsx-uFqzDENKfQiIruIChpuFdcsUM9AkfOogs/edit?usp=sharing


