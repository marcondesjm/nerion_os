# SKILL: Aprovar e publicar post

Aprova e publica um post da fila — flipa o blog de draft pra published,
copia os PNGs do carrossel pro public folder do site, faz commit e push
(Netlify/Vercel deploya), aguarda o deploy, e posta o carrossel no
Instagram + Facebook via Meta Graph API.

**Invoke:** `/aprovar-post [numero]`

**Exemplo:** `/aprovar-post 5` ou `/aprovar-post 12`

---

## O que faz (passo a passo)

1. **Verificar draft do post**
   - Lê `dados/posts/draft/post-[numero].md`
   - Se não existir, avisa erro

2. **Mover pra published**
   - Move de `draft/` pra `published/`
   - Post agora fica em `dados/posts/published/post-[numero].md`

3. **Copiar imagens do carrossel**
   - Lê lista de imagens no post
   - Copia PNGs de `dados/imgs/posts/[numero]/` para `saidas/public/posts/[numero]/`
   - Verifica se todas foram copiadas ✓

4. **Fazer commit e push**
   - `git add .`
   - `git commit -m "Publica post #[numero]"`
   - `git push origin main`

5. **Aguardar deploy**
   - Verifica Netlify/Vercel até site atualizar
   - Timeout: 5 minutos
   - Se timeout, avisa ao usuário

6. **Postar no Instagram + Facebook**
   - Lê credenciais de `.env.local` (INSTAGRAM_TOKEN, FACEBOOK_TOKEN)
   - Faz chamada à Meta Graph API
   - Posta carrossel (automático com as imagens copiadas)
   - Retorna link do post publicado

7. **Confirmação final**
   - Mostra: ✅ Post #[numero] publicado
   - Links: blog, Instagram, Facebook

---

## Arquivos usados

- `dados/posts/draft/post-[numero].md` (entrada)
- `dados/posts/published/post-[numero].md` (saída)
- `dados/imgs/posts/[numero]/` (imagens do carrossel)
- `saidas/public/posts/[numero]/` (cópia pra deploy)
- `.env.local` (tokens de API)
- `.git/` (repositório)

---

## Integração com ChatGPT + Codex

No Chat do Codex, digitar:

```
/aprovar-post 5
```

O Codex vai executar sequência completa (1-7 acima).

---

## Outputs esperados

- ✅ Post moveido de draft → published
- ✅ Imagens copiadas pra public folder
- ✅ Commit feito e pusheado
- ✅ Site redeplogado (Netlify/Vercel)
- ✅ Carrossel postado no Instagram
- ✅ Carrossel postado no Facebook
- ✅ Links de confirmação

---

## Quando usar

- Quando post tá pronto e revisado
- Quando imagens tão finalizadas
- Quando conteúdo foi aprovado internamente

---

## Pré-requisitos

Antes de usar essa skill:

1. **Post deve existir em draft**
   - Arquivo: `dados/posts/draft/post-[numero].md`
   - Formato: Markdown com frontmatter

2. **Imagens devem existir**
   - Pasta: `dados/imgs/posts/[numero]/`
   - Formato: PNG

3. **Credenciais configuradas**
   - `.env.local` com:
     - `INSTAGRAM_TOKEN=seu_token`
     - `FACEBOOK_TOKEN=seu_token`
   - Tokens do Meta Business Manager

4. **Repositório Git configurado**
   - Remote `origin` apontando pra GitHub
   - Permissão pra fazer push

---

## Troubleshooting

- **Erro: "post-[numero].md not found"**
  - Verificar se arquivo existe em `dados/posts/draft/`
  - Verificar ortografia do número

- **Erro: "Images not found in [caminho]"**
  - Verificar se pasta `dados/imgs/posts/[numero]/` existe
  - Verificar se tem arquivos `.png` lá

- **Erro: "API authentication failed"**
  - Verificar `.env.local`
  - Gerar novo token no Instagram/Facebook
  - Rodar `/debug` pra ver mais detalhes

- **Deploy timeout (5min)**
  - Pode ser falha da Netlify/Vercel
  - Verificar painel de deploy
  - Tentar `/aprovar-post [numero]` de novo

- **Post criado mas não aparece no Instagram/Facebook**
  - Verificar se account está conectado ao Business Manager
  - Verificar permissões do token
  - Reautenticar em `.env.local`

---

## Variações

### Aprovar sem postar no Instagram/Facebook
```
/aprovar-post [numero] --no-social
```
Apenas publica no blog, não posta em redes.

### Aprovar com mensagem customizada
```
/aprovar-post [numero] --message="Novo post: [titulo]"
```
Usa mensagem customizada em vez de gerar automático.

### Pré-visualizar antes de publicar
```
/aprovar-post [numero] --preview
```
Mostra o resultado final sem fazer push.

---

## Próximos passos

1. Configurar `.env.local` com tokens
2. Criar primeiro post em `dados/posts/draft/`
3. Adicionar imagens em `dados/imgs/posts/1/`
4. Rodar `/aprovar-post 1`
5. Verificar se tudo funcionou nos três lugares (blog, Instagram, Facebook)

---

## Ver status

Pra ver posts publicados:
```bash
ls dados/posts/published/
```

Pra ver logs da última publicação:
```bash
git log --grep="Publica" --oneline -5
```
