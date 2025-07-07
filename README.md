## Instruções para primeiro uso

1. Instalar o git (Verificar tópico específico abaixo)
2. Navegar até a pasta onde deseja salvar os arquivos do trabalho, clicar com o botão direito do mpouse e selecionar a opção **Abrir janela de comando aqui**
3. Clonar o repositório utilizando o comando abaixo dentro do prompt que abriu
```bash
git clone https://github.com/joaoxfernando/Univesp-PI-S03.git
```

Essas etapas só precisam ser feitas uma única vez, e essa última etapa irá baixar os arquivos atualizados para a sua máquina, quando você fizer alterações e quiser sincronizar ou deseja sincronizar com a versão mais recente do servidor, utilize os comandos listados no tópico específico

## Instalação do git


## Instalação do LaTeX


## Criar conta GitHub


## Trabalhando no projeto e sincronizando com o github

No geral, utilizaremos sempre o prompt de comando para sincronizar os arquivos com o github, logo, todos os comandos listados no decorrer desse tópico devem ser feitos nele e são válidos no Windows, Linux e MacOS.

O git utiliza o conceito de branch, que é uma forma de separar o **ramo** em que podemos configurar para mais de uma pessoa conseguir mexer nos arquivos sem interferir na versão principal, chamada de **main**. 

Seguiremos um padrão de nomenclatura das branchs: **nome-da-seção/nome-da-pessoa**, utilizando traços/hífens no lugar dos espaços entre o nome da seção e da pessoa e barra separando o nome da seção e o nome da pessoa. 
Exemplo: importancia-da-algebra/joao-fernando

Sempre que for realizar alguma alteração no projeto, utilize o comando **git branch** para checar em qual branch você está no momento. Se for a que você está editando. Prosseguir, caso contrário, utilize o comando **git checkout -b nome-da-branch

Após isso, você pode fazer as devidas edições nos arquivos normalmente.

Ao finalizar, para enviar as alterações para o github, você deve utilizar dois comandos:

```bash
git commit -m "inserir de forma resumida o que foi alterado"
git push -u origin nome-da-branch
```

Lembre-se, no primeiro comando, o comando git commit precisa seguir aquela regra, deve trocar apenas o conteúdo da mensagem que está dentro das aspas, mas NÃO devemos remover as aspas. Se preferir, pode enviar sem nenhuma mensagem, usando apenas o comando git commit -m ""

### Puxar atualizações do servidor

De tempos em tempos, os conteúdos das branches serão mescladas com o projeto original, até finalizarmos e gerar o projeto final, nesse intervalo, é interessante de tempos em tempos sincronizar o projeto salvo em sua máquina com o github com o comando git pull, esse comando irá baixar os arquivos mais recentes direto do github e atualizar em sua máquina.

## Principais comandos git

### git status

Verifica se há arquivos que faltam commitar e enviar pro servidor/github.

### git commit -m ""

Sempre antes de enviar qualquer alteração, precisamos fazer o commit, que é um resumo do que foi alterado, para aí sim fazer o push (envio dos dados).

### git add

Quando adicionamos algum arquivo novo no projeto, para que ele seja enviado para o github, é necessáriorodar o comando **git add nome_do_arquivo** ou **git add .** (sim, com um ponto no final) para que ele adicione o novo arquivo ou todos os novos arquivos caso utilize a opção com o ponto no final.

### git reset

Caso tenha commitado, mas ainda não fez o git push e deseja desfazer o commit, você pode utilizar o comando git reset. Caso tenha feito o push, verificar o comando git revert logo abaixo

### git revert

Se quiser reverter o último commit no servidor, utilize o comando **git revert HEAD~1**

Há diversos outros comandos para utilização do git, mas, creio que para a elaboração do projeto, esses são mais do que suficientes.

Qualquer dúvida quanto ao uso do git e/ou LaTeX, podem me acionar no e-mail 24201690@aluno.univesp.br
