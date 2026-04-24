# Template SBC Conferences 2017 para Tectonic e VS Code
Adaptação do **template oficial da SBC Conferences (2017)** para uso **local**, mantendo a **máxima fidelidade visual** e estrutural ao **oficial** do Overleaf. 

## **TL;DR (Resumo Rápido):**
1. Instale o **Tectonic** e a extensão **LaTeX Workshop** no VS Code.
2. Abra o arquivo `main.tex`.
3. Salve o arquivo (`Ctrl+S`).
4. O arquivo `main.pdf` será gerado/atualizado na raiz. 
5. Habilite o `gitdoc` em [.vscode/settings.json](.vscode/settings.json) (opcional)

---

## 📄 Sobre o Projeto

Este é um template LaTeX otimizado para edição de artigos no padrão da **Sociedade Brasileira de Computação (SBC)** localmente. Ele foi configurado para ser o **mais semelhante em todos os aspectos** ao **template oficial da SBC Conferences de 2017** publicado oficialmente no overleaf. 

Para isso, foi escolhido:
- Motor LaTeX **Tectonic**: Compilador de LaTeX escrito em Rust, leve, rápido, baixa as dependencias sob demanda, é autossuficiente e é multiplataforma (Windows, Linux, Mac). 
- Editor de código **VS Code**: Editor de código muito popular com um excelente ecossistema de extensões, inclusive a `latex-workshop`, essencial para uma boa experiencia de edição com live preview e geração do PDF final. 

### Diferenças para o template original do overleaf 
#### Ajustes pra funcionar com Tectonic 
- **Correção de Fontes:** Configurado para usar fontes equivalentes à Times New Roman (Nimbus Roman), resolvendo problemas comuns de layout do Tectonic.
- **UTF-8 Nativo:** Pronto para caracteres acentuados modernos, substituindo o antigo `latin1`.

*Atualmente, apenas 3 linhas de importação no main.tex foram modificadas para viabilizar isso.*

#### Sugestões de organização e arquitetura 
- **Arquitetura Limpa:** Arquivos organizados em pastas (`images`, `bib`, `styles`), mantendo a raiz limpa.
- **Build Out-of-Source:** Logs e artefatos temporários são gerados na pasta `build/`, evitando poluição.

---

## 📂 Estrutura de Pastas

```text
/
├── .vscode/            # Configurações automáticas para Tectonic e LaTeX Workshop
├── images/             # Imagens e figuras (JPG, PNG, PDF)
├── bib/                # Banco de dados (.bib) e estilos (.bst) bibliográficos
├── styles/             # Arquivos de estilo (.sty) da SBC
├── build/              # Artefatos gerados (logs, aux, pdf intermediário)
├── tmp/                # Sandbox para testes e comparações (versionado)
├── main.tex            # Arquivo principal do artigo
└── main.pdf            # PDF final gerado (atualizado automaticamente)
```

---

## 🚀 Como Usar

### Pré-requisitos
1.  **Tectonic:** Um motor LaTeX moderno e autossuficiente.
2.  **VS Code:** Com a extensão `LaTeX Workshop` instalada. 

### Opcionais 
1. **GitDoc**: Extensão do vscode para habilitar salvamento automático no git (commit e push) assim como em editores de texto comuns. É possível customizar as regras em [.vscode/settings.json](.vscode/settings.json). 

### Editando e Compilando
1. Abra a pasta do projeto no VS Code.
2. Edite o arquivo `main.tex`.
3. Ao salvar (`Ctrl+S`), o build iniciará automaticamente.
4. O PDF será gerado automaticamente em `build/` e uma cópia atualizada aparecerá na raiz como `main.pdf`. 
5. Habilite o `gitdoc` em [.vscode/settings.json](.vscode/settings.json) para uma experiência de salvamento automático de editores de texto comuns (opcional) 

