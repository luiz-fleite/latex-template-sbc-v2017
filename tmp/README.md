# Diretório Temporário (`tmp/`)

Este diretório serve como uma área de rascunho ("sandbox") para testes e diagnósticos.

- **Propósito:** Armazenar arquivos de comparação (diffs), PDFs de referência e versões experimentais do artigo sem poluir a raiz do projeto.
- **Conteúdo Típico:**
    - `visual_diff.pdf`: Comparação visual entre versões.
    - `*_fonts.txt`: Análise técnica de fontes embutidas.
    - `ref_text.txt`: Texto extraído para verificação.
- **Nota:** O conteúdo desta pasta é versionado no Git por opção do usuário, permitindo rastrear o histórico de testes e comparações.
