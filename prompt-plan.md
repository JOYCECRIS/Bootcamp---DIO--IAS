
Prompt Dinâmico (Template) — Copiloto “PLAN”
✅ Objetivo

Implementar ${FEATURE_NAME} garantindo ${EXPECTED_RESULT}.

🧭 Contexto e Assunções
Projeto: Node.js + TypeScript
Estrutura padrão: src/, routes/, controllers/, services/, repositories/
Framework HTTP: ${HTTP_FRAMEWORK}` (Express/Fastify/etc.)
Banco: ${DB_TYPE}` (Postgres/Mongo/SQLite)
Supondo ESM (import/export)
Dependências: ESLint, Prettier, Vitest/Jest
📦 Escopo

Inclui:

Implementação de ${FEATURE_NAME}
Validação de input
Tratamento de erros
Integração com ${DB_TYPE} ou API externa

Não inclui:

UI/frontend
Autenticação avançada (a menos que especificado)
Otimizações de alta escala
🧩 Estratégia
Controller → Service → Repository (separação de camadas)
Validar input (ex: Zod/Yup)
Centralizar tratamento de erro
Separar regras de negócio da rota
Alternativa simples: lógica direto na rota (desaconselhado)
🗂️ Arquivos/áreas provavelmente afetadas
src/index.ts
src/routes/${FEATURE_NAME}.ts
src/controllers/${FEATURE_NAME}.controller.ts
src/services/${FEATURE_NAME}.service.ts
src/repositories/${FEATURE_NAME}.repository.ts
src/types/${FEATURE_NAME}.types.ts
tests/${FEATURE_NAME}.test.ts
🪜 Plano passo a passo
Criar estrutura de pastas (routes/, controllers/, etc.)
Criar rota base / ${FEATURE_NAME}
Implementar controller (req/res)
Implementar service (regras de negócio)
Integrar repository / banco
Adicionar validação de input
Adicionar tratamento de erro centralizado
Escrever testes: happy path + erro + edge cases
Validar fluxo completo
🧪 Testes e validação
Rodar testes: npm run test
Testar via Postman/Insomnia

Casos de teste:

Sucesso com dados válidos
Validação falha
Erro interno
Edge cases: null, vazio, limites
⚠️ Riscos e mitigação

Riscos:

Input inválido → fluxo quebra
Integração com DB falha
Diferença de versão Node ou dependência

Mitigação:

Validação forte
try/catch + logs
Fixar versão Node e dependências críticas
❓ Perguntas (se necessário)
Qual banco vai usar? ${DB_TYPE}
Precisa de autenticação? (sim/não)
Estrutura de pastas já existe?
▶️ Próximo passo

Confirme este plano ou preencha as variáveis:

${FEATURE_NAME}
${EXPECTED_RESULT}
${HTTP_FRAMEWORK}
${DB_TYPE}
