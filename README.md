# ElasticSearch

* Banco de dados orientado a documentos.
* Engine de busca.
* Análise de dados.
* Rápido.
* Escalável.
* API REST.


... falta uma parte inicial do curso.


## Cap 03.

### Campo " all "


GET - /catalog/pessoas/_search?q=futebol

- Quando o elasticsearch salva os dados ele pega todos os atributo e concatena em uma string por exemplo:

```JSON
"nome":"João Silva",
"interesses": ["futebol", "música", "literatura"],
"cidade": "São Paulo",
"formação": "Letras",
"estadio": "SP",
"país": "Brasil"
```

```
"João Silva futebol música literatura São Paulo Letras Brasil"
```

- A busca com all vai ser feita na string concatenada.

- É possível também selecionar um atributo para a busca.

GET - /catalog/pessoas/_search?q=estado:SP

