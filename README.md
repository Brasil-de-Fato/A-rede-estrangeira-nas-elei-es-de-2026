# A rede estrangeira nas eleições de 2026

Investigação em fontes abertas sobre a rede internacional de pessoas, organizações e dinheiro em torno da
candidatura de Flávio Bolsonaro à Presidência do Brasil em 2026: o que foi oferecido ao governo dos Estados
Unidos e não ao eleitor, quem financia a rede e quem paga a conta.

**[Abrir o mapa interativo](https://brasil-de-fato.github.io/A-rede-estrangeira-nas-elei-es-de-2026/)** · [English summary](#english-summary)

> Dados atualizados até **23 de outubro de 2026**, dois dias antes do 2º turno. Fatos posteriores não
> estão no material.

## O que há neste repositório

| Pasta | Conteúdo |
|---|---|
| [`1 - Relatório`](1%20-%20Relatório) | O relatório completo (179 páginas, nove capítulos), em português e inglês, em `.docx` (para editar e citar) e `.pdf` (para leitura). As notas de rodapé indicam a fonte de cada fato, com link. |
| [`2 - Mapa interativo`](2%20-%20Mapa%20interativo) | Mapa navegável da rede, em português (`mapa-rede-2026.html`) e inglês (`foreign-network-map-2026.html`). Cada laço traz a fonte em que foi lido. A pasta `licencas` reúne os créditos das fotos e as licenças das fontes tipográficas e da biblioteca D3. |
| [`3 - Painel`](3%20-%20Painel) | Resumo visual em 4 páginas, em PDF e em PNG, por idioma. |
| `LEIA-ME.txt` | Guia do material e cuidados na hora de publicar. |

### Os nove capítulos do relatório

1. **O programa escondido.** O que foi entregue ao Escritório do Representante Comercial dos EUA (USTR) em
   1º de julho de 2026 e o que o programa registrado no TSE diz sobre os mesmos temas: Pix, Mercosul,
   cartões, etanol e China.
2. **Da via encoberta à franquia.** As formas da intervenção americana no Brasil de 1962 a 2026, até o
   modelo de conferências licenciadas (CPAC Brasil).
3. **O circuito do dinheiro.** Fundo Partidário, a Gettr e o dinheiro de Guo Wengui, o Banco Master e o
   filme "Dark Horse", e empresas ligadas a Abu Dhabi.
4. **O que está em jogo.** Tarifas de cartão, terras raras (Serra Verde, em Minaçu-GO) e concessões
   estaduais.
5. **A contradição China.** O agronegócio que financia a campanha e vende a maior parte da soja à China.
6. **A coerção.** Tarifas, sanções Magnitsky, vistos e verbas do Departamento de Estado.
7. **Israel, o Golfo e a Iberosfera.** Os polos secundários da rede.
8. **A máquina de informação.** Da tese de fraude nas urnas em 2022 às cotações de apostas apresentadas
   como pesquisa em 2026.
9. **O que é a rede.** A leitura de conjunto, quem paga a conta e as perguntas que seguem abertas.

## Como foi feito

O material usa apenas fontes abertas: documentos oficiais do Brasil e dos EUA (Federal Register, USTR,
Tesouro, SEC, TSE), processos judiciais, registros de empresas, reportagens e estudos acadêmicos. Cada fato
remete, em nota, ao documento ou à reportagem de origem. Quando o texto interpreta, ele deve dizer que é uma
interpretação; as acusações feitas em processos são tratadas como acusações, e as negativas dos citados
estão registradas.

Os números do mapa e da página 1 do painel (431 atores estrangeiros, 816 vínculos, 32 países) contam apenas
pessoas e organizações de fora do Brasil e apenas vínculos que constam de alguma fonte.

## Leia com cuidado

- **Acusação não é condenação.** Os casos citados estão em fases diferentes: há condenados, denunciados,
  indiciados, investigados e pessoas sem nenhuma acusação. Ao citar ou recortar, mantenha essa distinção.
- **Um laço no mapa não indica crime.** Alinhamento político aberto, financiamento ilegal e operação
  encoberta são coisas diferentes. O mapa registra vínculos que aparecem em fontes, não intenções.
- **Hipóteses são hipóteses.** Por exemplo, a suspeita de que um fundo do Texas pagou a estadia de Eduardo
  Bolsonaro nos EUA é hipótese da Polícia Federal, e ele a nega.
- **Confira na fonte.** Antes de reproduzir qualquer fato, abra a nota e leia o documento original.

## Perguntas em aberto

O relatório termina com perguntas que os documentos públicos ainda não respondem, entre elas:

- Quem redigiu o documento de 86 páginas entregue ao USTR?
- Quem são os donos da Rockbridge Brazil LLC, aberta em Wyoming em 12 de maio de 2026?
- Quem vai receber o US$ 1 milhão empenhado pelo Departamento de Estado para o Brasil?
- Quem pagou os posts estrangeiros que apresentaram cotações de apostas como pesquisa eleitoral?

## Mapa interativo

O mapa é uma página HTML estática e autossuficiente: código, dados, fontes e fotos vão dentro do arquivo.
Ele não faz requisições de rede, não usa cookies nem analytics e funciona offline. Para abrir localmente,
basta dar dois cliques no arquivo.

Links diretos (o estado do mapa fica depois do `#`):

| Exemplo | Abre |
|---|---|
| `mapa-rede-2026.html#n=eduardo-bolsonaro` | o painel de uma pessoa |
| `mapa-rede-2026.html#v=circulos` | a vista em círculos |
| `mapa-rede-2026.html#r=completa` | a rede completa |

### Publicação no GitHub Pages

1. Em **Settings → Pages**, escolha **Deploy from a branch**, branch `main`, pasta `/ (root)`.
2. O endereço `https://brasil-de-fato.github.io/A-rede-estrangeira-nas-elei-es-de-2026/` abre o `index.html` da raiz, que leva aos mapas em
   português e em inglês.
3. O arquivo `.nojekyll` faz o GitHub servir os arquivos como estão, sem processamento.

## Licenças e créditos

- **D3 7.9.0**, licença ISC: [`licencas/d3-ISC.txt`](2%20-%20Mapa%20interativo/licencas/d3-ISC.txt).
- **Fontes Rajdhani e Cormorant**, SIL Open Font License 1.1: [`licencas/`](2%20-%20Mapa%20interativo/licencas).
- **198 retratos** da Wikimedia Commons, em domínio público, CC BY ou CC BY-SA. O autor, a licença e o link
  de cada foto estão em
  [`licencas/creditos-fotos.csv`](2%20-%20Mapa%20interativo/licencas/creditos-fotos.csv) e no painel de cada
  nome dentro do mapa. Ao reaproveitar uma foto fora do mapa, mantenha o crédito e a licença.

---

## English summary

An open-source investigation into the international network of people, organizations and money around
Flávio Bolsonaro's 2026 presidential campaign in Brazil: what was offered to the United States government
but not to voters, who funds the network and who pays the bill.

- **Report** (`1 - Relatório/English`): *The Foreign Network in Brazil's 2026 Election*, 179 pages, nine
  chapters, footnoted with links to official documents, court records, company registries, news reports
  and academic studies.
- **Interactive map** (`2 - Mapa interativo/foreign-network-map-2026.html`): a self-contained, offline
  network map; every link cites the source it was read from.
- **Panel** (`3 - Painel`): a four-page visual summary, as PDF and PNG.

Data current as of **23 October 2026**, two days before the runoff. Allegations are not convictions, and a
link on the map does not imply wrongdoing: open political alignment, illegal funding and covert operations
are different things. Check every fact against the cited source before reusing it.
