# Inclus-AI

![status](https://img.shields.io/badge/status-em_desenvolvimento-0a7ea4)
![fase](https://img.shields.io/badge/fase-estruturacao_inicial-1f6feb)
![foco](https://img.shields.io/badge/foco-acessibilidade_judicial-1b8a5a)
![stack](https://img.shields.io/badge/stack-FastAPI%20%7C%20Next.js%20%7C%20PostgreSQL-f39c12)
![licenca](https://img.shields.io/badge/licenca-MIT-6f42c1)

O Inclus-AI e um projeto academico e tecnico voltado a ampliar a acessibilidade da comunicacao judicial e institucional por meio de inteligencia artificial com revisao humana.

A proposta e analisar documentos, comunicados, orientacoes e outros conteudos, identificar barreiras de comunicacao e gerar versoes acessiveis complementares para diferentes perfis de acessibilidade, sem substituir a validacao institucional.

## Visao Geral

O repositorio foi estruturado para apoiar:

- desenvolvimento academico de um projeto formal de ensino superior;
- levantamento de requisitos e validacao tecnica de uma solucao de acessibilidade;
- construcao incremental de um MVP com base arquitetural real;
- eventual apresentacao institucional futura, se houver contexto adequado.

O projeto nao presume adocao oficial por tribunal ou orgao publico. Seu objetivo e investigar, prototipar e validar uma abordagem tecnicamente responsavel para acessibilidade digital e comunicacional no contexto da Justica.

## Problema Central

Comunicacoes judiciais e institucionais sao frequentemente publicadas em formatos de dificil acesso, navegacao ou compreensao para diferentes perfis de cidadaos, especialmente:

- pessoas com deficiencia;
- pessoas idosas;
- pessoas com baixa familiaridade juridica;
- pessoas com baixa alfabetizacao digital.

O problema central enfrentado pelo Inclus-AI e a ausencia de uma camada tecnologica estruturada capaz de:

- identificar barreiras de acessibilidade em conteudos oficiais;
- adaptar o mesmo conteudo para diferentes formas de percepcao, compreensao e interacao;
- preservar o significado original da comunicacao;
- apoiar revisao humana antes de qualquer uso ou publicacao.

## Proposta do Projeto

O Inclus-AI adapta a comunicacao judicial e institucional para diferentes formas de perceber, compreender e interagir com a informacao.

Na pratica, o projeto busca:

- transformar linguagem juridica em linguagem simples;
- gerar orientacoes por etapas para o cidadao;
- apoiar acessibilidade documental para leitores de tela;
- estruturar futuros fluxos de transcricao, legenda e roteiros acessiveis;
- estabelecer criterios objetivos para um selo de acessibilidade.

## Objetivo Geral

Desenvolver um sistema modular que auxilie na analise e na geracao de versoes acessiveis de comunicacoes judiciais e institucionais, utilizando inteligencia artificial como camada de apoio para acessibilidade, simplificacao e orientacao, com validacao humana e saidas rastreaveis.

## Objetivos Especificos

- identificar barreiras de comunicacao em textos, PDFs, arquivos escaneados, imagens e conteudos audiovisuais;
- gerar versoes acessiveis voltadas a diferentes perfis de usuarios;
- apoiar a adaptacao de conteudo juridico e procedimental para linguagem simples;
- produzir saidas complementares como texto descritivo, orientacao estruturada, transcricao e roteiros de acessibilidade;
- definir um modelo de classificacao para um selo de acessibilidade com base em criterios objetivos;
- preservar auditabilidade, fluxo de revisao e governanca institucional sobre o conteudo gerado.

## Escopo do MVP

O primeiro MVP sera concentrado em um fluxo principal: receber uma comunicacao institucional em texto ou PDF e produzir saidas acessiveis complementares para revisao.

Incluido no MVP:

- envio de documento em PDF textual ou texto simples;
- sinalizacao de OCR para arquivos escaneados ou baseados em imagem;
- versao em linguagem simples do conteudo;
- passo a passo orientado a acao do cidadao;
- resumo de acessibilidade com foco inicial em barreiras visuais e cognitivas;
- rascunho de pontuacao preliminar para o selo de acessibilidade;
- interface de revisao humana antes da aprovacao final.

Fora do MVP:

- geracao automatica completa de Libras;
- interacao por voz em tempo real;
- integracao direta com sistemas judiciais de producao;
- publicacao oficial automatica sem aprovacao humana;
- suporte a interpretacao juridica final ou decisao institucional.

## Modulos Funcionais

- `IncluTexto`: adaptacao para linguagem simples, resumos e orientacoes por etapas.
- `IncluVisao`: suporte a estrutura para leitores de tela, descricao de imagens e verificacoes de acessibilidade documental.
- `IncluLibras`: preparacao de transcricao, legenda e roteiro para fluxos futuros de Libras.
- `IncluVoz`: apoio a comunicacao escrita e geracao assistida para usuarios com barreiras relacionadas a fala.
- `Selo Acessivel`: motor de criterios para classificacao de acessibilidade e avaliacao rastreavel.

## Arquitetura de Referencia

A arquitetura tecnica segue uma estrutura modular orientada a servicos:

- `frontend`: Next.js + TypeScript para envio, revisao e visualizacao;
- `backend`: FastAPI como camada central de validacao, orquestracao, persistencia e classificacao;
- `worker`: processamento assincrono para OCR, parsing, analise e geracao;
- `database`: PostgreSQL para persistencia estruturada;
- `cache/queue`: Redis para execucao em segundo plano;
- `storage`: armazenamento de documentos e artefatos derivados;
- `ai adapters`: integracoes isoladas para linguagem, OCR, fala e futuros servicos de acessibilidade.

Mais detalhes estao documentados em [docs/architecture.md](docs/architecture.md).

## Estrutura do Repositorio

```text
.
|-- README.md
|-- docs/
|   |-- architecture.md
|   `-- project-foundation.md
|-- backend/
|   |-- app/
|   |   |-- api/
|   |   |-- core/
|   |   |-- domain/
|   |   |-- services/
|   |   `-- workers/
|   `-- README.md
`-- frontend/
    |-- app/
    |-- components/
    |-- lib/
    `-- README.md
```

## Estado Atual

O repositorio contem, neste momento, a documentacao fundacional e o scaffold inicial do projeto. A proxima fase de implementacao deve priorizar:

1. modelagem de dominio;
2. definicao dos contratos da API;
3. desenho do fluxo de revisao;
4. bootstrap do MVP em backend e frontend.

## Contribuicao

Contribuicoes sao bem-vindas, desde que respeitem o escopo academico, a coerencia arquitetural e a necessidade de rastreabilidade do projeto.

Antes de contribuir, leia:

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [docs/project-foundation.md](docs/project-foundation.md)
- [docs/architecture.md](docs/architecture.md)

## Licenca

Este repositorio esta licenciado sob a [MIT License](LICENSE).
