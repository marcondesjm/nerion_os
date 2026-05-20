# NERION OS — Setup & Uso

Sistema operacional pra seu negócio rodando com ChatGPT + Codex no VS Code.

---

## Setup inicial

### 1. Instalar extensão Codex no VS Code
- Abrir Extensions (Ctrl+Shift+X)
- Buscar "Codex"
- Instalar a extensao oficial da OpenAI/ChatGPT
- Fazer login com sua conta OpenAI/ChatGPT

### 2. Configurar ChatGPT API (opcional, mas recomendado)
Se quiser usar ChatGPT via terminal/scripts:

```bash
# Instalar OpenAI CLI
npm install -g openai

# Configurar API key
export OPENAI_API_KEY=sua_chave_aqui
```

### 3. Criar arquivo `.nerion/config.json` (opcional)
```json
{
  "model": "gpt-4-turbo",
  "temperature": 0.7,
  "max_tokens": 2000
}
```

---

## Estrutura de pastas

```
.nerion/
├── skills/              # Skills locais do projeto
│   ├── aprovar-post/    # Exemplo: skill para publicar posts
│   └── salvar/          # Exemplo: skill para commit/push
├── workflows/           # Scripts que executam ações
├── config.json          # Configurações globais (opcional)
└── README.md            # Esse arquivo
```

---

## Como usar

### Via Codex inline (VS Code)

1. Abrir arquivo no VS Code
2. Digitar comentário ou começar código
3. Pressionar `Ctrl+K` para sugestão do Codex
4. Aceitar com `Tab` ou rejeitar com `Esc`

O Codex lê automaticamente:
- `NERION-OS.md` (regras do sistema)
- `_memoria/empresa.md` (contexto do negócio)
- `_memoria/preferencias.md` (tom e estilo)
- `_memoria/estrategia.md` (prioridades)

### Via command (prompt)

Abrir Chat do Codex (`Ctrl+Shift+I`) e escrever:

```
/aprovar-post numero-do-post
/salvar "Descrição do commit"
/criar-skill nome-da-skill
```

---

## Skills principais

### `/aprovar-post [numero]`
Publica um post da fila:
- Flip blog de draft → published
- Copia PNGs do carrossel pra public/
- Faz commit + push (redeploy automático)
- Posta no Instagram + Facebook

**Arquivo:** `.nerion/skills/aprovar-post/SKILL.md`

### `/salvar [mensagem]`
Salva trabalho no GitHub:
- Commit automático
- Push pra main
- Primeira vez: configura repositório remoto

**Arquivo:** `.nerion/skills/salvar/SKILL.md`

### `/criar-skill [nome]`
Cria nova skill:
- Pergunta se é local ou global
- Gera template
- Adiciona ao `.nerion/skills/`

---

## Aprender com correções

Quando o ChatGPT errar ou você corrigir algo, diga:

> "Salva isso pra próxima vez"

O Codex vai atualizar automaticamente:
- `_memoria/empresa.md` (negócio)
- `_memoria/preferencias.md` (estilo)
- `_memoria/estrategia.md` (foco)
- `NERION-OS.md` (regras)

---

## Troubleshooting

### Codex não tá sugerindo nada
- Verificar se Codex está ativado (VS Code → Settings → Extensions → Codex)
- Verificar se você fez login (Codex icon no canto inferior)
- Reinstalar a extensão se necessário

### Skills não funcionam
- Verificar se existe arquivo `SKILL.md` na pasta da skill
- Verificar se os paths estão corretos no arquivo
- Rodar `/debug` pra ver logs

### Memory não tá atualizando
- Verificar se os arquivos em `_memoria/` existem
- Verificar se estão no formato Markdown correto
- Rodar `/atualizar` pra forçar rescan

---

## Próximos passos

1. ✅ Renomear NERION-OS.md → NERION-OS.md
2. ✅ Criar pastas `.nerion/skills` e `.nerion/workflows`
3. ⏳ Preencher `_memoria/empresa.md` com dados
4. ⏳ Adaptar skills existentes pra ChatGPT/Codex
5. ⏳ Criar workflows pra automação

Rode `/instalar` pra começar!
