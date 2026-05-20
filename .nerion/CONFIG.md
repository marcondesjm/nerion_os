# Configuração do NERION OS para Copilot

Arquivo de configuração que o VS Code Copilot lê ao abrir o projeto.

---

## Como adicionar ao VS Code

1. Criar arquivo `.copilot/config.json` na raiz do projeto
2. Ou adicionar as settings ao `settings.json` do workspace

## Configuração recomendada

```json
{
  "chat.context": {
    "include": [
      "NERION-OS.md",
      "_memoria/empresa.md",
      "_memoria/preferencias.md",
      "_memoria/estrategia.md"
    ]
  },
  "copilot.enable": true,
  "copilot.chat.enabled": true,
  "copilot.language.suggestions": true,
  "copilot.model": "gpt-4-turbo"
}
```

## VS Code Workspace Settings

Adicionar ao `.vscode/settings.json`:

```json
{
  "github.copilot.enable": {
    "*": true
  },
  "github.copilot.chat.enabled": true,
  "[markdown]": {
    "editor.formatOnSave": false
  }
}
```

## .gitignore

Adicionar ao `.gitignore` da pasta (se não existir):

```
# Dependências
node_modules/
.env
.env.local

# Build
dist/
build/

# IDE
.vscode/
.idea/

# OS
.DS_Store
Thumbs.db

# Copilot cache (opcional)
.copilot/cache/
```

---

## Verificar se tá tudo configurado

1. Abrir qualquer arquivo no VS Code
2. Abrir Chat do Copilot (Ctrl+Shift+I ou Ctrl+I)
3. Digitar: "Qual é o contexto do meu negócio?"
4. Se o Copilot responder baseado em `_memoria/empresa.md`, tá funcionando! ✓

---

## Troubleshooting

### Copilot não reconhece contexto
- Verificar se `NERION-OS.md` existe
- Verificar se `_memoria/` tem os arquivos
- Fazer reload do VS Code (Ctrl+R)

### Chat não tá disponível
- Verificar se GitHub Copilot Chat está instalado
- Fazer login no GitHub (bottom left do VS Code)
- Reinstalar extensão se necessário

### Atalhos não funcionam (ex: `/aprovar-post`)
- Copilot Chat não suporta atalhos customizados nativamente
- Usar como prompt: "Execute a skill /aprovar-post 5"
- Ou criar workflow em `.nerion/workflows/`
