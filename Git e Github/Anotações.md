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

 

## **PRIMEIROS COMANDOS COM O GIT**

Objetivos:

​     \- Iniciar o Git;

​     \- Iniciar o versionamento;

​     \- Criar um commit.

### **Comandos mais importantes**

​    **git help (comando)** - Mostra informações sobre o comando informado;

​	**git init** – Inicia o diretório na pasta;

​    **git add** */nomedoarquivo - Dá início ao versionamento;

​    **git commit** -m “mensagem” – Faz commit do repositório de forma local;

​    **git status** – Mostra os status dos arquivos, para mostrar qualquer tipo de alteração;

​	**git config --global --unset** user.email/user.nickname - Remove as configurações tanto de email, como de nome (que devem ser, por recomendação, iguais ao do github, não obrigatoriamente);

​	**git config** (**user.email** "email@email..." ou **user.nickname"name_login") - Configura o email e/ou o nome, que por recomendação devem ser iguais aos cadastrados no github;

​    **git remote add origin (url disponibilizado pelo repositório no github)** – Aponta para o repositório remoto que receberá o commit;

​    **git remote -v** – Lista todas as origens cadastras;

​    **git push origin master** – Manda/Empurra o commit local para o remoto;

​	**git pull origin master** - Puxa os commits/alterações feitas no repositório remoto;

​    **git clone (url disponibilizado pelo repositório no github)** - Clona o repositório armazenado no github. É necessário o URL do repositório para isso;