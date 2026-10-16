---
title: "Lição 12 - Publicar o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Dê ao Space Quiz um endereço público publicando-o com o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a publicação, mas cabe a você revisar as mudanças e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot que configure a publicação com o GitHub Pages.
- revisar o fluxo de trabalho e o pull request antes de fazer o merge.
- acompanhar a publicação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma forma simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages disponibiliza uma URL pública sem adicionar um servidor nem dependências de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um fluxo de trabalho do GitHub Actions que compile o site se necessário e o publique no GitHub Pages. Se ainda não houver um README, adicione um que descreva o aplicativo e como executá-lo localmente. Crie um pull request com essas mudanças e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a publicação até que ela seja concluída e, em seguida, informe a URL final do site. Se você não tiver permissão para habilitar o Pages ou fazer o merge, informe exatamente o que preciso aprovar ou fazer; não diga que a tarefa foi concluída antes de o site estar no ar.
```

![Diagrama de três etapas: um pull request do space-quiz mesclado; uma execução bem-sucedida de Deploy website no GitHub Actions com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça o merge de um pull request e altere as configurações do Pages do repositório. Antes de continuar, revise o diff, as permissões de publicação e qualquer solicitação de aprovação do GitHub.

## Revise o fluxo de trabalho e verifique a publicação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as mudanças do pull request, incluindo as etapas de build e publicação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de publicação do GitHub Actions até ela ser concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não conseguir habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas que ele fornecer. Não considere a tarefa concluída até a publicação ser bem-sucedida e o site carregar.

## Resumo e próximos passos

Agora o Space Quiz está publicado, e você verificou o site em vez de confiar apenas no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
