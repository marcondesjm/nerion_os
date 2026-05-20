# Sistema Operacional NERION

> O sistema operacional do seu negocio dentro do CODEX.

Voce acabou de instalar o NerionOS. Em alguns minutos, sua empresa vai ter
uma memoria propria, uma identidade visual aplicada em tudo que o sistema
gera, e 15 habilidades prontas para fazer marketing, SEO, anuncios e operacao
rodarem com voce dirigindo.

Bora voar.

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
