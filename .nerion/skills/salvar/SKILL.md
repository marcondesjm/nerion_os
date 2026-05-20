# SKILL: Salvar no GitHub

Salva o trabalho do NERION OS no GitHub (commit + push).

**Invoke:** `/salvar [mensagem]` ou `/salvar`

**Exemplo:** `/salvar "Adiciona features novas"` ou `/salvar`

---

## O que faz

1. Se for primeira vez: configura repositório remoto (remote origin)
2. Faz `git add .` (stage de tudo)
3. Faz `git commit -m "[mensagem]"` (commit com sua mensagem)
4. Faz `git push origin main` (envia pra GitHub)
5. Mostra confirmação com link do commit

---

## Arquivos usados

- Toda pasta do projeto (qualquer coisa modificada)
- `.git/` (histórico e configuração do repositório)
- `NERION-OS.md` e `_memoria/` (arquivos do sistema, sempre salvos)

---

## Integração com VS Code + Codex

No Chat do Codex, digitar:

```
/salvar Adiciona novo post sobre X
```

O Codex vai executar:

```bash
git add .
git commit -m "Adiciona novo post sobre X"
git push origin main
```

---

## Outputs

- ✅ Commit criado com sua mensagem
- ✅ Push enviado pra `main` branch
- ✅ GitHub redeploy automático (Netlify/Vercel)
- ✅ Confirmação com hash do commit

---

## Quando usar

- Após criar/editar conteúdo
- Antes de fazer deploy
- Regularmente pra manter backup
- Quando terminar uma tarefa importante

---

## Opções

### Default (sem mensagem)
```bash
/salvar
```
Cria commit genérico: `"Update: [data e hora]"`

### Com mensagem customizada
```bash
/salvar "Seu commit message aqui"
```

### Force push (cuidado!)
```bash
/salvar --force
```
(use apenas se souber o que tá fazendo)

---

## Troubleshooting

- **Erro: "fatal: not a git repository"**
  - Solução: Rodar `git init` pra inicializar repositório
  - Depois rodar `/salvar` novamente

- **Erro: "Permission denied (publickey)"**
  - Solução: Verificar se SSH key tá configurada no GitHub
  - Ou usar HTTPS em vez de SSH

- **Erro: "nothing to commit, working tree clean"**
  - Tudo já tá commitado
  - Fazer edições e tentar de novo

- **Push não funciona**
  - Verificar se remoto tá configurado: `git remote -v`
  - Se não tiver, rodar: `git remote add origin [URL do repo]`

---

## Ver histórico

Pra ver últimos commits:
```bash
git log --oneline -10
```

Pra ver o status:
```bash
git status
```

---

## Próximos passos

1. Configurar SSH key ou token GitHub
2. Rodar `/salvar` pra fazer primeiro commit
3. Verificar se push funcionou em github.com
