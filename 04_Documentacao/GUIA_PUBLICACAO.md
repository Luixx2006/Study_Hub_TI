# Aplicação e conclusão da entrega

## 1. Preservar o trabalho anterior
Use sua cópia local atual de Study_Hub_TI. Se não houver alterações locais pendentes, execute `git pull --ff-only`. Se houver, salve-as em commit antes de atualizar. Faça uma cópia de segurança antes de sobrepor arquivos.

Extraia o ZIP em uma pasta separada. Ele contém uma cópia da estrutura pública consultada e os novos arquivos. Copie seu conteúdo para a raiz do repositório local; preserve materiais que existirem apenas no seu computador. Não crie uma segunda pasta Study_Hub_TI dentro do repositório.

## 2. Registrar a versão 1.0.0
No terminal do VS Code, na raiz do repositório:
```bash
git status
git switch -c feat/entrega-intermediaria
git add README.md CONTRIBUTING.md CHANGELOG.md docs 01_Apresentacao_e_Perfil 02_Disciplinas_Atuais 03_Projetos_e_Certificados 04_Documentacao
git diff --cached --stat
git commit -m "feat: adiciona portfolio e ciclo de estudos"
git tag -a v1.0.0 -m "Primeira versao funcional do portfolio"
git push -u origin feat/entrega-intermediaria
git push origin v1.0.0
```
Não recrie uma tag existente. Se `v1.0.0` já existir, confira o histórico antes de escolher o próximo número. Abra um Pull Request de `feat/entrega-intermediaria` para `main`, revise e faça o merge. Depois:
```bash
git switch main
git pull --ff-only
```

## 3. Demonstrar evolução real
Crie uma nova branch e altere o rodapé de `docs/index.html`, acrescentando “Atualizado na entrega intermediária”. Atualize o CHANGELOG para registrar a mudança como concluída, valide a página e registre outro commit:
```bash
git switch -c docs/atualiza-rodape
git add docs/index.html CHANGELOG.md
git commit -m "docs: atualiza identificacao da entrega no portfolio"
git push -u origin docs/atualiza-rodape
```
Abra e mescle um segundo PR. Isso cria uma alteração posterior rastreável; executar comandos sem alterar arquivos não demonstra evolução.

## 4. GitHub Pages
Abra https://github.com/Luixx2006/Study_Hub_TI/settings/pages . Selecione **Deploy from a branch**, branch **main**, pasta **/docs** e **Save**. Aguarde a conclusão da execução em Actions. Use o endereço exibido no painel Pages; o esperado, sem domínio personalizado, é https://Luixx2006.github.io/Study_Hub_TI/ . Teste em janela anônima e no celular. Repositório deve continuar público.

## 5. Reutilizar materiais anteriores
Adicione documentos, slides e vídeo reais da etapa inicial em sua pasta existente ou inclua links acessíveis. Na seção Trajetória da página, adicione links específicos para esses materiais. O pacote não inclui arquivos anteriores que não estavam no repositório consultado.

## 6. LinkedIn
No próprio perfil, localize a opção de adicionar projeto ou um link em Destaques. Use título “Study Hub TI - Portfólio acadêmico”, URL pública do Pages e descrição: “Portfólio desenvolvido em Bootcamp I para organizar minha trajetória em ADS. Reúne projetos acadêmicos e pessoais, documentação em Markdown, versionamento com Git e publicação com GitHub Pages.” Confirme que o item aparece no perfil e capture uma imagem como evidência.

## 7. YouTube e PDF
Grave aproximadamente 5 minutos seguindo ROTEIRO_VIDEO.md. Publique como público ou não listado e teste o link sem autenticação. Atualize RELATORIO_ENTREGA.md com o link real do vídeo, do LinkedIn, do Pages e dos commits/PRs. Copie o relatório para Word ou Google Docs, insira as capturas e exporte como PDF. O PDF entregue neste pacote é uma base de revisão e não comprova publicações pendentes.

## Conferência final
- Página pública abre e os links funcionam.
- Histórico mostra versão inicial e alteração posterior.
- README de cada projeto identifica objetivo, execução e limitações.
- Materiais anteriores estão vinculados à página.
- LinkedIn e vídeo estão acessíveis.
- PDF final contém links clicáveis e capturas, sem campos pendentes.
- Enviar individualmente no AVA até 17/10/2026 às 23h55, conforme enunciado.

Referência técnica: https://docs.github.com/pt/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site
