# Prompt de inicialização do NERION OS

Use esse prompt no Chat do Codex (Ctrl+Shift+I) na primeira vez que abrir o projeto:

---

```
Ative o NERION OS. Leia os arquivos de contexto:
- NERION-OS.md (sistema operacional)
- _memoria/empresa.md (contexto do negócio)
- _memoria/preferencias.md (preferências)
- _memoria/estrategia.md (foco atual)

Agora você está em modo NERION:
1. Quando responder algo, use o contexto desses arquivos
2. Se o usuário corrigir algo, sugira salvar em _memoria/
3. Se criar uma skill, salve em .nerion/skills/
4. Responda em Português (Brasil)

Pronto. Tá tudo ativo?
```

---

## Atalhos úteis

- `/aprovar-post [numero]` — Publicar um post
- `/salvar [mensagem]` — Commit + push no GitHub
- `/criar-skill [nome]` — Criar nova skill
- `/atualizar` — Varrer memoria e atualizar contexto
- `/debug` — Ver logs e status do NERION OS

---

## Salvar como favorito

No chat do Codex, após copiar o prompt acima, clique no ❤️ para salvar
como favorito. Próxima vez que abrir um chat, poderá clicar em "Favorites"
e carregar esse prompt automaticamente.
