BootCamp - Sportheca - Aula 3 - Git e GitHub - Primeiros Comandos

- Git Init
- Git Add
- Git commit
- Git pull
- Git Push

**Git Init**

Cria-se um repositório

Tracked ou Untracked

Ls -a - Mostra pastas ocultas

Untracked

**Git Add**

> git add nomeArquivo
> git add * (adiciona todas as alterações  do repositório local para Staging Area)
> git add .

Quando usado o comando GitAdd seja ele para adicionar a alteração em um arquivo ou a alteração realizada em todos os arquivos e movendo para Staging Area, ou seja, a área que irá entrar em ação, a área local.

São os arquivos que o Git ainda não tem ciência deles.

**Tracked** 

São os arquivos que o Git já tem ciência deles.

**Unmodified** 

É um arquivo que ainda não foi modificado

**Modified** 

É o arquivo Unmodified que sofreu alguma modificação.

**Staged**

É onde se encontra os arquivos que estão se preparando para fazer parte de outro tipo de grupamento. 

Quando o commit é acionado ele tira os arquivos do Staged e agora passam a ser commit. E o commit retorna todos esses arquivos para Unmodified, para aguardando novas modificações.

**Clico de vida dos arquivos no Git**

Untracked

      -
Tracked

Unmodified

*Adiciona o arquivo

Modified

Edita o arquivo

Starged

"stage" o arquivo

commit

**Ambiente de desenolvimento**

Representa tudo que está na máquina.

Working Directoy
Staging Area
Local Repository

Durante as alterações realizadas na maquina o sistema intercala-se entre o Working Directory e Staging Area, porém após a execução do comando commit ele é inserido no Local Repository o que permite que esse arquivo possa migrar para o servidor. 

Quando o comando commit é acionado os arquivos que estavam em Staging migram para o Unmodified (pronto para receber novas modificações).  Além disso ele permite que você popule o seu repositório local. Sem o commit não é possivel enviar arquivos para o repositório remoto.

**Servidor**

O Git é um sistema distribuido. Ele tem uma versão na sua máquina e no servidor. As alterações realizada na maquina ela não repercute imediatamente na versão que está no repositório remoto (remote repository) a não ser que seja executado um conjunto de códigos especificos onde você passa a alteração do seu repositório local para o repositório remoto.

**Enviando um arquivo para o GitHub**

Digite git remote add origin + link do diretório github

Digite  git push origin master 
Digite a senha 

  Obs: a palavra "origin" não faz parte do comando, é apenas um apelido para não digitar o HTTPS ou o link o tempo inteiro, é o apelido do link. Por convenção usa-se "Origin"

**Listando as lista de repositórios remotos cadastradas**

Digite  remote -v

**Conflitos**

**Conflitos de merge**

Quando o gitHub tenta juntar duas alterações e existem duas alterações na mesma linha. O github não irá fazer nenhuma alteração. Ele vai deixar que você abra aquele arquivo onde ocorreu edição na mesma linha realizado por pessoas diferentes. E você mesmo manualmente resolva aquele conflito, e depois empurra o código correto para o GitHub.

**Clonando um repositório** 

Vá no github e click em code
Copie o link
Vá ao terminal GuitBash
Digite " Git Clone + o Link "

**O que difere a clonagem de baixar manualmente?**

Quando clonado ele não vem apenas como uma pasta simples. e sim como um repositório. Significa que dentro deste repositório ele tem a pasta .git, que é a pasta que contém todo o versionamento de código e contém também para onde esse repositório está apontado ou seja  sua origem.

**Como verificar se o conteúdo na maquina é uma pasta baixada ou uma pasta clonada?**

Digite ls -a que mostrará os arquivos ocultos. Aparecento a pasta .git significa que trata-se de um clone. 

**Como verificar para qual repositório o respositório da máquina está apontado?**

Digite git remote -v e ele mostrará seu local de origem. 