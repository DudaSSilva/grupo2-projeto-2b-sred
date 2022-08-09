## 3. Criação de uma rede ponto a ponto física entre quatro PCs e uma LAN lógica com 8 VMs

## Configurações das VMs para o computador 1:

### Na VM1-PC1

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.17/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

### Na VM2-PC1

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.21/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

## Configurações das VMs para o computador 2:

### Na VM1-PC2

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.18/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

### Na VM2-PC2

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.22/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

## Configurações das VMs para o computador 3:

### Na VM1-PC3

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.19/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

### Na VM2-PC3

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.23/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

## Configurações das VMs para o computador 4:

### Na VM1-PC4

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.20/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

### Na VM2-PC4

```
network:
    ethernets:
        enp0s3:                              
            addresses: [192.168.13.24/25]    
            gateway4: 192.168.13.17          
            dhcp4: false                     
    version: 2
```

### Testando a conectividade entre as VMs

   * Ping da VM1-PC1 para VM2-PC2

```shell
ping 192.168.13.22      # ctrl + c para finalizar o comando
```
   * Ping da VM1-PC1 para VM2-PC3

```shell
ping 192.168.13.23      
```

 * Ping da VM1-PC1 para VM2-PC4

```shell
ping 192.168.13.24     
```

* Ping das demais VMS para VM1-PC1

```shell
ping 192.168.13.17    
```

* Ping das demais VMS para VM2-PC1

```shell
ping 192.168.13.21    
```

* Fazer ping de todos para todos.
