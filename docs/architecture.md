# Arquitetura Inicial

## Principios Arquiteturais

- a IA apoia e orquestra, mas a validacao institucional permanece humana;
- regras criticas devem estar explicitas em servicos de backend, e nao apenas em prompts;
- integracoes externas devem ficar isoladas por adaptadores;
- artefatos gerados devem ser rastreaveis ate sua origem e contexto de geracao;
- a arquitetura inicial deve priorizar clareza, modularidade e possibilidade de endurecimento institucional futuro.

## Componentes de Alto Nivel

### 1. Frontend

Responsabilidades:

- receber o envio de documentos;
- apresentar versoes acessiveis geradas;
- apoiar o fluxo de revisao e aprovacao;
- exibir a analise de acessibilidade e o rascunho de classificacao do selo.

Stack sugerida:

- Next.js
- TypeScript
- Tailwind CSS

### 2. API Backend

Responsabilidades:

- autenticar requisicoes em fases futuras;
- validar arquivos e metadados de entrada;
- registrar jobs de analise;
- orquestrar pipelines de processamento;
- persistir documentos de origem, saidas e estados de revisao;
- expor endpoints de revisao e relatorios.

Stack sugerida:

- Python
- FastAPI
- Pydantic
- SQLAlchemy

### 3. Workers de Processamento

Responsabilidades:

- extracao textual de documentos;
- deteccao de OCR e enriquecimento;
- analise estrutural;
- geracao de saidas acessiveis;
- calculo de classificacao do selo;
- retries assincronos e isolamento de falhas.

Stack sugerida:

- Celery ou RQ
- Redis

### 4. Camada de Persistencia

Responsabilidades:

- armazenar metadados dos documentos;
- armazenar execucoes de processamento;
- armazenar saidas geradas e status de revisao;
- suportar trilhas de auditoria e futuras analises.

Stack sugerida:

- PostgreSQL

### 5. Camada de Armazenamento

Responsabilidades:

- armazenar uploads originais;
- armazenar derivados extraidos;
- armazenar artefatos acessiveis gerados.

Opcoes sugeridas:

- armazenamento local na primeira etapa de desenvolvimento;
- armazenamento de objetos compativel com S3 em fases futuras.

### 6. Adaptadores de IA e Acessibilidade

Responsabilidades:

- integrar provedores de modelos de linguagem;
- integrar ferramentas de OCR;
- integrar futuras ferramentas de transcricao ou fala;
- isolar logica especifica de provedor das regras de dominio.

## Areas Iniciais de Dominio

- `documents`: conteudo enviado e texto-fonte extraido;
- `analysis`: barreiras detectadas e achados tecnicos;
- `adaptations`: versoes acessiveis geradas por perfil;
- `seal`: criterios de acessibilidade e classificacao;
- `review`: validacao humana e decisoes de aprovacao;
- `audit`: rastros do ciclo de processamento e saida.

## Fluxo Inicial de Processamento

1. O usuario envia um documento em texto ou PDF.
2. O backend valida o arquivo e cria um job de processamento.
3. O worker extrai o texto e verifica barreiras estruturais.
4. O adaptador de IA produz saidas acessiveis candidatas.
5. O backend persiste as saidas e a analise preliminar do selo.
6. O revisor compara o material original e o material gerado.
7. O revisor aprova, rejeita ou solicita ajustes.

## Entidades de Dados do MVP

- `Document`
- `DocumentSource`
- `AnalysisRun`
- `BarrierFinding`
- `AccessibilityProfile`
- `GeneratedArtifact`
- `SealEvaluation`
- `ReviewDecision`

## Estrategia Sugerida de Pastas do Backend

```text
backend/app/
|-- api/
|-- core/
|-- domain/
|-- models/
|-- schemas/
|-- services/
|-- repositories/
`-- workers/
```

## Estrategia Sugerida de Pastas do Frontend

```text
frontend/
|-- app/
|-- components/
|-- features/
|-- lib/
`-- styles/
```

## Riscos e Decisoes em Aberto

- o primeiro publico-alvo ainda nao foi formalmente definido;
- a primeira categoria documental do MVP continua em aberto;
- os criterios do selo de acessibilidade ainda precisam de regras objetivas de pontuacao;
- requisitos institucionais de seguranca e LGPD ainda precisam ser especificados em fases futuras.
