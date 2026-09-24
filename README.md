# Utilizando GIT - GITHUB

### CONFIGURAÇÃO INICIAL DO GIT


> NOTA: Estes comandos devem ser feitos no GITBASH dentro da pasta que deseja usar para salvar o seu projeto

Para setar a configuração do GIT de forma global no seu repositório:

`git config – global user.email “EMAIL_QUE_USA_NO_GIT@EMAIL.COM”`

`git config –global user.name "NICK_USADO_NO_GIT"`

 
> Observação: esses comandos não retornam mensagem de sucesso

---

### VER CONFIGURAÇÕES DO GIT

Para ver as configurações do git:
`git config –list`

---

### ATALHOS DE USO
 Para limpar o terminal basta clicar o atalho **Ctrl + L**

Ao começar a digitar um comando e der **TAB**, ele vai completar 

Dentro da sua pasta onde vai iniciar o trabalho, abra o git bash clicando com o botão direito 

dentro da pasta, para eliminar a necessidade de navegar nas pastas pelos comandos no 

terminal.

---

### CLONAGEM DE REPOSITÓRIO

#### Processo usando o HTTPS:

Vá no Github e copie o código **htpps** em **CODE** do repositório

Inicialize o git na pasta que deseja abrir o projeto e use o comando:

`git clone` **COLE O CAMINHO HTTPS QUE COPIO DO GITHUB**

> Evite atalhos como Ctrl + C e Ctrl + V, eles naõ tem o mesmo comportamento no GitBash. Utilize o botão direito do mouse

Para saber se deu certo use o comando  `ls`no termimal

---
#### Processo usando o ssh:

Vá no Github e copie o código **SSH** em **CODE** do repositório

Inicialize o git na pasta que deseja abrir o projeto e use o comando:

`git clone` **COLE O CAMINHO SSH QUE COPIO DO GITHUB**

Se der certo, ele vai perguntar: continue connecting (yes/no/)? Digite: yes

Para saber se deu certo use o `ls`

---

### PUXAR A VERSÃO SINCRONIZADA MAIS RECENTE DO CÓDIGO SALVO NO GITHUB



Quando quiser puxar a última versão empurrada para o github:

`git pull origin master`

> Atualmente, a o GitHub adota o nome MAIN em vez de master para a branch principal. Caso seu repositório utilize o padrão novo, o comando correto será: 

`git pull origin main`

---

### NAVEGAR NAS PASTAS 

Para navegar nas pastas é usado o comando `cd` ex:
`cd /C/Users/efrem/workspace` 

>Para saber o caminho completo da pasta em que esta, usa o comando pwd ex:

`pwd`

Para retroceder pastas usa `..` após o nome da pasta atual ex: 

`cd /C/Users/efrem/..`

Para criar pasta :

`mkdir NOME_DA_PASTA`

Para mover o arquivo de uma pasta para a outra :

`mv NOME_DO_ARQUIVO.extenscao ./NOME_da_PASTA_QUE_DESTINO `



### VISUALIZAR O CONTEÚDO DA PASTA

Para visualizar o conteúdo da pasta digital:

`ls`

Para visualizar conteúdos ocultos da pasta digitar :

´ls -a`

Para ver o caminho completo da pasta que está no momento:

`pwd`

Para criar pasta :

`mkdir NOME_DA_PASTA`

---

### FAZENDO O COMMIT DOS ARQUIVOS



Para fazer o commit dos arquivos, usar a sequência de comandos:

`git add * `

Para adicionar somente um arquivo ao commit

`git add NOME_DO_ARQUIVO NOME_DE_MAIS_UM_ARQUIVO` 

>Observação: Pode adiconar mais de um arquivo no comendo 

`git commit -m “Neste campo, anote que tipo de commit é"` 

ex: ("commit inicial")("Alteração da tela de login")”



>Para saber se precisa fazer algum commit use o comando:

`git status`

---



### CRIAR CHAVE SSH 

> O trecho abaixo não está atualizado (DESCONSIDERE)

Para criar a chave de encriptação ssh para o github:

ssh-keygen -t ed25519 -C email_usado_no_github@email

Se der certo ele vai apontar onde ela vai ser salva, aperte Enter e insira uma senha.

Para visualizar a chave é necessário entrar na pasta (.ssh) ex:

cd /C/Users/efrem/.ssh

Usar o ls para listar os arquivos e depois usar o comando CAT para ver a chave ex:

cat id_ed25519.pub

Lembrete ( para criar a chave no github é usada a chave com a extensão .pub)



### PARA INICIALIZAR O AGENTE QUE VAI GERENCIAR AS CHAVES CRIADAS

Esse processo deve ser feito para que as chaves funcione

Primeiro inicialize o agente :

eval $(ssh-agent -s)  "se o agente for inicializado, a mensagem: Agent pid SEQUÊNCIA DE 

NÚMEROS será exibida"

Segundo, entregue a chave para ele:

ssh-add id_ed25519  "Deve ser entregue a chave privada, a que não tem a extensão .pub" " Esse 

comando só pode ser executado assim se estiver dentro da pasta ".ssh"

Neste passo é digitado a mesma senha que uso na criação das chaves.















### EMPURRAR O CÓDIGO PARA O GITHUB



Como apontar o repositório da área de desenvolvimento local para o remoto:
git remote add origin LINK_DO_REPOSITÓRIO_GITHUB

obs: origin pode ser substituído por qualquer nome, mas por convenção é usado o origin
Para ver a lista de repositórios cadastrados:
git remote -v

Para empurrar o repositório para o GitHub
git push origin master






