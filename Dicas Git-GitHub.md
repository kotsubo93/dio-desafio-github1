# #Conteúdo sobre Git-Github

## Git - Sistema distribuido

#### Objetos:

Blob: Contém o tipo, tamanho, \0, conteúdo e o seu Sha1.

Tree: Pode ter outras trees, armazena blobs, o nome do arquivo e seu Sha1.

Commit: Objeto que junta todos os outros, pode ter outros commits, trees, autor, mensagem, timestamp (carimbo de data e hora) e também tem seu Sha1.

Sha1: Criptografia do arquivo, uma alteração no menor nivel (blob) altera o Sha1 de todos seus objetos de hieraquia maior. Isso torna o git tão confiavel, qualquer alteração em menor nivel pode ser identificado através da mudança no Sha1.

Commit >>> Tree >>> Blob

#### Estado do arquivo:

Tracked Unmodified: Já está reconhecido pelo git e está sem modificações.

Modified: Arquivo foi modificado.

Staged: Arquivo está em "espera", para entrar em ação.



Quando criamos um arquivo e não usamos o comendo Git add ele ainda está untracked, ao usar este comando ele passa a estar tracked e fica no estado de Staged, trabalhamos no arquivo e usamos commit que tira um snapshoot (prova) e o arquivo passa para o estado unmodified que é provado pelo commit feito, ao editar esse arquivo ele muda para modified e volta para staged novamente até fazermos um novo commit e salvar sua nova versão em um snapshoot para que ele retorne para unmodified.



#### Comandos:

Git init: Inicializa um repositório

Git commit -m "mensagem" - Cria um commit (snapshoot) com uma mensagem explicando o que foi feito.

Echo > nome do arquivo.formato - Cria um arquivo.

Git config -- global user.name nome - "Seta" o nome do usuario no Git (Usar mesmo nome do GitHub)

Git config -- global user.email email - "Seta" o email do usuario no Git (Usar mesmo email do GitHub)

Git config -- global -- unset user.name ou user.email - Apaga ou reseta o nome do usuario ou email no Git.

**Git remote add origin link https do repositorio GitHub - Estamos linkando o repositorio do GitHub com o Git. Copiamos o link https do repositorio criado no GitHub, abrimos o Git bash na pasta do nosso projeto e usamos esse comando.

**Git remote - v - Vai listar os repositorios remotos (confere se o comando acima /\ deu certo).

**Git push origin main - Manda "Push" o repositório do Git para o GitHub.

**Git clone link https do repositorio GitHub - Clona o repositorio do GitHub para seu Git local.




