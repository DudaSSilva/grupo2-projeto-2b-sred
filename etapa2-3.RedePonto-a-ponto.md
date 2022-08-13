## 3. Montando uma rede ponto a ponto física entre quatro PCs e uma LAN lógica com 8 VMs

### 3.1. conecção de cabos via Switch

<p><center> Figura 1: Conecção via switch</center></p>   
   <img src="figures/switch.jpg" alt=""
    title="Figura 1: switch" width="400" height="auto"/>

### 3.2. Modo Bridge

### 3.3. Testando a conectividade entre as VMs

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

* Fazer ping de todos para todos e verificar o funcionamento dos mesmos.

### 3.4. Resultados de pings

* De VM1-PC1 para VM1-PC4

<p><center> Figura 2: Ping VM1-PC1 para VM1-PC4</center></p>   
   <img src="figures/1114.jpg" alt=""
    title="Figura 2: ping1" width="400" height="auto"/>
    
* De VM1-PC1 para VM2-PC1

<p><center> Figura 3: Ping VM2-PC1 para VM1-PC1</center></p>   
   <img src="figures/1121.jpg" alt=""
    title="Figura 3: ping2" width="400" height="auto"/>
    
* De VM2-PC1 para VM1-PC1

<p><center> Figura 3: Ping VM2-PC1 para VM1-PC1</center></p>   
   <img src="figures/2111.jpg" alt=""
    title="Figura 3: ping2" width="400" height="auto"/>
    
* De VM2-PC1 para VM1-PC2

<p><center> Figura 4: Ping VM2-PC1 para VM1-PC2</center></p>   
   <img src="figures/2112.jpg" alt=""
    title="Figura 4: ping3" width="400" height="auto"/>
    
* De VM2-PC1 para VM2-PC2

<p><center> Figura 4: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/2122.jpg" alt=""
    title="Figura 4: ping3" width="400" height="auto"/>
    
* De VM2-PC1 para VM1-PC3

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/2113.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>
    
* De VM2-PC1 para VM2-PC3

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/2123.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>
    
* De VM2-PC1 para VM1-PC4

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/2114.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>

* De VM1-PC3 para VM2-PC3

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/1323.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>   

* De VM2-PC1 para VM2-PC4

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/2124.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>
    
* De VM1-PC4 para VM2-PC4

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/1424.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>
    
* De VM1-PC2 para usuário duda1 (VM1-PC4) e para usuário duda2 (VM2-PC4)

<p><center> Figura 5: Ping VM2-PC1 para VM2-PC2</center></p>   
   <img src="figures/12-duda1-2.jpg" alt=""
    title="Figura 5: ping4" width="400" height="auto"/>
