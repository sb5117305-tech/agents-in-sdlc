---
title: "Lección 12 - Despliega el sitio con GitHub Pages"
description: "Usa la aplicación GitHub Copilot para configurar un flujo de trabajo de Pages, revisar su solicitud de cambios y verificar Space Quiz en directo."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Dale a Space Quiz un sitio público desplegándolo con GitHub Pages. Copilot puede preparar el flujo de trabajo y guiarte durante el despliegue, pero sigues siendo responsable de revisar los cambios y confirmar que el sitio está activo.

En esta lección:

- pide a Copilot que configure el despliegue con GitHub Pages.
- revisa el flujo de trabajo y la solicitud de cambios antes de fusionarla.
- sigue el despliegue y verifica el sitio publicado.

## Escenario

Space Quiz ya está en un repositorio de GitHub, pero la gente todavía necesita una forma sencilla de probarlo. Publicar el sitio de un solo archivo con GitHub Pages permite acceder a él desde una URL pública sin añadir un servidor ni dependencias de ejecución.

## Pide a Copilot que despliegue el sitio

En la sesión de la aplicación Copilot para `space-quiz`, envía este mensaje:

```plaintext
Enable GitHub Pages for this repository. Create a GitHub Actions workflow that builds the website if needed and deploys it to GitHub Pages. Add a README describing the app and how to run it locally if one does not already exist. Create a pull request with these changes and merge it after required checks pass. Monitor the deployment until it succeeds, then report the final URL of the live website. If you lack permission to enable Pages or merge, tell me exactly what I need to approve or do; do not report success until the site is live.
```

![Diagrama de tres etapas: una solicitud de cambios de space-quiz fusionada; una ejecución correcta de GitHub Actions Deploy website con los pasos Build website, Upload artifact y Deploy to Pages; y Space Quiz activo en yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este mensaje pide al agente que cree y fusione una solicitud de cambios y que modifique la configuración de Pages del repositorio. Revisa el diff, los permisos de despliegue y cualquier solicitud de aprobación de GitHub antes de continuar.

## Revisa el flujo de trabajo y verifica el despliegue

1. Confirma que el README solo se añade si el repositorio aún no tiene uno.
2. Revisa los cambios de la solicitud de cambios, incluidos los pasos de compilación y despliegue del flujo de trabajo.
3. Fusiona los cambios solo cuando se superen las comprobaciones requeridas de la solicitud de cambios.
4. Sigue la ejecución del despliegue de GitHub Actions hasta que termine correctamente.
5. Abre la URL indicada y confirma que Space Quiz se carga.

Si el agente no puede activar Pages ni fusionar la solicitud de cambios, sigue las instrucciones específicas que te proporcione. No des la tarea por terminada hasta que el despliegue se complete correctamente y el sitio esté disponible.

## Resumen y siguientes pasos

Space Quiz ya está disponible como sitio web y has verificado el despliegue en lugar de confiar en el informe del agente. Continúa con la [lección 13: Repaso y próximos pasos][next-lesson].

[next-lesson]: ../13-review/
