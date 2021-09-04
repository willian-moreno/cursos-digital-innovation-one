## **SHA1** 

Secure Hash Algorithm ou Algoritmo de Hash Seguro, é uma função de dispersão criptográfica projetada pela Agência de Segurança Nacional dos Estados Unidos e é um Padrão Federal de Processamento de Informação dos Estados Unidos publicado pelo Instituto Nacional de Padrões e Tecnologia.

A encriptação cria um conjunto de caracteres identificador de 40 dígitos, e é essa a tecnologia utilizada pelo Git.

Ex. comando no terminal: echo “teste” | **openssl sha1**

O **openssl sha1** é o pipe responsável por fazer a encriptação do texto ou arquivo.

 

## **BLOBS, TREES e COMMITS**

Estes são os três objetos básicos do Git para versionamento.

* Um “blob” é usado para armazenar dados de arquivo - geralmente é um arquivo. O blob contém os metadados do Git, ou seja, o tipo de dado, o tamanho do objeto, etc.

* Uma “árvore” é basicamente como um diretório - faz referência a um monte de outras árvores e blobs (ou seja, arquivos e subdiretórios).

* Um objeto “commit” contém metadados para cada mudança introduzida no repositório, incluindo o autor , committer , commit-data e log-messages.

Encriptação usando Git - Comando:

Ex.: echo “teste” | **git hash-object –stdin**

A encriptação é diferente dessa maneira por causa do Blob.

Para fazer a encriptação usando o **openssl sha1**, e usando o blob, fazemos da seguinte forma:

​     echo **-e ‘blob 9/0**teste**’** | **openssl sha1**



## Gerando uma chave SSH

 https://docs.github.com/pt/github/authenticating-to-github/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

## **PRIMEIROS COMANDOS COM O GIT**

Objetivos:

​     \- Iniciar o Git;

​     \- Iniciar o versionamento;

​     \- Criar um commit.

### **Comandos mais importantes**

​    **git help (comando)**

​		O que faz: Mostra informações sobre o comando informado;

​	**git init**

​		O que faz: Inicia o diretório na pasta;

​    **git add * ** ou **git add diretório/arquivo**

​		O que faz: Dá início ao versionamento;

​		Observação: O comando git add * inicializa o versionamento para TODOS os arquivos alterados. Já o *git add diretório/arquivo*, onde ‘diretório/arquivo’ é o caminho do arquivo modificado, inicializa o versionamento para arquivos específicos.

​	**git rm diretório/arquivo**

​		O que faz: Remove o arquivo do versionamento;

​    **git commit -m “mensagem”**

​		O que faz: Faz commit do repositório de forma local;

​    **git status**

​		O que faz: Mostra os status dos arquivos, para mostrar qualquer tipo de alteração;

​	**git diff**

​		O que faz: O comando *git diff* é usado para listar os conflitos;

​	**git config --global --unset user.email** e **git config --global --unset user.name**  

​		O que faz: Remove as configurações tanto de email, como de nome (que devem ser, por recomendação, iguais ao do github, porém não obrigatoriamente);

​	**git config --global user.email "email@email"** e **git config --global user.name "name_login"**

​		O que faz: Configura o email e/ou o nome (Por recomendação devem ser iguais aos cadastrados no github);

​    **git remote add origin url_repositório** 

​		O que faz: Aponta para o repositório remoto que receberá o commit;

​		Exemplo: git remote add origin https://github.com/UsuarioGit/NomeRepositorio.git

​		Observação: *origin* é um nome que referência o link do repositório, podendo ser qualquer outro nome. Logo, é possível adicionar mais de um repositório mudando o nome de referência. Exemplo: git remote add desenv https://github.com/UsuarioGit/NomeRepositorio2.git.

​	**git remote set-url origin url_repositório** 

​		O que faz: Altera o repositório configurado;

​		Exemplo: git remote set-url origin https://github.com/UsuarioGit/OutroRepositorio.git

​    **git remote -v** 

​		O que faz: Lista os repositórios cadastrados localmente, dentro do repositório iniciado, cujo comando foi executado;

​    **git push -u origin master** 

​		O que faz: Manda/Empurra o commit local para o remoto;

​	**git fetch**

​		O que faz: Permite que um usuário obtenha todos os objetos do repositório remoto que atualmente não residem no diretório de trabalho local;

​	**git pull origin master** 

​		O que faz: Puxa os commits/alterações feitas no repositório remoto da branche master;

​    **git clone url_repositório** 

​		O que faz: Clona o repositório armazenado no github. É necessário o URL do repositório para isso;

​		Exemplo: git clone https://github.com/UsuarioGit/OutroRepositorio.git

​	**git checkout -b nome_branche** 

​		O que faz: Cria um novo branche, para que os arquivos sejam adicionados em outro local. Um exemplo é a criação de um branche para desenvolvimento (desenv), enquanto o master (que é um branche padrão) fica para produção, assegurando que o código commitado não quebre o projeto;

​		Exemplo: git checkout -b desenv

​	**git checkout nome_branche_existente** 

​		O que faz: Muda para uma branch existente, por exemplo, git checkout desenv, muda para a branch desenv;

