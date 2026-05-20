# Sistema Operacional NERION

> O sistema operacional do seu negocio dentro do CODEX.

Voce acabou de instalar o NerionOS. Em alguns minutos, sua empresa vai ter
uma memoria propria, uma identidade visual aplicada em tudo que o sistema
gera, e 15 habilidades prontas para fazer marketing, SEO, anuncios e operacao
rodarem com voce dirigindo.

Bora voar.

---

## Ligando o sistema

Dois caminhos. Escolhe o que combina contigo.

### Pelo CODEX (mais rapido)

Abre o CODEX em qualquer pasta e cola:

```text
Clona o https://github.com/marcondesjm/nerion_os/ na pasta atual,
entra nela e roda o /instalar.
```

Ele clona, entra na pasta nova e dispara a entrevista de configuracao. Voce
so responde.

### Pelo terminal (mais previsivel)

```bash
git clone https://github.com/marcondesjm/nerion_os/
cd nerion_os
code .
```

Na janela do VS Code que abre: terminal integrado -> `codex` -> `/instalar`.

Quando `/instalar` terminar, renomeia a pasta `NerionOS/` pro nome do seu
negocio (fecha o VS Code, renomeia no Explorer/Finder, abre de novo). A pasta
nao fica como "NerionOS": ela e o seu negocio agora.

O `/instalar` roda uma vez so. Ele entrevista sobre o negocio, monta a memoria
e configura o sistema. Depois disso, e so usar.

---

## O que tem aqui

**Memoria do negocio**

`_memoria/` guarda informacoes importantes sobre empresa, preferencias,
estrategia, foco atual e aprendizados que nao devem ser repetidos toda vez.

**Identidade**

`identidade/` centraliza guia visual, tom, padroes de marca e referencias
para materiais criados pelo sistema.

**Skills**

`.nerion/skills/` guarda habilidades locais do NERION OS. Cada skill descreve
um processo repetivel que o Codex pode executar seguindo um padrao.

**Templates**

`templates/` contem modelos para perfis, identidade, ferramentas e novas
skills.

**Saidas e operacao**

`marketing/`, `saidas/`, `dados/` e `scripts/` organizam materiais gerados,
entradas de trabalho e automacoes.

---

## O sistema

**Nucleo** - o jeito de operar o dia a dia

`/abrir` carrega o contexto antes de cada sessao de trabalho. `/salvar` faz
commit + push no GitHub. `/atualizar` varre o projeto e atualiza a memoria.
`/novo-projeto` cria massa isolada pra cada cliente ou iniciativa.
`/mapear-rotinas` descobre o que voce repete e transforma em habilidade
personalizada.

**Conteudo e SEO** - vitrine publica da empresa

`/carrossel` cria carrosseis 1080x1350 com identidade da marca, com ou sem
foto IA. `/publicar-tema` pega um tema e entrega artigo de blog + carrossel
+ 3 legendas amarradas. `/seo` roda fluxo completo de 8 passos: demanda,
concorrencia, GMB, on-page, conteudo, anuncios, monitoramento e GEO.
`/responder-avaliacoes` escreve respostas humanas pras reviews do Google.
`/aprovar-post` publica blog + Instagram + Facebook num comando.

**Anuncios pagos** - onde o dinheiro entra

`/anuncio-google` monta a campanha inteira em CSV pronto para importar no
Google Ads Editor. `/relatorio-ads` le as exportacoes do Google + Meta e
devolve relatorio semanal com alertas e recomendacoes.

**Producao** - ferramentas do dia a dia

`/analisar-dados` le CSV/XLSX/PDF e gera resumo executivo.
`/email-profissional` rascunha email a partir de contexto livre.

---

## Como usar

Abra esta pasta no VS Code com o Codex configurado.

No comeco de uma tarefa, o Codex deve considerar:

1. `NERION-OS.md`
2. `_memoria/empresa.md`
3. `_memoria/preferencias.md`
4. `_memoria/estrategia.md`
5. `identidade/design-guide.md`, quando a tarefa for visual

Quando existir uma skill relevante em `.nerion/skills/`, ela deve ser usada
como fluxo principal da tarefa.

---

## Estrutura principal

```text
.
├── NERION-OS.md
├── README.md
├── _memoria/
├── .nerion/
│   └── skills/
├── dados/
├── identidade/
├── marketing/
├── saidas/
├── scripts/
└── templates/
```

---

## Tese

IA nao e uma ferramenta que sua empresa usa. E o sistema operacional em que
ela roda.

A diferenca nao e velocidade. E capacidade nova: uma pessoa com IA constroi
o que antes exigia um time inteiro. Cada processo critico que hoje roda em
open loop (decide -> executa -> nao mede -> repete cego) vira closed loop
dentro do NerionOS (decide -> executa -> captura -> realimenta -> ajusta
sozinho).

O sistema nao substitui voce. Vira parte da sua empresa.

---

## Como o NerionOS pensa

`_memoria/` e o cerebro. Tudo o que importa do seu negocio mora aqui:
quem e a empresa, como ela fala, o que esta em foco essa semana. O Codex
le isso antes de cada resposta. Quanto melhor a memoria, melhor o sistema.

`identidade/` e o rosto. Cores, fontes, logotipo, padrao visual. Todo
carrossel, slide ou peca que o sistema gera respeita isso.

`marketing/`, `saidas/` e `scripts/` sao o resultado. O sistema produz,
versiona no GitHub e fica tudo seu.
