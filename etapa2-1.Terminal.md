## 1.   No terminal

Para iniciar a etapa 2, é necessário abrir o terminal de sua máquina física. É nele onde serão realizados a maioria dos passos necessários para concluir esta primeira etapa. 

Observação: os passos dessa parte 1 serão os mesmos para os quatro PCs, independente da VM a ser criada. 

### 1.1. Login na rede

Primeiro, é preciso entrar na rede para, assim, conseguirmos efetuar os comandos posteriores. Para isso, vamos executar no terminal o comando: 

``su redes``

Esse comando serve para alterar o usuário que, inicialmente, está configurado como aluno@LABREDES-VM. Após o comando anterior e a inserção da senha (admin@Lab92) para o usuário redes, o usuário foi alterado para redes@LABREDES-VM conforme a imagem 1.  

(Por questões de segurança, a senha fica invisível. Então, digite-a corretamente. Caso haja falha na autenticação, basta tentar novamente.)



### 1.2. Criar pasta labredes na raiz / e subpastas

Posteriormente criaremos as pastas/os diretórios onde ficarão armazenados nossos arquivos (imagem 2). Mas, antes de criar essas pastas, é importante verificar se elas já existem (tal como ocorre na imagem 3), no caso de não ser a primeira vez configurando uma VM com esses passos.

Para efetuar esta criação dos diretórios, primeiro entra-se no diretório raiz usando:


```shell
cd /
```

Depois, usamos o comando ``mkdir`` prosseguido pelo ``nome do diretório``, mas no caso de ser um usuário comum do sistema, utiliza-se o comando ``sudo`` antes. 


```shell
sudo mkdir /labredes
```

Agora, entramos no diretório labredes para criar as subpastas ``images`` e ``original``:


```shell
cd /labredes
sudo mkdir images
cd images
sudo mkdir original
cd original
```

Agora, entramos novamente no diretório labredes com ``cd /labredes`` para criar os diretórios referentes aos usuários da máquina em questão, faremos isso digitando os comandos: 


```shell
sudo mkdir VM
cd /labredes/VM
sudo mkdir 913 
cd /labredes/VM/913
sudo mkdir <student>
```

Como são 4 PCS com 4 usuários/estudantes distintos, o passo anterior fica da seguinte maneira:


Para terminal do PC1: ```shell sudo mkdir matheus ```

Para terminal do PC2: ```shell sudo mkdir ygor ```

Para terminal do PC3: ```shell sudo mkdir camile ```

Para terminal do PC4: ```shell sudo mkdir eduarda ```
