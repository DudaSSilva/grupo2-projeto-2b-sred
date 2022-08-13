## 4. Roteiro SSH

Agora que nossas VMs estão configuradas e os cabos estão conectados, vamos fazer o acesso remoto ssh entre as VMs, ou seja, conectar-se a um usuário de um pc a partir da VM de outro.

### 4.1. Criando usuários

Em cada VM crie um usuário com o comando ``adduser``

<p><center> Figura 2: Configuração das NICs</center></p>   
   <img src="figures/adduser.jpg" alt=""
    title="Figura 2: Login-Admin" width="400" height="auto"/>

### 4.2. Acessando uma VM remotamente

* Exemplo: $ ssh ``<user>``@``<ipServidorRemoto>``

### 4.3. Fazendo o login 


* de: srv-vm2-pc1
   * para: srv-vm2-pc3

```shell
ssh camile@192.168.13.23
```

<p><center> Figura 3: Configuração das NICs</center></p>   
   <img src="figures/adduser.jpg" alt=""
    title="Figura 3: Login-Admin" width="400" height="auto"/>

* de: srv-vm1-pc3
   * para: srv-vm2-pc4

```shell
ssh eduardasoares@192.168.13.24
```

* de: srv-vm1-pc3
   * para: srv-vm2-pc4

## 5. Roteiro Host-Only (SSH pelo terminal)

* abrir opção ´´´Host Network Manager´´´ dentro da aba ´´´Arquivo´´´ do Virtualbox, 

