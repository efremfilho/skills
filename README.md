# Skills do Éfrem

Coleção de skills criadas a partir de processos que uso no dia a dia. Cada skill reúne instruções para um assistente executar uma tarefa com critérios explícitos de pesquisa e decisão.

## Catálogo

| Skill | Para que serve |
| --- | --- |
| [Mecânicas especializadas](skills/mecanicas-especializadas/SKILL.md) | Encontrar e comparar oficinas para um carro, serviço e região, cruzando relatos de proprietários com referências sobre os profissionais. |

## Como ler

Abra o link da skill no catálogo. O arquivo `SKILL.md` contém as instruções completas, em texto: os campos `name` e `description` identificam a skill; o restante descreve como o assistente deve trabalhar.

Na skill de mecânicas, a pesquisa prioriza relatos detalhados em fóruns e comunidades de proprietários, além de notícias e entrevistas sobre a trajetória dos profissionais. Avaliações do Google entram como complemento. O objetivo é encontrar referências úteis para a escolha, sem investigar se comentários foram escritos por bots.

## Como instalar no Codex

Peça ao Codex:

```text
Use $skill-installer para instalar a skill deste endereço:
https://github.com/efremfilho/skills/tree/main/skills/mecanicas-especializadas
```

O instalador copia apenas a pasta escolhida. Não é necessário instalar toda a coleção. Se a skill não aparecer após a instalação, reinicie o Codex.

Depois, invoque pelo nome e informe seu contexto. Exemplo:

```text
Use $mecanicas-especializadas para procurar oficinas para um Honda Fit 2015
automático em Recife. Preciso de uma revisão e posso me deslocar até Olinda.
Priorize relatos de proprietários e explique as evidências de cada indicação.
```

O assistente precisa ter acesso à pesquisa na web para buscar referências atuais. A skill fornece o método de pesquisa; não contém uma base pronta de oficinas.

Para detalhes sobre instalação e descoberta de skills, consulte a [documentação oficial](https://learn.chatgpt.com/docs/build-skills).

## Organização

```text
skills/
└── mecanicas-especializadas/
    ├── SKILL.md
    └── agents/
        └── openai.yaml
```

Cada skill tem sua própria pasta em `skills/`. O arquivo `SKILL.md` é o ponto de entrada; `agents/openai.yaml` configura o nome e a descrição exibidos na interface.

Novas skills entram como pastas independentes e ganham um link no catálogo. Scripts, referências e outros recursos podem ficar dentro da pasta da skill quando a tarefa exigir.
