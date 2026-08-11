# radar-psiq

Agregador de periódicos de alto impacto de psiquiatria, separado por subespecialidade.

**Radar Psiquiatria** é um aplicativo estático (PWA) que consulta o PubMed via
[NCBI E-utilities](https://www.ncbi.nlm.nih.gov/books/NBK25501/) e monta, direto
no navegador, um feed dos artigos mais recentes dos principais periódicos de
psiquiatria do mundo. Não há servidor, cadastro ou banco de dados: todo o
processamento roda no cliente.

## Como funciona

- Cada periódico é consultado pela sua abreviação NLM (campo `[ta]`).
- Os artigos são ordenados por data e classificados em dois níveis a partir do
  título: **subespecialidade** (1º nível, ex.: Transtornos do Humor, Psicoses,
  Adicções) e **grupo de transtornos** (2º nível, ex.: Transtorno bipolar,
  Esquizofrenia, Álcool).
- A classificação é heurística (baseada no título) e multi-rótulo — um mesmo
  artigo pode aparecer em 2–3 subespecialidades quando o tema é transversal.

## Hospedar

Basta publicar os arquivos (`index.html`, `sw.js`, `manifest.webmanifest` e os
ícones) no GitHub Pages ou em qualquer servidor de arquivos estáticos.

## Instalar no celular

- **Android/Chrome:** use o botão *Instalar app* na página.
- **iPhone:** abra no Safari e use *Compartilhar → Adicionar à Tela de Início*.

> A classificação por subespecialidade serve para triagem rápida e não
> substitui a leitura do artigo.
