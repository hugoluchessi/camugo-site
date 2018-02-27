# README	
Esse site é propriedade de CAMUGO Acessórios para móveis. Feito com [Jekyll](https://jekyllrb.com).

## Instalação
Instale a gema do Jekyll
```
gem install jekyll bundler
```

Para executar o site após clonar o repositório
```
bundle exec jekyll serve
```

Acesse 
`http://127.0.0.1:4000/camugo-site/`  para visualizar o site gerado

## Configuração
Para remover o subdiretório `camugo-site` , entre no arquivo `_config.yml` e altere a `baseurl` 

## Páginas do site
Cada página presente no site possui um arquivo `.md` localizado na raiz do repositório:
```
about.md
contact.md
index.md
partners.md
products.md
```

Dentro de cada arquivo *.md* existe o parâmentro `layout:` para definir qual é o layout onde será exibido o conteúdo do markdown. 

Os layouts se encontram dentro de `_layouts`


## Adicionando Produtos
As principais categorias de produtos é um item de uma [Collection](https://jekyllrb.com/docs/collections/) do Jekyll e  se encontram no diretório `_categorias`
Cada um dos arquivos `.md` adicionados nesse diretório será utilizado na página principal e na página de resultados para exibir os filtros de busca. 

Os produtos também são uma [Collection](https://jekyllrb.com/docs/collections/) localizados no diretório `_products` 

Para adicionar um novo produto, adicione um arquivo `.md`dentro do diretório `_products`. O produto será exibido com base nos parâmetros seguintes:
```
---
    layout: product
    title: Nome do Produto
    partner: Nome do fornecedor
    categories: Categoria (titulo da categoria de acordo com o título do arquivo da collection Categories)      
    subcategory: subcategoria
    description: "descrição do produto"
    images: 
      - title: Título da imagem do produto
        image_path: image_path.jpg
---

Conteúdo da página com markdown

```


No parâmetro `images` é possível incluir várias imagens para criar a galeria:

```
images: 
   - title: Imagem 1
     image_path: /assets/img/image_path.jpg
 	 - title: Imagem 2
     image_path: image_path.jpg
 	 - title: Imagem 3
     image_path: image_path.jpg
```

