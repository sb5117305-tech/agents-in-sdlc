---
title: "Lição 12 - Implante o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um fluxo de trabalho do Pages, revisar a solicitação de pull e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz para que todos possam acessá-lo usando o GitHub Pages. O Copilot pode preparar o fluxo de trabalho e orientar a implantação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- pedir ao Copilot que configure a implantação no GitHub Pages.
- revisar o fluxo de trabalho e a solicitação de pull antes de fazer o merge.
- acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas as pessoas ainda precisam de uma maneira simples de experimentá-lo. Publicar o site de um único arquivo no GitHub Pages disponibiliza o conteúdo em uma URL pública sem adicionar um servidor ou dependência de runtime.

## Peça ao Copilot para implantar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama em três etapas: solicitação de pull do space-quiz mesclada; execução bem-sucedida do GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz no ar em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça merge de uma solicitação de pull e altere as configurações do Pages no repositório. Revise o diff, as permissões de implantação e qualquer solicitação de aprovação do GitHub antes de continuar.

## Revise o fluxo de trabalho e verifique a implantação

1. Confirme que o README foi adicionado somente se o repositório ainda não tiver um.
2. Revise as alterações da solicitação de pull, incluindo as etapas de build e implantação do fluxo de trabalho.
3. Faça o merge somente depois que as verificações obrigatórias da solicitação de pull forem aprovadas.
4. Acompanhe a execução da implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz carrega.

Se o agente não puder habilitar o Pages ou fazer o merge da solicitação de pull, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site carregue.

## Resumo e próximos passos

O Space Quiz agora está disponível como um site publicado, e você verificou a implantação em vez de confiar no relato do agente. Continue para a [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
