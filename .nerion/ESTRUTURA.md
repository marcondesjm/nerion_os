# Estrutura final do NERION OS

```
NERION-OS (raiz do projeto)
│
├── NERION-OS.md                    # Sistema principal - LEIA ISSO PRIMEIRO
│
├── _memoria/                       # Seu contexto (lido pelo Codex)
│   ├── empresa.md                  # Negócio, clientes, serviços
│   ├── preferencias.md             # Tom, estilo, o que evitar
│   └── estrategia.md               # Foco, prioridades, prazos
│
├── .nerion/                        # Núcleo do NERION OS
│   ├── README.md                   # Setup rápido
│   ├── CHECKLIST.md                # Checklist de implementação
│   ├── CONFIG.md                   # Configuração técnica
│   ├── MIGRATION.md                # Como migrar skills do Codex
│   ├── PROMPT-INICIAL.md           # Prompt pra ativar NERION
│   ├── settings.json               # Settings do VS Code
│   │
│   ├── skills/                     # Skills do projeto
│   │   ├── TEMPLATE.md             # Template pra criar novo skill
│   │   ├── salvar/
│   │   │   └── SKILL.md            # Skill: commit + push GitHub
│   │   └── aprovar-post/
│   │       └── SKILL.md            # Skill: publicar post
│   │
│   └── workflows/                  # Automações (scripts, etc)
│       └── (vazio, add conforme precisar)
│
├── dados/                          # Dados do projeto
│   ├── posts/
│   │   ├── draft/                  # Posts em rascunho
│   │   └── published/              # Posts publicados
│   └── imgs/
│       └── posts/                  # Imagens dos posts
│
├── identidade/
│   └── design-guide.md             # Visual do brand (cores, fontes, etc)
│
├── templates/                      # Templates e exemplos
│   ├── skills/
│   │   └── catalogo.md
│   ├── identidade/
│   │   └── exemplos/
│   │       ├── design-guide-agencia.md
│   │       └── design-guide-solopreneur.md
│   └── perfis/
│       ├── codex-md-agencia.md
│       ├── codex-md-empresa.md
│       ├── codex-md-freelancer.md
│       └── codex-md-solopreneur.md
│
├── saidas/                         # Outputs finais
│   ├── public/                     # Pasta pra deploy (Netlify/Vercel)
│   │   └── posts/
│   └── README.md
│
├── scripts/                        # Scripts de automação
│   └── README.md
│
├── .git/                           # Repositório Git
├── .gitignore
├── .vscode/
│   └── settings.json               # Settings do workspace
└── README.md                       # Documentação geral
```

---

## Fluxo de trabalho típico

```
1. Abrir VS Code
   ↓
2. Fazer edições (posts, design, conteúdo)
   ↓
3. Abrir Chat do Codex (Ctrl+Shift+I)
   ↓
4. Digitar: /salvar "descrição"
   ↓
5. Codex faz commit + push
   ↓
6. GitHub redeploya (Netlify/Vercel)
   ↓
7. Pronto!
```

---

## Diferença chave: NERION OS vs NERION OS

**NERION OS:**
- Rodava em Codex
- Skills eram criadas via Codex
- Context era carregado automaticamente

**NERION OS:**
- Roda em VS Code + Codex
- Skills são arquivos Markdown em `.nerion/skills/`
- Você copia/cola prompt pra ativar no Codex
- Mais flexível, rodas em ambiente local

---

## Próximas melhorias (backlog)

- [ ] Criar workflow automático via GitHub Actions
- [ ] Integrar com Zapier/Make pra social media
- [ ] Criar dashboard de status dos posts
- [ ] Adicionar versionamento de conteúdo
- [ ] Criar sistema de templates de posts
- [ ] Backup automático em cloud
- [ ] Integrar com Google Analytics

---

## Suporte rápido

- Quer criar nova skill? → Leia `.nerion/skills/TEMPLATE.md`
- Quer saber como configurar? → Leia `.nerion/CONFIG.md`
- Quer saber como migrar de Codex? → Leia `.nerion/MIGRATION.md`
- Quer começar agora? → Leia `.nerion/README.md`

---

## Status

| Item | Status | Responsável |
|------|--------|-------------|
| NERION-OS.md | ✅ Pronto | Sistema |
| Skills básicas | ✅ Pronto | Sistema |
| Documentação | ✅ Pronto | Sistema |
| Configuração VS Code | ⏳ Manual (seu setup) | Você |
| Preencher memória | ⏳ Manual | Você |
| Testar skills | ⏳ Manual | Você |
