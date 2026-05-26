# Guia de Contribuicao

Obrigado por considerar contribuir com o `IncluJus AI`.

Este projeto possui natureza academica e tecnica, com foco em acessibilidade, comunicacao institucional e implementacao responsavel. Contribuicoes sao bem-vindas, desde que respeitem o escopo, a clareza arquitetural e a necessidade de rastreabilidade.

## Principios de Contribuicao

- priorize clareza, manutencao e modularidade;
- nao introduza regra critica apenas em prompts ou texto solto;
- trate o backend como fonte de verdade para validacao e persistencia;
- preserve a revisao humana em fluxos sensiveis;
- evite acoplamento desnecessario com provedores externos;
- documente decisoes relevantes de produto e arquitetura.

## Antes de Comecar

Antes de abrir uma contribuicao:

- leia o [README.md](README.md);
- leia [docs/project-foundation.md](docs/project-foundation.md);
- leia [docs/architecture.md](docs/architecture.md);
- confirme se a mudanca faz sentido para o MVP atual do projeto.

## Tipos de Contribuicao Aceitos

- correcao de bugs;
- melhorias de documentacao;
- refinamentos de arquitetura;
- implementacao incremental do MVP;
- melhorias de acessibilidade;
- testes, validacoes e automacoes de qualidade.

## Tipos de Mudanca que Exigem Mais Cuidado

Abra uma issue ou descreva claramente a motivacao no PR quando a mudanca envolver:

- alteracao de arquitetura;
- novas dependencias estruturais;
- mudanca de modelo de dados;
- integracao externa;
- alteracao de escopo do MVP;
- qualquer fluxo sensivel relacionado a validacao institucional.

## Fluxo Recomendado

1. Crie um fork do repositorio.
2. Crie uma branch descritiva a partir de `main`.
3. Faca mudancas pequenas, objetivas e coerentes.
4. Atualize a documentacao quando necessario.
5. Abra um Pull Request com contexto suficiente para revisao.

## Convencoes Minimas

- use nomes de branch claros, por exemplo: `feat/upload-documento`, `fix/ajuste-readme`, `docs/arquitetura-mvp`;
- prefira commits objetivos, por exemplo: `feat: adiciona endpoint de upload` ou `docs: refina escopo do mvp`;
- mantenha mudancas relacionadas agrupadas no mesmo PR;
- evite PRs gigantes com multiplos assuntos ao mesmo tempo.

## Padrao Esperado para Pull Requests

Todo PR deve informar:

- problema que esta sendo resolvido;
- abordagem adotada;
- arquivos principais afetados;
- riscos ou limitacoes conhecidas;
- impacto no MVP, se houver.

Se houver interface, fluxo ou comportamento alterado, inclua exemplos, capturas ou descricao do antes/depois.

## Qualidade Minima

Antes de enviar um PR:

- revise seu proprio codigo;
- valide se a mudanca nao contradiz a documentacao atual;
- remova arquivos temporarios e artefatos locais;
- mantenha o repositorio limpo e sem ruido desnecessario.

## Escopo e Responsabilidade

Este projeto nao deve:

- substituir validacao humana em fluxos sensiveis;
- presumir integracao oficial com instituicoes;
- introduzir logica juridica critica sem base clara e revisavel;
- transformar a IA na unica camada decisoria do sistema.

## Discussao e Alinhamento

Se a contribuicao for maior que uma correcao simples, o ideal e alinhar antes por issue ou descricao previa do escopo pretendido.

Isso ajuda a evitar retrabalho e preserva a coerencia academica e tecnica do repositorio.
