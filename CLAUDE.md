# Diretrizes do Projeto

## 1. Padrões de Git & Workflow
- Criar Issues no GitHub para todas as tarefas (Correção, Melhoria ou Nova função).
- Gerenciar deploys via Pull Requests (PRs), mencionando a Issue correspondente na descrição do PR.

## 2. Padrões de UI, Design & Taste Skill
- Seguir estritamente as diretrizes de direção de arte sem aspecto genérico/AI-made definidas no arquivo `SKILL.md` do repositório `Neto3x/taste-skill`.
- Aplicar Motion Principles (baseados no repositório kylezantos/design-motion-principles): uso de skeletons, lazy loading, smooth animations de entrada/saída e carregamento, além de indicadores de progresso em todos os elementos.
- Respeitar a regra de frequência de animações (Frequency Gate): ações frequentes devem ter transições rápidas ou instantâneas (180ms a 300ms) e navegação por teclado nunca deve ser atrasada por animação.
- Garantir acessibilidade básica: incluir atributos `alt` descritivos em todas as imagens e assegurar navegação por teclado fluida e visível (`:focus-visible`).

## 3. Arquitetura, Qualidade & Observabilidade
- Garantir observabilidade (Sentry, Datadog, NewRelic, OpenTelemetry).
- Garantir qualidade e lint de código (Arch-contract, Biome, Commitlint, Knip, Stryker).
- Cobertura de testes unitários, de integração e end-to-end (Codecov, Playwright).
- 
