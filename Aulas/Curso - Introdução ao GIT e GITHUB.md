# Curso - Introdução ao Git e GitHub

**GIT**: sistema de abstecimento de codigos distribuidos
**GITHUB**: repositório de códigos
-controle de versões
-armazenamento em nuvem
-trabalho equipe
-melhora codigo
-reconhecimento

**GUI X CLI**
GUI - forma de interagir por interface gráfica
CLI - forma de interagir por linha de comando

**CLI - GIT**
windows (shell)- cd, dir, mkdir, del/rmdir
Unix (bash) - cd, ls, mkdir, rm-rf

**COMANDOS**
*cd+ pasta :leva para base do diretório C
*cls : limpa a tela, o terminal windows
*TAB : auto completa nomes
*mkdir : criar uma pasta (ex. workspace)
*echo : devolve o que digitou
*del : delete arquivos
*rmdir : deleta repositórios

**GIT POR BAIXO DOS PANOS**
*SHA1 - algorítmo de incriptação, ele pega o arquivo e embaralha o código de maneira bem especifica (40digitos) que servem como caracteres de identificação --> segurança
(a cada mudança os caracteries mudam)
É A FORMA CURTA DE REPRESENTAR UM ARQUIVO

**OBJETOS INTERNOS DO GIT**
1-BLOBS- onde os arquivos ficam armazenados. O Blob tem metadados. Tem o tipo, tamanho,\0 e o conteúdo.
2-TREE- armazenam BLOBS. tem tbm metadados e apontam para um blob que contem o SHA1. Ela tbm armazena o nome e pode apontar para blobs ou outras arvores e tbm te o SHA1 incriptado.
3-COMMIT- mais importante, da sentido. Aponta pra tudo, autor, mensagem... O SHA1 desse commit é o hash de toda essa informação.
Ajuda na segurança. Qualquer alteração vai acabar aparecendo. 

**PRIMEIROS COMANDOS COM GIT**
*git init
*git add
*git commit

ls(listar)->cdworkspace->mkdir livro-receitas(cirou a pasta)->
cd livro-receitas->git init (iniciou um repositório vazio)->
ls -a(mostra arquivos ocultos, ex.livro-receitas)->
git config --global user.email "blablabla"->
git config --global user.name  BLA->

git add * ->git commit -m "commit inicial" (ou qualquer coisa)->
git status (vê status. diretório de trabalho, repositório...)->
mv strogonoff.md ./receitas/ (move a pasta)->
git add (nome arquivo)... ->

GIT INIT - cria um repositório
*tracked (rastreável)
-unmodififed: não modificado
-modified: modificado
-staged: arquivos que estão se preparando pra fazer parte ou executar uma ação, PARA FAZER PARTE DE UM COMMIT

*untracked (git não tem ciencia)

Quando você cria um arquivo ele ta untracked, daí se add ele ele vai para staged.

*ambiente de desenvolvimento
-diretório de trabalho (untracked)
-staging (unmodified-modified)
-repositório local (commit)
*repositor/servidor

**RESOLVENDO CONFLITOS**
*CONFLITO DE MERGE - 2 pessoas mexendo no mesmo código na mesma linha ( deixa que abre o arquivo que teve conflito na mesma linha e pode alterar)

git pull origin master (puxa o conteudo do github)
