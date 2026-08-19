# IncluJus AI

![status](https://img.shields.io/badge/status-em_desenvolvimento-0a7ea4)
![fase](https://img.shields.io/badge/fase-estruturacao_inicial-1f6feb)
![foco](https://img.shields.io/badge/foco-acessibilidade_judicial-1b8a5a)
![stack](https://img.shields.io/badge/stack-FastAPI%20%7C%20Next.js%20%7C%20PostgreSQL-f39c12)
![licenca](https://img.shields.io/badge/licenca-MIT-6f42c1)

O **IncluJus AI** é um projeto acadêmico e técnico voltado a ampliar a acessibilidade da comunicação judicial e institucional por meio de Inteligência Artificial com revisão humana.

A proposta é analisar documentos, comunicados, orientações e outros conteúdos, identificar barreiras de comunicação e gerar versões acessíveis complementares para diferentes perfis de acessibilidade, sem substituir a validação institucional.

## Visão geral

O repositório foi estruturado para apoiar:

- desenvolvimento acadêmico de um projeto formal de ensino superior;
- levantamento de requisitos e validação técnica de uma solução de acessibilidade;
- construção incremental de um MVP com base arquitetural real;
- eventual apresentação institucional futura, quando houver contexto adequado.

O projeto não presume adoção oficial por tribunal ou órgão público. Seu objetivo é investigar, prototipar e validar uma abordagem tecnicamente responsável para acessibilidade digital e comunicacional no contexto da Justiça.

## Problema central

Comunicações judiciais e institucionais são frequentemente publicadas em formatos de difícil acesso, navegação ou compreensão para diferentes perfis de cidadãos, especialmente:

- pessoas com deficiência;
- pessoas idosas;
- pessoas com baixa familiaridade jurídica;
- pessoas com baixa alfabetização digital.

O problema central enfrentado pelo IncluJus AI é a ausência de uma camada tecnológica estruturada capaz de:

- identificar barreiras de acessibilidade em conteúdos oficiais;
- adaptar o mesmo conteúdo para diferentes formas de percepção, compreensão e interação;
- preservar o significado original da comunicação;
- apoiar revisão humana antes de qualquer uso ou publicação.

## Proposta do projeto

O IncluJus AI adapta a comunicação judicial e institucional para diferentes formas de perceber, compreender e interagir com a informação.

Na prática, o projeto busca:

- transformar linguagem jurídica em linguagem simples;
- gerar orientações por etapas para o cidadão;
- apoiar acessibilidade documental para leitores de tela;
- estruturar futuros fluxos de transcrição, legenda e roteiros acessíveis;
- estabelecer critérios objetivos para um selo de acessibilidade.

## Objetivo geral

Desenvolver um sistema modular que auxilie na análise e na geração de versões acessíveis de comunicações judiciais e institucionais, utilizando Inteligência Artificial como camada de apoio para acessibilidade, simplificação e orientação, com validação humana e saídas rastreáveis.

## Objetivos específicos

- identificar barreiras de comunicação em textos, PDFs, arquivos escaneados, imagens e conteúdos audiovisuais;
- gerar versões acessíveis voltadas a diferentes perfis de usuários;
- apoiar a adaptação de conteúdo jurídico e procedimental para linguagem simples;
- produzir saídas complementares como texto descritivo, orientação estruturada, transcrição e roteiros de acessibilidade;
- definir um modelo de classificação para um selo de acessibilidade com base em critérios objetivos;
- preservar auditabilidade, fluxo de revisão e governança institucional sobre o conteúdo gerado.

## Escopo do MVP

O primeiro MVP será concentrado em um fluxo principal: receber uma comunicação institucional em texto ou PDF e produzir saídas acessíveis complementares para revisão.

Incluído no MVP:

- envio de documento em PDF textual ou texto simples;
- sinalização de OCR para arquivos escaneados ou baseados em imagem;
- versão em linguagem simples do conteúdo;
- passo a passo orientado à ação do cidadão;
- resumo de acessibilidade com foco inicial em barreiras visuais e cognitivas;
- rascunho de pontuação preliminar para o selo de acessibilidade;
- interface de revisão humana antes da aprovação final.

Fora do MVP:

- geração automática completa de Libras;
- interação por voz em tempo real;
- integração direta com sistemas judiciais de produção;
- publicação oficial automática sem aprovação humana;
- suporte à interpretação jurídica final ou decisão institucional.

## Módulos funcionais

- `IncluTexto`: adaptação para linguagem simples, resumos e orientações por etapas.
- `IncluVisão`: suporte à estrutura para leitores de tela, descrição de imagens e verificações de acessibilidade documental.
- `IncluLibras`: preparação de transcrição, legenda e roteiro para fluxos futuros de Libras.
- `IncluVoz`: apoio à comunicação escrita e geração assistida para usuários com barreiras relacionadas à fala.
- `Selo Acessível`: motor de critérios para classificação de acessibilidade e avaliação rastreável.

## Arquitetura de referência

A arquitetura técnica segue uma estrutura modular orientada a serviços:

- `frontend`: Next.js + TypeScript para envio, revisão e visualização;
- `backend`: FastAPI como camada central de validação, orquestração, persistência e classificação;
- `worker`: processamento assíncrono para OCR, parsing, análise e geração;
- `database`: PostgreSQL para persistência estruturada;
- `cache/queue`: Redis para execução em segundo plano;
- `storage`: armazenamento de documentos e artefatos derivados;
- `ai adapters`: integrações isoladas para linguagem, OCR, fala e futuros serviços de acessibilidade.

Mais detalhes estão documentados em [docs/architecture.md](docs/architecture.md).

## Estrutura do repositório

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

## Estado atual

O repositório contém, neste momento, a documentação fundacional e o scaffold inicial do projeto. A próxima fase de implementação deve priorizar:

1. modelagem de domínio;
2. definição dos contratos da API;
3. desenho do fluxo de revisão;
4. bootstrap do MVP em backend e frontend.

## Contribuição

Contribuições são bem-vindas, desde que respeitem o escopo acadêmico, a coerência arquitetural e a necessidade de rastreabilidade do projeto.

Antes de contribuir, leia:

- [CONTRIBUTING.md](CONTRIBUTING.md)
- [docs/project-foundation.md](docs/project-foundation.md)
- [docs/architecture.md](docs/architecture.md)

## Licença

Este repositório está licenciado sob a [MIT License](LICENSE).
