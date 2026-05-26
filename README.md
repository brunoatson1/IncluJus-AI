# IncluJus AI

O IncluJus AI e um projeto academico e tecnico voltado a ampliar a acessibilidade da comunicacao judicial e institucional por meio de inteligencia artificial com revisao humana.

A proposta e analisar documentos, comunicados, orientacoes e outros conteudos, identificar barreiras de comunicacao e gerar versoes acessiveis complementares para diferentes perfis de acessibilidade, sem substituir a validacao institucional.

## Posicionamento do Projeto

Este repositorio foi estruturado para apoiar:

- o desenvolvimento academico de um projeto formal de ensino superior;
- o levantamento de requisitos e a validacao tecnica de uma solucao de acessibilidade;
- a construcao incremental de um MVP com base arquitetural real;
- eventual apresentacao institucional futura, se houver contexto adequado.

O projeto nao presume adocao oficial por tribunal ou orgao publico. Seu objetivo e investigar, prototipar e validar uma abordagem tecnicamente responsavel para acessibilidade digital e comunicacional no contexto da Justica.

## Problema

Comunicacoes judiciais e institucionais sao frequentemente publicadas em formatos de dificil acesso, navegacao ou compreensao para diferentes perfis de cidadaos, especialmente pessoas com deficiencia, pessoas idosas e pessoas com baixa familiaridade juridica ou digital.

O problema central enfrentado por este projeto e a ausencia de uma camada tecnologica estruturada capaz de:

- identificar barreiras de acessibilidade em conteudos oficiais;
- adaptar o mesmo conteudo para diferentes formas de percepcao, compreensao e interacao;
- preservar o significado original da comunicacao;
- apoiar revisao humana antes de qualquer uso ou publicacao.

## Objetivo Geral

Desenvolver um sistema modular que auxilie na analise e na geracao de versoes acessiveis de comunicacoes judiciais e institucionais, utilizando inteligencia artificial como camada de apoio para acessibilidade, simplificacao e orientacao, com validacao humana e saidas rastreaveis.

## Objetivos Especificos

- identificar barreiras de comunicacao em textos, PDFs, arquivos escaneados, imagens e conteudos audiovisuais;
- gerar versoes acessiveis voltadas a diferentes perfis de usuarios;
- apoiar a adaptacao de conteudo juridico e procedimental para linguagem simples;
- produzir saidas complementares como texto descritivo, orientacao estruturada, transcricao e roteiros de acessibilidade;
- definir um modelo de classificacao para um selo de acessibilidade com base em criterios objetivos;
- preservar auditabilidade, fluxo de revisao e governanca institucional sobre o conteudo gerado.

## Escopo Inicial do MVP

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

## Resumo da Arquitetura

A arquitetura tecnica segue uma estrutura modular orientada a servicos:

- `frontend`: interface em Next.js + TypeScript para envio, revisao e visualizacao;
- `backend`: API FastAPI como camada central de validacao, orquestracao, persistencia e classificacao;
- `worker`: processamento assincrono para OCR, parsing, analise de conteudo e pipelines de geracao;
- `database`: PostgreSQL para persistencia estruturada;
- `cache/queue`: Redis para execucao em segundo plano e estado temporario;
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

Este repositorio contem, neste momento, a documentacao fundacional e o scaffold inicial do projeto. A proxima fase de implementacao deve priorizar:

1. modelagem de dominio;
2. definicao dos contratos da API;
3. desenho do fluxo de revisao;
4. bootstrap do MVP em backend e frontend.

## Licenca

A definicao de licenca ainda esta pendente.
