# tutorial_scrapy
Codigo do tutorial encontrado na documentação do Scrapy com comentários adicionais

Olá novamente...

O framework Scrapy é um framework para estração de dados de páginas da web. Semelhante ao que o Google faz para encontrar o seu e a infinidade de sites pela web.
No tutorial escrito em Inglês do framework, existe um projeto base de teste.
Basicamente ele vai numa URL de um site, extrai os dados de citações famosas do site e gera dois HTML's com os dados extraidos.

Informações relavantes até o momento do projeto:

Dentro do framework existe um classe chamada Spider.
O Scrapy usa essa clase para extrair informações de um site ou grupo de sites.

Durante a criação da subclasse Spider, é definido o "request" inicial, onde opcionalmente você pode informar como o "crawler" irá seguir os links e como ele vai "parsear" a página e extrair os dados do site.
Dentro da subclasse Spider são definidos alguns métodos e atributos.

O atributo "name" 
  É um identificador único para o spider
  Não pode ter mais de um no projeto todo.
O método "start_requests()" é um método que:
  Retorna um interador da classe "Requests"
  Esse interador poder ser uma "generator function"
  Esse interador pode simplesmente ser uma lista de "requests"
  Os "requests" subsequentes são gerados sucessivamente através dos "requests" iniciais
O método "parse()"
  "Parseia" uma instancia da classe "TextResponse"
  O "TextReponse" contém o conteúdo da página
  O "TextResponde" contém métodos úteis para lidar com os dados
  Normalmente o método realiza o "parse" da resposta do site
  O método extrai os dados da pagína como um dict(dicionário)
  Procura novas urls para seguir
  Cria novos "requests(Request)" das novas URLs achadas
