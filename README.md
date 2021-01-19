# Git e Github

Guia prático para iniciantes.
visto no link abaixo:
https://www.youtube.com/watch?v=2alg7MQ6_sI

## Extensão para modificar a visualização do terminal (tutorial)
https://blog.rocketseat.com.br/terminal-com-oh-my-zsh-spaceship-dracula-e-mais/

### Instalação

https://git-scm.com/download

# Scenes (casos de uso) - Parte I

- Com o Git é possível criar pontos durante o desenvolvimento de projeto e esses pontos podem ser revisitados.
- Com o Git é possível verificar mudanças feitas no projeto.

para iniciar o projeto usamos o comando: 
**git init**

para criar um ponto de recuperação do projeto usamos o comando:
**git add** nome_dos_arquivos_e_pastas
**git commit** -m "a mensagem que desejamos para lembrar desse ponto"

com isso foi executado uma das funcionalidades do Git
- [X] criado um pontos do projeto que podem ser revisitados (recuperados, retornados, etc.).

comando para ver esse ponto:
**git log**

comando para saber o estado do monitoramento do git no projeto:
**git status**

após salvar o segundo commit é possivel utilizar uma segunda funcionalidade do Git com o comando:
**git log**

e segunda funcionalidade é verificar as modificações no projeto!

o comando git show + código do commit mostra as modificações feitas no código do projeto
**git show** numero_do_commit

o comando abaixo mostra a ultima modificação realizada no arquivo:
**git show**

# Scenes (casos de uso) - Parte II

- Começar uma nova funcionalidade sem estragar o estado do projeto atual
- Adicionar novas funcionalidades ao projeto em produção
- Excluir o ramo (branch) da nova funcionalidade após aplicar a nova funcionalidade ao projeto.

o comando abaixo cria uma ramificação do projeto:
**git branch** nome_do_ramo

comando para visualizar os ramos (branch):
**git branch**

comando para mudar de ramo (branch):
**git checkout** nome_da_branch

- aqui atendemos ao caso de uso sobre criar nova(s) funcionalidade(s) sem estragar o projeto atual porque podemos criar ou modificar arquivos sem prejudicar os arquivos que podem estar sendo usados.

para juntar dois ramos (branch) usamos o comando:
**git merge** nome_do_ramo

- aqui atendemos ao caso de uso relacionado a adicionar novas funcionalidades porque o merge uni a funcionalidade que foi criado em outro ramo, sem alterar o projeto original, ao ramo principal.

Para excluir o ramo (branch) que foi criado o recurso, porque já que usamos o merge quer dizer que ele foi integrado no projeto e perdeu a utilidade, mas podemos manter ele se quiser seguindo as modificações:
usamos o comando:
**git branch -D** nome_do_ramo

podemos ter certeza disso com o comando 
**git branch**

- aqui atendemos ao caso de uso relacionado a eliminar o ramo (branch) que foi criado para o desenvolvimento da funcionalidade.

# Revisando comandos

- `git init` // inicia um monitoramento de arquivos no projeto
- `git add` // alem do git monitorar podemos adicionar um arquivo ou diretório (pasta) a um ponto de restaração assim o git salva um estado do documento (linha do tempo) que pode ser recuperada futuramente
- `git commit` // adiciona a descrição e confirma o estado do documento que foi adicionado com o `git add`
- `git log` // visualiza o todos os estados do documento e informa o um código que pode ser usado para ver com mais detalhes essas modificações, tambem pode ser usado para restaurar o documento para aquele estado do documento.
- `git status` // informa se os arquivos ou diretórios monitorados foram alterados e se essa alterações não foram salvas como um estado (linha do tempo) ou se o documento atual não sofreu nenhuma modificação.
- `git show` // apresenta um determinada mudança no estado do documento, com o código que pode ser obtido no `git log` ele mostra o estado do código especifico sem o código ele mostra a ultima mudança.

# Scenes (caso de uso) - parte III

- Colocar o projeto na nuvem (com o github)

é necessario uma conta no github
https://github.com/

na página do github na pagina de sua bio (overview) clique em mais na aba proxima a sua foto no canto superior direito!

clique em new repository

ou clique em new na aba (repositories)

agora executamos esses comandos na linha de comando para adicionar ao repositório remoto:
**git remote add origin** https://github.com/nomedeusuario/nomedorepositorioremoto.git

comando para visualizar os repositórios remotos 
**git remote -v**

comando para enviar os arquivos do repositório local (arquivos monitorados pelo git) para o repositório remoto (github), na primeira vez que fazemos isso precisamos usar o argumento (flag, etc.) -u origin master ele cria um ramo (branch) no repositório remoto. atualmento por conta das definições da microsoft o master virou o main então se você copiar o comando da pagina do github será criado um ramo chamado main 
**git push** -u origin master (pode ser main tambem.)
**git push** -u origin main

- nesse momento cumprimos o caso de uso de colocar nosso projeto na nuvem

comando para adicionar todas as modificações para monitorar via git:
**git add .**
 

Desenvolvido por &copy;Rocketseat explicado por Mayk Brito, esse material foi retirado de uma video aula *https://www.youtube.com/watch?v=2alg7MQ6_sI* produzida pelo Mayk Brito e &copy;Rocketseat a cópia e reprodução é apenas por interesse de aprendizado recomendo demais que façam essa aula bem interessante para praticar, algumas modificações são de minha autoria para fixar o aprendizado! 