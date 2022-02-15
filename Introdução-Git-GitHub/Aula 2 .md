BootCamp - Sportheca - Aula 2 - Git e GitHub - Fundamentos

- SHA1
- Objetos Fundamentais
- Sistema  distribuido
- Segurança

**SHA1**

​	É um algoritmo de encriptação. Ele vai pegar um arquivo e embaralhar de uma forma especifica.
​	A encriptação gera um conjuto de characteres indentificador de 40 digitos.

​	Todo arquivo possui uma chave SHA1, e qualquer alteração que seja realizada por menor que seja gera um nova chave. É uma forma inteligente e eficente do GIT para garantir e identificar  que os arquivos sofreram alterações.

Para verificar o SHA1 de um arquivo

Digite openssl sha1 + nome do arquivo+formato(.txt,jpg...)

**Objetos**

Blobs
Trees
Commits

**Blobs " arquivos "**

Contém metadados
Contem: O tipo do objeto, o tamanho do arquivo, \0 e o conteúdo do aquivo.

**Tree " pastas "**

​	Armazenas as Blobs, então é uma crescente a Blob sendo o bloco básico da composição. A tree armazenando e apontando para tipos de blobs diferentes. 

​	As trees  também contem metadados. Ela tem \0 ela aponta para um blob, que por sua vez tem um SHA1. As Trees também guardam o nome do arquivo.

​	As árvores são reponsáveis por montar toda estrutura de onde está os arquivos, de onde estão localizados esses arquivos. Podem apontar tanto para blobs quanto para outras árvores. 

**Commit**

​	Ele é um objeto que vai juntar tudo. Vai da sentido para alteração que esta sendo realizada. Aponta para uma árvore, aponta para um parente, ou seja, aponta para o último commit realizado antes dele. Aponta para um autor e aponta para uma mensagem também. 

​	Timestamp - é um carimbo de tempo, esse objeto leva a data e hora de quando foi criado.  Também possuem uma SHA1

**Sistema Distribuido**

​	Um sistema distribuído é uma coleção de dispositivos autônomos conectados por uma rede de comunicação que é percebida pelos usuários como um único dispositivo provendo serviços ou resolvendo algum problema. Dessa forma contribui para que as plataformas diferentes de hardware possam manter uma comunicação eficiente.

**Chave SSH**

É uma forma de estabelecer uma conexão segura e encripitada entre duas máquinas. 

**Cadastrando uma chave SSH:**

No site do GitHub:

1 - Settings
2 - SSH and GPG keys
3 - New SSH key

No GitBash

Digite: ssh-keygen -t ed25519 - C (seu email github)

**Para verificar as chaves na maquina:**

Procure a pasta .ssh onde foi salva as chaves

Digite Ls para listar os conteúdos da pasta
Para verificar o conteúdo de uma chave digite cat mais o nome da chave: Ex; id_ed25519.pub

*A chave pública que deve ser adicionada a sua conta GitHub.*

**Para ativar a chave**

No CLI 

Digite eval $(ssh-agent -s)

Irá retornar o agent e o número de processo

Ex: agent pid 1382 (numero de processo)

Após isso digite 

ssh-add id_25519 

Digite sua senha

Token de acesso pessoal

É gerado um token de acesso, diferente da SSH com o token você precisa informar a senha toda vez que for realizar uma operação

**Para gerar o token:**

Settings 
Developer settings
Click em New Token
Em nota escreve o nome do Token
Expiration coloque um prazo para esset token expirar
Selecione a opção Repo: Se for mexer nos diretórios padrão do Git
Click Generate Token
Copie e Salve o token pois não é possível ve-lo novamente.

**Baixando o respositório com o token**

Code
Https
Copia o link
No termial digita Git Clone e cola URL
Cole o token quando solicitado na janela