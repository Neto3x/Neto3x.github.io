# Diretrizes do Projeto — Neto.web

## 1. Padrões de Git & Workflow
- Criar Issues no GitHub para todas as tarefas (Correção, Melhoria ou Nova função).
- Gerenciar deploys via Pull Requests (PRs), mencionando a Issue correspondente na descrição do PR.

## 2. Padrões de UI, Design & Taste Skill (Anti-Slop)
- Seguir estritamente as diretrizes de direção de arte do arquivo `SKILL.md` do repositório `Neto3x/taste-skill`.
- Evitar estampa genérica ("AI-slop"): sem cantos exageradamente arredondados, sem quebras bruscas de contraste sem sentido, sem badges sobrepondo textos do hero e sem botões flutuantes cobrindo conteúdos.
- Garantir acessibilidade básica: incluir atributos `alt` descritivos em todas as imagens e assegurar navegação por teclado fluida e visível (`:focus-visible`).

## 3. Animações, Interatividade & Scroll Storytelling
- **Seção Hero Interativa (Scroll-Driven):** Por padrão, crie todas as Landing Pages incorporando uma Seção Hero com animação baseada em Scroll (GSAP + ScrollTrigger).
  - Incluir CDN do GSAP e ScrollTrigger.
  - Travar a seção inicial usando `pin: true` (`100vh` / `min-h-screen`) e sincronizar a animação com `scrub: 1` ou `scrub: true`.
  - Liberar o pin para a rolagem fluir normalmente após concluir a transição da animação.
  - Otimizar para Mobile/Touch sem *jank*, utilizando `will-change: transform` e aceleração por GPU (`transform: translate3d`).
- **Motion Principles (Kyle Zantos):** Aplicar uso de skeletons, lazy loading e suporte a `prefers-reduced-motion`.
- **Frequency Gate:** Ações frequentes devem ter transições rápidas (180ms a 300ms) e navegação por teclado nunca deve ser atrasada por animações.

## 4. Arquitetura, Qualidade & Observabilidade
- Garantir observabilidade (Sentry, Datadog, NewRelic, OpenTelemetry).
- Garantir qualidade e lint de código (Arch-contract, Biome, Commitlint, Knip, Stryker).
- Cobertura de testes unitários, de integração e end-to-end (Codecov, Playwright).
- 
