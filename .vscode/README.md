# Configurações do VS Code (`.vscode/`)

Este diretório contém as configurações que automatizam o fluxo de trabalho acadêmico para este projeto. O objetivo é proporcionar uma experiência "salvou, compilou, atualizou", similar ao Overleaf, mas com as vantagens de um ambiente local organizado.

## 🛠️ Automação de Build (LaTeX Workshop)

As configurações em `settings.json` definem uma receita de build customizada chamada **Tectonic**:

1.  **Ferramenta `tectonic`**: 
    - Executa o motor Tectonic com o argumento `--outdir=build`.
    - **Por que?** Implementa o *Out-of-source build*, mantendo os arquivos auxiliares (`.aux`, `.log`, `.synctex`) isolados para não sujar a raiz do projeto.
2.  **Ferramenta `copyPdf`**:
    - Um comando de pós-processamento (`cp build/main.pdf main.pdf`).
    - **Por que?** Como o Tectonic coloca tudo na pasta de saída, este comando traz o PDF final de volta para a raiz, facilitando o acesso rápido e visualização.

## ⚙️ Configurações Importantes

- **`latex-workshop.latex.autoBuild.run`**: Configurado como `onSave`. O artigo é recompilado instantaneamente ao salvar.
- **`latex-workshop.synctex.afterBuild.enabled`**: Ativado para permitir o "Click-to-Source". Você pode clicar no PDF e o VS Code abrirá a linha correspondente no LaTeX.
- **`latex-workshop.latex.outDir`**: Aponta para `%DIR%/build`. Isso garante que a extensão procure os logs de erro e o mapa de sincronização no lugar certo.

## 📦 Extensões Recomendadas (`extensions.json`)

- **James-Yu.latex-workshop**: Essencial para o funcionamento de todas as automações acima.

---
*Nota: Se você alterar a estrutura de pastas ou o nome do arquivo principal (`main.tex`), lembre-se de atualizar os caminhos nestas configurações.*
