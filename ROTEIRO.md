# Clonando apps com REA — roteiro de perguntas

Copie os prompts para o seu agente de IA conectado ao REA. Troque os campos entre colchetes. Você não precisa conhecer os comandos internos da ferramenta.

Use o prompt rápido ou siga a sequência guiada. Envie uma etapa por vez e aproveite a resposta anterior. Se a informação já estiver clara, pule a pergunta correspondente.

## Começo rápido: um único prompt

```text
Use $clonar-app para investigar [APP: nome, link ou caminho] e me guiar na criação de uma versão própria de [FUNÇÕES DESEJADAS; se não souber, escreva “fluxo principal”].

Comece pelo que o REA consegue analisar neste ambiente. Identifique a estrutura do app e escolha o menor fluxo completo que vale reproduzir primeiro. Separe descobertas comprovadas, hipóteses e partes ainda desconhecidas. Antes de implementar, apresente o fluxo e como vamos verificar se funciona.

Faça apenas as perguntas que mudam o resultado. Reaproveite evidências, consulte resumos e trechos, e guarde notas para retomarmos sem repetir a investigação.
```

Se a skill não estiver instalada, substitua `Use $clonar-app` por `Use o REA`. Os prompts guiados abaixo também podem ser usados sem a skill.

## Sequência guiada

### 1. O que conseguimos investigar?

```text
Quero criar uma versão própria de [APP: nome, link ou caminho]. Use o REA para identificar o que conseguimos analisar com o acesso e as ferramentas disponíveis. Comece por uma inspeção resumida. O que temos em mãos, quais são os limites e qual é o próximo passo útil?
```

Resultado esperado: alvo identificado, capacidades disponíveis e bloqueios concretos. Evita começar por uma análise completa sem saber se o app é compatível.

### 2. Como esse app está dividido?

```text
Com base nas evidências já obtidas, quais partes cuidam da interface, das funções principais, dos dados salvos e da comunicação com servidores? Mostre um mapa simples. Diferencie o que foi encontrado do que é hipótese e indique as evidências principais. Aprofunde só onde isso muda o caminho da reconstrução.
```

Resultado esperado: entender quais peças podem ser estudadas localmente e quais dependem de serviços externos.

### 3. Por onde começamos?

```text
Meu objetivo é [O QUE QUERO REPRODUZIR]. Qual fluxo completo devemos recriar primeiro para ter um resultado útil e demonstrável? Descreva as ações do usuário, os resultados esperados e o que precisa ficar salvo. Se eu ainda não defini funções, recomende um fluxo principal e explique a escolha.
```

Resultado esperado: uma primeira entrega com começo e fim. Um projeto maior pode continuar depois por outros fluxos.

### 4. O que acontece quando uso essa função?

```text
Investigue este fluxo: [EXEMPLO: criar um item, editar e salvar]. O que acontece entre a ação do usuário e o resultado? Use o REA onde houver suporte e relacione interface, funções, dados e chamadas externas. Reaproveite as evidências existentes. Separe observação, inferência e desconhecido; não atribua a REA resultados de outras ferramentas. Use um arquivo de teste descartável para alterações.
```

Resultado esperado: um caminho técnico ligado ao comportamento que queremos reproduzir. Um nome de função sozinho não comprova o funcionamento inteiro.

### 5. Já temos o necessário para construir?

```text
Para reproduzir esse fluxo, o que já sabemos e qual dúvida ainda pode mudar a implementação? Resolva apenas essas dúvidas com as ferramentas disponíveis. Apresente um plano curto, os critérios de teste e as partes que precisarão de implementação própria ou substituição. Não trate mocks como funções concluídas.
```

Resultado esperado: uma decisão baseada em evidências sobre a primeira construção, sem investigar o aplicativo inteiro por precaução.

## Quando decidir construir

Este prompt inicia a implementação; os anteriores orientam a investigação.

```text
Implemente o fluxo que acabamos de definir em [PROJETO OU PASTA], para [NAVEGADOR, COMPUTADOR OU CELULAR]. Reuse a stack existente; se começarmos do zero, escolha uma solução simples compatível. Entregue interface, ação, resultado e persistência quando necessária. Compare com a referência nos cenários definidos e informe o que funciona, o que foi testado e o que falta.
```

## Para continuar depois

```text
Retome pelas notas e evidências salvas deste projeto. Resuma onde paramos e continue pela próxima pendência que muda o resultado, sem repetir análises concluídas. Só refaça uma análise se o alvo ou a entrada mudou, ou se o bloqueio anterior foi resolvido.
```

## Exemplo para a live: Figma

```text
Use $clonar-app para investigar o Figma e planejar uma versão própria do fluxo de criar uma forma, selecionar, alterar tamanho e cor, desfazer/refazer e salvar. Reaproveite nossa investigação anterior. Identifique o que falta observar em um arquivo descartável e proponha a primeira entrega verificável.
```

## Como gastar menos tokens

- Diga qual app e qual resultado você quer; não precisa antecipar a arquitetura.
- Prefira “investigue o fluxo X” a “analise tudo”.
- Peça resumo com referências; deixe saídas grandes em arquivos locais.
- Reaproveite as notas e faça a próxima pergunta sobre a dúvida que restou.
- Se houver um bloqueio, peça uma alternativa suportada antes de repetir a chamada.

Trabalhe com apps e materiais aos quais você tenha acesso autorizado. “Clonar”, neste roteiro, significa investigar uma referência e construir uma versão própria; o resultado e a fidelidade precisam ser demonstrados por testes.
