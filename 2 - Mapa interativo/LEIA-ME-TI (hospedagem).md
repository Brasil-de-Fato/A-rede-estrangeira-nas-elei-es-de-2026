# Mapa interativo "A rede estrangeira": instruções de hospedagem

## O que é

Duas páginas HTML estáticas, uma por idioma. Cada uma é um arquivo único e autossuficiente: o código (JavaScript e
CSS), a biblioteca de gráficos D3, as fontes, as fotos e os dados vão todos dentro do arquivo.

| Arquivo | Idioma | Tamanho | Com gzip |
|---|---|---|---|
| `mapa-rede-2026.html` | português | 3,0 MB | 1,7 MB |
| `foreign-network-map-2026.html` | inglês | 3,0 MB | 1,7 MB |

Não há back-end, banco de dados, etapa de build nem dependência de CDN. A página não faz nenhuma requisição de rede ao
carregar nem durante o uso; isso foi testado com todas as requisições externas bloqueadas. Só há tráfego externo quando
o leitor clica num link de fonte, que abre em nova aba.

## Como publicar

1. Copie os dois arquivos para qualquer servidor ou serviço de páginas estáticas (Apache, Nginx, S3/CloudFront, Netlify,
   o próprio CMS como arquivo anexo, etc.). Os nomes podem ser trocados livremente, por exemplo `/mapa/index.html` e
   `/en/map/index.html`.
2. Sirva com `Content-Type: text/html; charset=utf-8`.
3. Ative gzip ou brotli para HTML. Isso reduz a transferência de 3 MB para cerca de 1,7 MB.
4. Cache: como o nome do arquivo não muda quando o mapa for atualizado, use um cache curto (por exemplo,
   `Cache-Control: max-age=3600`) ou acrescente `?v=AAAAMMDD` aos links que apontam para a página.

Recomendamos publicar como **página própria (tela cheia)**. O layout ocupa toda a janela e foi feito para isso; também
funciona em celular.

### Se for preciso embutir numa página existente (iframe)

```html
<iframe src="/mapa/index.html" title="A rede estrangeira: mapa interativo"
        style="width:100%;height:90vh;min-height:680px;border:0"
        allow="clipboard-write" loading="lazy"></iframe>
```

`allow="clipboard-write"` é necessário para o botão "Compartilhe", que copia o link. Dentro de um iframe, o link
copiado é o do próprio arquivo do mapa.

## Política de segurança (CSP) testada

A página usa script e estilo embutidos (inline), imagens e fontes em `data:` e, na exportação de PNG, URLs `blob:`.
A política abaixo foi testada com a página completa, incluindo busca, fotos, painéis e "Gerar imagem", sem erros:

```
Content-Security-Policy: default-src 'none'; script-src 'unsafe-inline'; style-src 'unsafe-inline'; img-src data: blob:; font-src data:; connect-src 'none'; base-uri 'none'; form-action 'none'
```

Se o site acrescentar ferramentas próprias, como analytics, amplie a política para os domínios delas. Para controlar
quem pode embutir a página, defina `frame-ancestors`.

## Privacidade

A página não usa cookies e não tem analytics. O único dado guardado no navegador é a escolha de tema claro ou escuro,
no `localStorage`, chave `tema-rede`. Os links externos saem com `rel="noopener"`, e a página declara
`<meta name="referrer" content="no-referrer">`.

## Links diretos (para redes sociais e matérias)

O estado do mapa fica no endereço, depois do `#`:

| Exemplo | Abre |
|---|---|
| `…/mapa/#n=eduardo-bolsonaro` | o painel de Eduardo Bolsonaro |
| `…/mapa/#v=circulos` | a vista em círculos |
| `…/mapa/#r=historia:parscale` | uma das histórias guiadas |
| `…/mapa/#r=frente:23` | uma frente de pesquisa (aqui, Israel) |
| `…/mapa/#r=completa` | a rede completa |

O botão "Compartilhe" copia o link do estado atual.

## Navegadores

Testado no Chromium, no computador e numa tela de celular simulada (390 px). A página usa só recursos padrão da web, suportados pelas versões atuais de Chrome, Edge, Firefox e Safari, mas vale uma conferência rápida no Safari do iPhone e no Firefox antes de divulgar. A busca abre com a tecla `/`.

## Licenças e créditos (pasta `licencas/`)

- **D3 7.9.0**, licença ISC: `licencas/d3-ISC.txt`. O aviso de copyright também vai dentro do HTML.
- **Fontes Rajdhani e Cormorant**, SIL Open Font License 1.1: `licencas/OFL-*.txt`. Vão embutidas como subconjunto
  latino.
- **198 retratos** da Wikimedia Commons, todos com licença livre (domínio público, CC BY ou CC BY-SA). Cada foto
  traz autor, licença e link no painel do nome dentro do mapa; a lista completa está em `licencas/creditos-fotos.csv`.
  Se for reaproveitar alguma foto fora do mapa, mantenha o crédito e a licença indicados.

Recomendamos publicar a pasta `licencas/` junto, ou pelo menos manter acessíveis os textos de licença das fontes e do D3.

## Atualizações

O mapa é gerado a partir dos dados da pesquisa. Uma atualização chega como novos arquivos HTML com os mesmos nomes;
basta substituir os arquivos publicados e invalidar o cache.
