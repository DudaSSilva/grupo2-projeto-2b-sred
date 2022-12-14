# Criação de tabela de definições de endereços IPs da Rede e Nomes de Hosts

Nesta primeira etapa, vamos, primeiramente, criar uma tabela na qual irá conter as definições dos IPs de cada uma das 8 VMs a serem criadas neste projeto. 

A sub-rede norteadora desta etapa é a sub-rede 192.168.13.[16-31]. A partir dessa informação, é possível determinar a nossa rede, nosso broadcast e o nosso gateway. São eles:

* Sub-rede: 192.168.13.[16-31]
* Rede: 198.168.13.16
* Broadcast: 198.168.13.31
* gateway: 192.168.13.17

Sabendo-se disso, e sabendo que as VMs do PC1, PC2, PC3 e PC4 foram designadas para os alunos Matheus, Ygor, Camile e Eduarda, respectivamente, a nossa tabela pôde ser constituída (Tabela 1).

```
Tabela 1: Definições de endereços IPs da Rede e Nomes de Hosts

------------------------------------------------------------------------------------------------------------
|  DESCRICAO  |  IP                |   hostname        |              FQDN              |      aliase      |
------------------------------------------------------------------------------------------------------------
| VM1-PC1     | 192.168.13.17      |   srv-vm1-pc1     | vm1-pc1.grupo2-913.ifalara.net |       math1      |
| VM2-PC1     | 192.168.13.21      |   srv-vm2-pc1     | vm2-pc1.grupo2-913.ifalara.net |       math2      |
| VM1-PC2     | 192.168.13.18      |   srv-vm1-pc2     | vm1-pc2.grupo2-913.ifalara.net |       ygor1      |
| VM2-PC2     | 192.168.13.22      |   srv-vm2-pc2     | vm2-pc2.grupo2-913.ifalara.net |       ygor2      |
| VM1-PC3     | 192.168.13.19      |   srv-vm1-pc3     | vm1-pc3.grupo2-913.ifalara.net |       cami1      |
| VM2-PC3     | 192.168.13.23      |   srv-vm2-pc3     | vm2-pc3.grupo2-913.ifalara.net |       cami2      |
| VM1-PC4     | 192.168.13.20      |   srv-vm1-pc4     | vm1-pc4.grupo2-913.ifalara.net |       duda1      |
| VM2-PC4     | 192.168.13.24      |   srv-vm2-pc4     | vm2-pc4.grupo2-913.ifalara.net |       duda2      |
------------------------------------------------------------------------------------------------------------
```

# Configurações de hardware

As configurações de cada VM foram determinadas como as padrões definidas pelo próprio VirtualBox. Ficando, portanto:

```
* Memória principal: 512 MB
* Memória de vídeo:  16 MB
* CPU:               1
* Controladora:      VMSVGA
* Porta SATA 0-
* ubuntu-server-mini-disk001.vdi
* Software da máquina: Linux e VirtualBox (para a criação das VM's).
* Software VM: Net-tools, open ssh server.
* Rede Fisica: Foram utilizados 4 computadores e 8 VM's, sendo duas em cada computador. Além disso, utilizou-se um switch e 4 cabos para conectar os PC's
```
