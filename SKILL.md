---
name: clonar-app
description: Guia usuários iniciantes na engenharia reversa e recriação de um app ou funcionalidade com REA, de uma referência até uma implementação verificável. Use para pedidos como clonar este app, fazer um app igual ou descobrir como esta função funciona.
---

# Clonar app

Transforme uma referência em uma versão própria e funcional, com poucas perguntas e investigação focada. Responda no idioma do usuário, sem exigir vocabulário técnico. “Qualquer app” é um ponto de entrada; a fidelidade possível depende do acesso e das evidências.

## Começo fácil

Reaproveite o contexto. Pergunte somente o que falta, em um único bloco curto:

- Sem alvo: “Qual app você quer recriar? Pode mandar o nome, link ou caminho do arquivo.”
- Sem objetivo: “O que quer reproduzir: aparência, uma função específica ou o fluxo principal? Se não souber, começo pelo fluxo principal.”

Não envie um questionário técnico. Descubra plataforma e tecnologias nos arquivos e ferramentas disponíveis. Se o destino continuar indefinido e mudar a implementação, pergunte “Vai usar no navegador, computador ou celular?”; sugira uma opção baseada na referência. Não assuma web para recursos que dependam de hardware ou APIs nativas.

Com alvo claro, comece a inspeção disponível enquanto resolve dúvidas independentes. Um pedido de investigação autoriza investigar; implemente quando o usuário pedir recriação. Se pedir o app inteiro, mantenha esse objetivo e divida a entrega em partes verificáveis, começando pelo caminho principal.

## Investigue com uma pergunta concreta

1. Identifique o alvo e materiais disponíveis: app instalado, pacote, página, imagens ou código. Nome ambíguo exige seleção; não use um app vizinho como alvo.
2. Se houver REA, use as ferramentas anunciadas e seus schemas reais. Se disponível, consulte a skill `reverse-engineer-anything` para os detalhes técnicos necessários. Código-fonte completo pede ferramentas normais do repositório; screenshots permitem inferir aparência, não provar arquitetura ou comportamento interno.
3. Comece por inventário/resumo. Selecione apenas telas, módulos, eventos, arquivos e chamadas ligados ao fluxo escolhido. Só aprofunde quando isso resolver uma dúvida que altera a implementação.
4. Para cada comportamento relevante, registre entrada, ação, saída, estado persistido e falha observável. Separe observado, inferido e desconhecido; associe evidência por arquivo/localização ou ID retornado.

Sem REA conectado, confira CLI e capacidades existentes antes de orientar configuração. Não invente comandos ou resultados. Continue a parte suportada e explique o bloqueio específico. Não instale dependências nem altere configuração global silenciosamente.

## Reconstrua e confira

Escreva um contrato curto do fluxo escolhido: ações do usuário, resultados esperados e critérios observáveis de conclusão. Informe a abordagem em poucas linhas e siga o trabalho autorizado, sem pedir aprovação de plano rotineira.

Implemente uma fatia completa: interface → ação → resultado → persistência, quando aplicável. Reuse a stack do projeto; escolha a solução mais simples compatível quando começar do zero. Backend inacessível continua desconhecido: explicite substituições e mocks. Uma tela com dados fictícios não comprova funcionamento completo.

Compare referência e versão própria nos mesmos cenários: caminho principal, erro relevante e recarga/reabertura quando houver persistência. Use medidas visuais para aparência e entradas/saídas para comportamento. Não declare equivalência total a partir de cobertura parcial. Informe o que funciona, o que foi verificado e o que falta; continue pelas partes restantes do escopo autorizado.

## Economize contexto

- Guarde notas curtas no projeto, com alvo/versão, escopo, evidências, decisões, pendências e próximo passo. Reabra essas notas ao retomar.
- Use resumos, filtros e páginas. Salve saídas grandes em arquivo e leia trechos; não despeje bundles, código minificado ou listas inteiras no chat.
- Reaproveite evidências; repita análise apenas após mudança do alvo, entrada ou bloqueio.
- Não investigue funções fora do escopo nem carregue manuais inteiros preventivamente.
- Atualizações curtas: descoberta útil, decisão e próximo passo. Não prometa uma economia percentual de tokens sem medição.

Trabalhe com o acesso disponível; não contorne autenticação ou licenças. Use identidade e recursos próprios na reconstrução, salvo materiais fornecidos ou autorizados. Não execute compras, publicações ou alterações em contas como parte implícita de observar um fluxo.
