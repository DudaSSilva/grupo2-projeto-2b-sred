## 4. Roteiro SSH

Agora que nossas VMs estão configuradas e os cabos estão conectados, vamos fazer o acesso remoto ssh entre as VMs, ou seja, conectar-se a um usuário de um pc a partir da VM de outro.

### 4.1. Atribuindo nomes aos servidores hostname

Antes de criar novos usuários, vamos alterar os nomes de hostname do usuário administrador (seguindo as definições denomes determinada na tabela da etapa 1). Logo, em cada VM executamos um comando no formato seguinte: 

```sudo hostnamectl set-hostname <hostname>```

### 4.1.1.  VM's  PC1

<p><center> Figura 1: Exemplo alteração de hostname PC1</center></p>   
   <img src="figures/hostNamePC1.jpg" alt=""
    title="Figura 1: hostname1" width="400" height="auto"/>

* VM1 PC1

```sudo hostnamectl set-hostname srv-vm1-pc1```

* VM2 PC1

```sudo hostnamectl set-hostname srv-vm2-pc1```
   
### 4.1.2.  VM's  PC2

<p><center> Figura 2: Exemplo alteração de hostname PC2</center></p>   
   <img src="figures/hostNamePC2.jpg" alt=""
    title="Figura 2: hostname2" width="400" height="auto"/>

* VM1 PC2
 
```sudo hostnamectl set-hostname srv-vm1-pc2```

* VM2 PC2

```sudo hostnamectl set-hostname srv-vm2-pc2```

### 4.1.3.  VM's  PC3

<p><center> Figura 3: Exemplo alteração de hostname PC3</center></p>   
   <img src="figures/hostNamePC3.jpg" alt=""
    title="Figura 3: hostname3" width="400" height="auto"/>

* VM1 PC3

```sudo hostnamectl set-hostname srv-vm1-pc3```

* VM2 PC3

```sudo hostnamectl set-hostname srv-vm2-pc3```

### 4.1.4.  VM's  PC4

<p><center> Figura 4: Exemplo alteração de hostname PC4</center></p>   
   <img src="figures/hostNamePC4.jpg" alt=""
    title="Figura 4: hostname4" width="400" height="auto"/>

* VM1 PC4

```sudo hostnamectl set-hostname srv-vm1-pc4```

* VM2 PC4

```sudo hostnamectl set-hostname srv-vm1-pc4```


### 4.2. Criando usuários

Em cada VM crie um usuário com o comando ``adduser``

<p><center> Figura 5: Configuração das NICs</center></p>   
   <img src="figures/adduser.jpg" alt=""
    title="Figura 5: Login-Admin" width="400" height="auto"/>

### 4.3. Acessando uma VM remotamente

* Exemplo: $ ssh ``<user>``@``<ipServidorRemoto>``

### 4.4. Fazendo o login 


* de: srv-vm2-pc1
   * para: srv-vm2-pc3

```shell
ssh camile@192.168.13.23
```

* de: srv-vm1-pc3
   * para: srv-vm2-pc4

```shell
ssh eduardasoares@192.168.13.24
```

* de: srv-vm1-pc3
   * para: srv-vm2-pc4
    
## 5. Roteiro Host-Only (SSH pelo terminal)

* Abrir opção ``Host Network Manager`` dentro da aba ``Arquivo`` do Virtualbox ou ``ctrl + H``
* Criar novo adaptador de rede no botão ``Criar``
* Click na botão ``Propriedades`` --> ``Servidor DHCP`` --> click ``[]Habilitar Servidor``
* Entre em uma VM e digite ``ifconfig -a`` (necessita do ``sudo apt install net-tools`` antes de ser usado)
* Verifique se na saída do comando há o nome do adaptador de rede que foi criado
* Desligue a VM com ``sudo poweroff``
* Click no botão ``configurações`` --> ``Rede``
* Habilite um novo adaptador de rede clickando em ``Adaptador <n>`` --> ``[] Habilitar placa de rede``

* Iniciar VM
* Digite ``ifconfig -a``
* Verifique se na saída do comando há o nome do adaptador de rede que foi criado
* Execute ``cd /etc/netplan/``
* ``sudo nano <nome_do_arquivo>.yaml``
   * Adicione no arquivo:
      ```
      <nome_adaptador_de_rede>:
         dhcp4: true
      ```
* Execute ``sudo netplan apply``
* Verifique no ``ifconfig -a`` se as mudanças deram certo
* Abrir terminal do pc (sem ser da vm)
* ``ssh <user>@<ip>``


<p><center> Figura 6: Adaptador novo ativado</center></p>   
   <img src="figures/adaptador.jpg" alt=""
    title="Figura 6: adaptador" width="400" height="auto"/>

## 6. Testes de ssh

<p><center> Figura 7:  VM2-PC2 para srv-vm1-pc1</center></p>   
   <img src="figures/ssh1.jpg" alt=""
    title="Figura 7: ssh1" width="600" height="auto"/>

<p><center> Figura 8: VM2-PC1 para 192.168.13.18 (VM1-PC2)</center></p>   
   <img src="figures/ssh2.jpg" alt=""
    title="Figura 8: ssh2" width="600" height="auto"/>
    
<p><center> Figura 9: VM2-PC2 para srv-vm2-pc4</center></p>   
   <img src="figures/ssh3.jpg" alt=""
    title="Figura 9: ssh3" width="600" height="auto"/>
    
<p><center> Figura 10: VM2-PC1 para VM1-PC4</center></p>   
   <img src="figures/ssh4.jpg" alt=""
    title="Figura 10: ssh4" width="600" height="auto"/>
