# NERION OS

> Sistema operacional do negocio rodando com ChatGPT, Codex e memoria propria.

O NERION OS organiza o contexto, a identidade, os processos e as habilidades
do seu negocio dentro de uma pasta versionada no GitHub. A ideia e simples:
o trabalho deixa de ficar solto em conversas e passa a rodar em cima de uma
base viva, com memoria, padroes e comandos reutilizaveis.

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

O NERION OS nao e apenas uma colecao de prompts. Ele e uma forma de dar
continuidade ao trabalho com IA: contexto persistente, processos claros,
arquivos versionados e aprendizado acumulado.

Cada melhoria feita aqui fica registrada para a proxima sessao.
