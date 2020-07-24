# Criar Branch vazia
  - Referência: [Ask Stackoverflow](https://pt.stackoverflow.com/questions/86644/como-criar-um-branch-limpo-sem-levar-o-hist%C3%B3rico-do-master-branch)

* Primeiro crie um branch orfão:
`git checkout --orphan gh-pages`

* Agora remova todos os arquivos deste branch:
`git rm -rf .`
`git clean -fdx`

* Adicione algum arquivo, por exemplo README.md:
`echo > README.md`
`git add .`
`git commit "chore(app): initial commit"`

* Agora basta fazer o push para o servidor:
`git push origin gh-pages`

* Faça um checkout para o master e veja os branchs existentes:
`git checkout master`
`git branch`