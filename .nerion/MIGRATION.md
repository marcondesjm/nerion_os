# Migração de skills: Claude → ChatGPT

Guia para adaptar as skills existentes do MazyOS para o NERION OS.

---

## Skills a migrar

### 1. `/aprovar-post`
**O que faz:** Publica um post (draft → published), copia imagens, faz commit, posta no Instagram/Facebook.

**Arquivos originais:**
- `.claude/skills/aprovar-post/SKILL.md`

**Como adaptar para ChatGPT:**

1. Copiar conteúdo de `.claude/skills/aprovar-post/SKILL.md`
2. Criar `.nerion/skills/aprovar-post/SKILL.md`
3. Mudar referências de Claude → ChatGPT
4. Mudar paths `.claude/` → `.nerion/`
5. Se usar ChatGPT API, adicionar chamadas à OpenAI client
6. Se usar terminal, scripts continuam iguais

**Exemplo de adaptação:**

```markdown
# SKILL: Aprovar e publicar post

Invoke: `/aprovar-post [numero]`

Passos:
1. Ler arquivo do post em `dados/posts/draft/post-[numero].md`
2. Mover pra `dados/posts/published/post-[numero].md`
3. Copiar imagens do carrossel de `dados/imgs/` pra `saidas/public/posts/[numero]/`
4. Executar: `npm run build` (Netlify redeploy automático)
5. Chamar Instagram/Facebook API pra postar carrossel
6. Fazer commit: `git commit -m "Publica post #[numero]"`
7. Push: `git push origin main`
```

### 2. `/salvar`
**O que faz:** Commit + push no GitHub.

**Como adaptar:**

1. Copiar `.claude/skills/salvar/SKILL.md`
2. Criar `.nerion/skills/salvar/SKILL.md`
3. Adapt paths e referências

---

## Estrutura final

Depois de migrar, a pasta `.nerion/skills/` vai ter:

```
.nerion/skills/
├── aprovar-post/
│   ├── SKILL.md
│   └── (outros arquivos de apoio, se existirem)
├── salvar/
│   ├── SKILL.md
│   └── (outros arquivos de apoio, se existirem)
└── TEMPLATE.md (template pra novas skills)
```

---

## Testar migration

Depois de criar a skill:

1. Abrir Chat do Copilot (Ctrl+Shift+I)
2. Digitar: `/aprovar-post 1` (ou `/salvar "test commit"`)
3. Verificar se o Copilot reconhece o comando
4. Se não reconhecer, verificar sintaxe do SKILL.md

---

## Próximos passos

- [ ] Copiar `/aprovar-post` de `.claude/` pra `.nerion/`
- [ ] Copiar `/salvar` de `.claude/` pra `.nerion/`
- [ ] Testar cada skill no Copilot Chat
- [ ] Documentar novas skills conforme criar

---

## Dúvidas?

Se uma skill não rodar, verificar:
1. SKILL.md existe em `.nerion/skills/[nome]/SKILL.md`? ✓
2. Sintaxe Markdown está correta? ✓
3. ChatGPT consegue ler o arquivo? ✓
4. Paths e variáveis estão atualizados? ✓
