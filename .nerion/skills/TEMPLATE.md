# SKILL — Estrutura template

Todas as skills do NERION OS seguem esse padrão. Copie essa template quando
criar uma skill nova.

---

## Cabeçalho

```
# SKILL: [Nome da skill]

Descrição em uma linha do que a skill faz.

Invoke: `/nome-da-skill [argumentos]`

Exemplo: `/aprovar-post 5` ou `/salvar "mensagem do commit"`
```

## Passo a passo

Descrever o fluxo da skill em passos claros. Use números.

```
1. Verificar se arquivo X existe
2. Ler conteúdo de Y
3. Fazer ação Z
4. Salvar resultado em W
```

## Variáveis e paths

Listar arquivos/pastas que a skill vai usar:

- `_memoria/empresa.md` — contexto do negócio
- `dados/posts/` — pasta onde ficam os posts
- `saidas/` — onde salvar outputs

## Integração com VS Code

Se a skill precisa executar código/terminal:

```bash
# Exemplo: script que a skill vai rodar
node scripts/publish-post.js --id=5
```

Se a skill usa ChatGPT API:

```javascript
// Exemplo: chamada à API
const response = await openai.createCompletion({
  model: "gpt-4-turbo",
  prompt: "Seu prompt aqui",
  max_tokens: 1000
});
```

## Outputs

Descrever o que a skill vai fazer/retornar:

- ✅ Arquivo criado em X
- ✅ Mensagem enviada pra Y
- ✅ Commit feito com mensagem Z

## Quando usar

Descrever em quais casos a skill é útil:

- Quando o usuário diz X
- Quando precisa fazer Y regularmente
- Como alternativa pra Z manual

## Variações

Se a skill tiver opções ou flags, descrever:

```
/nome-da-skill [arg1] --flag1 --flag2=valor
```

## Troubleshooting

Listar erros comuns e como resolver:

- **Erro: X**
  - Solução: Y
  - Verificar: Z

---

## Exemplo completo

Veja as skills existentes em `.nerion/skills/` para exemplos práticos.
