# Clonar app com REA

Skill em português para guiar iniciantes na engenharia reversa e recriação de aplicativos, com poucas perguntas e investigação focada.

## Como usar

Instale a pasta desta skill no diretório de skills do seu agente e inicie com:

```text
Use $clonar-app para recriar este app: [nome, link ou caminho do arquivo].
```

Você também pode especificar o objetivo:

```text
Use $clonar-app para recriar o fluxo de cadastro deste app: [referência].
```

A skill identifica o que falta, investiga a referência, implementa o escopo solicitado e compara os comportamentos observáveis. Não exige que o usuário saiba formular perguntas técnicas.

## REA e requisitos

Para investigar binários e pacotes, é necessário ter o [REA](https://github.com/morluto/rea) disponível no ambiente. Esta skill contém instruções; não instala nem configura o REA automaticamente. Sem REA, o agente continua com os materiais e ferramentas disponíveis e informa as limitações.

O agente precisa ter acesso à referência e às ferramentas necessárias para a implementação. A fidelidade depende das evidências disponíveis; uma interface reproduzida não comprova equivalência do aplicativo inteiro.

## Economia de tokens

As instruções priorizam resumos, consultas focadas, reaproveitamento de evidências e notas para retomada. Não há percentual garantido de economia.

## Arquivos

- [SKILL.md](SKILL.md): instruções do fluxo.
- [agents/openai.yaml](agents/openai.yaml): nome e prompt de entrada na interface.

Use referências e materiais aos quais você tenha acesso autorizado. A skill não orienta contornar autenticação ou licenças.
