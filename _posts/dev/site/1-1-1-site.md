---
layout: dev
title: Site
special: [site, subsite]
---

##Instalando o Jekyll no linux

1. Instale as dependencias: `sudo apt-get install nodejs ruby ruby1.9.1-dev`
1. Instale o Jekyll: `sudo gem install jekyll`
1. Instale o Git: `sudo apt-get install git`

##GitHub

1. Faça uma conta
1. Mande um e-mail para o grupo para ser autorizado a fazer modificações

<div class="bs-callout bs-callout-danger">
  <h4>Atenção: Certifique-se que seu e-mail é verificado</h4>
</div>

##Testando o site localmente

1. Configure o seu git (importante!)
	1. Coloque seu nome: `git config user.name "Fulano da Silva"`
	1. Coloque seu e-mail: `git config user.email "fulano@servidor.com"`
1. Crie uma pasta para guardar o site: `mkdir SiteRoboFun`
1. Entre na pasta: `cd SiteRoboFun`
1. Baixe o site para o seu computador: `git clone --depth=1 https://github.com/petrobo/petrobo.github.io.git`
1. Entre na pasta do site: `cd petrobo.github.io`
1. Rode o servidor local: `jekyll serve`
1. Entre no endereço local: [http://localhost:4000](http://localhost:4000)

##Estrutura do Site

- Os posts do blog ficam em: `/_posts/blog`
- As imagens dos posts do blog ficam em: `/assets/img/posts`
- Os exercicios ficam em: `/_posts/apostila/problemas`
- As imagens dos exercicios ficam em: `/assets/img/exercicios`


<div class="bs-callout bs-callout-warning">
  <h4>Atenção:</h4>
  Todos os arquivos devem ter o nome no formato <code>YYYY-MM-DD-nome-do-post.md</code> onde <code>YYYY</code>,<code>MM</code> e <code>DD</code> corresponde a ano, mês e dia respectivamente.
</div>

##Salvando alterações no GitHub

<div class="bs-callout bs-callout-danger">
  <h4>Atenção: </h4>
  Se você estiver utilizando os computadores da sala do PET, certifique-se que você atualizou seu email usando o comando <code>git configure user.email "fulano@servidor.com"</code>
</div>

1. Certifique-se que seu repositório local está atualizado: `git pull origin master`
1. Verifique como estão suas alterações: `git status`
	- Os arquivos listados devem ser apenas os que você queria adicionar/editar
	- Muito cuidado para não excluir arquivos ou editar arquivos importantes!
1. Adicione os arquivos modificados no fluxo de trabalho: `git add .`
	- Caso você tenha excluido algum arquivo, verifique se é isso mesmo que você quer e use: *git add -A*
1. Verifique se está tudo certo usando: `git status`
	- Dá tempo ainda de adicionar aquele arquivo que você esqueceu ;)
1. Salve suas alterações localmente: `git commit -m "Adicionei isso, Alterei aquilo e Deletei etc"`
1. Mande suas alterações para o servidor remoto: `git push origin master`
	- Caso alguém fez uma alteração no servidor você talvez precise rodar `git pull origin master` novamente
	- Caso vocês modificaram o mesmo arquivo o processo é mais complicado, [leia isso](http://git-scm.com/book/pt-br/v1/Ramifica%C3%A7%C3%A3o-Branching-no-Git-B%C3%A1sico-de-Branch-e-Merge) ou mande um e-mail no grupo
	





Duvidas sobre Git? Acesse: [http://rogerdudler.github.io/git-guide/index.pt_BR.html](http://rogerdudler.github.io/git-guide/index.pt_BR.html)
