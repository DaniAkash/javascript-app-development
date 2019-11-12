---
id: IntelliSense
title: IntelliSense
sidebar_label: IntelliSense
---

Have you ever heard of IntelliSense ? Does it sound like a language from far away galaxy ? No it's not. We use this in most of the IDE's. Familar one was VScode, which are developed by *Microsoft*. 

## Quick Glance

Microsoft built this tool with advanced algorithms which will help developers to code in their IDE within few key strokes, this eventually helped in lot of time-saving.Some call Intellisense's feature as "code completion"and others call it as "content assist", and "code hinting". With all these features and other features such as parameter info, quick info, list members Visual Code's IntelliSense pops up its position among developers.

Let's see IntelliSense's supported languages, features, types, troubleshoot below.

### Supported Lanuages
Currently, VS Code IntelliSense is provided for JavaScript, TypeScript, JSON, HTML, CSS, Less, and Sass out of the box. VS Code supports word based completions for any programming language but can also be configured to have richer IntelliSense by installing a language extension.

![Intellisense Example](website/static/img/intellisense_image.png?raw=true )

VS Code IntelliSense features are powered by a language service. A language service provides intelligent code completions based on language semantics and an analysis of your source code. If a language service knows possible completions, the IntelliSense suggestions will pop up as you type. If you continue typing characters, the list of members (variables, methods, etc.) is filtered to include only members containing your typed characters. Pressing ` kbstyle(Tab) ` or `kbstyle(Enter)` will insert the selected member.

ou can trigger IntelliSense in any editor window by typing `kb(editor.action.triggerSuggest)` or by typing a trigger character (such as the dot character `(kbstyle(.))` in JavaScript).

