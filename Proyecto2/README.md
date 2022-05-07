# Proyecto 2
---------------
## Integrantes
|Carne | Nombre | Perfil |
|-----|-----|-----|
|201901510| Pablo Daniel Rivas Marroquin| https://github.com/PabloRivas201901510 |
|201903850 |Adrian Samuel Molina Cabrera| https://github.com/AdrianMolina2000 |
|201807160 | Saul Absalon Barillas Argueta| https://github.com/SaulB10 |
|201902934 |German Jose Paz Cordon| https://github.com/GermanJosePazCordon |


## Manual Tecnico
Este proyecto se realizo en gns3, el objetivo de este es la creacion de redes utilizando dispositivos intermedios.
Haciendo subnetting ya sea FLSM o VLSM.

### Topologia 1
![](img/TP1.png "TP1")

### Cloud1 topologia 1
![](img/tp1_c1.png "c1_tp1")
### Cloud2 topologia 1
![](img/tp1_c2.png "c2_tp1")
### Cloud3 topologia 1
![](img/tp1_c3.png "c3_tp1")
### Cloud4 topologia 1
![](img/tp1_c4.png "c4_tp1")

### -Routers
### R1 topologia 1
![](img/tp1_r1.png "r1_tp1")
### R2 topologia 1
![](img/tp1_r2.png "r2_tp1")
### R3 topologia 1
![](img/tp1_r3.png "r3_tp1")
### R4 topologia 1
![](img/tp1_r4.png "r4_tp1")

### Tabla resultante:
| Network | Mask | P.Asignable | U.Asignable | Broadcast | Host Totales | Cantidad de host |
|-----|-----|-----|-----|-----|-----|-----|
| 10.2.0.0/30 | 255.255.255.252 |10.2.0.1 | 10.2.0.2 | 10.2.0.3 | 2 | 2 | 
| 10.2.0.4/30 | 255.255.255.252 |10.2.0.5 | 10.2.0.6 | 10.2.0.7 | 2 | 2 |
| 10.2.0.8/30 | 255.255.255.252 |10.2.0.9 | 10.2.0.10 | 10.2.0.11 | 2 | 2 |
| 10.2.0.12/30 | 255.255.255.252 |10.2.0.13 | 10.2.0.14 | 10.2.0.15 | 2 | 2 |
| 10.2.0.16/30 | 255.255.255.252 |10.2.0.17 | 10.2.0.18 | 10.2.0.19 | 2 | 2 |
| 10.2.0.20/30 | 255.255.255.252 |10.2.0.21 | 10.2.0.22 | 10.2.0.23 | 2 | 2 |

### Topologia 2
![](img/tp2.png "TP2")

### Cloud3 topologia 2
![](img/tp2_c3.png "c3_tp2")
### Cloud4 topologia 2
![](img/tp2_c4.png "c4_tp2")

### VPCS topologia 2
### -Informatica
![](img/tp2_info.png "info_tp2")
### -Contabilidad
![](img/tp2_conta.png "info_tp2")
### -RRHH
![](img/tp2_rrhh.png "info_tp2")
### -Ventas
![](img/tp2_ventas.png "info_tp2")

### Router topologia 2
### R5
![](img/tp2_router.png "r5_tp2")

### ESW1
![](img/tp2_tr.png "esw1_tp2")
### VLANS topologia 2
![](img/tp2_vlan.png "vlan_tp2")
### Tabla resultante:
| Vlan | Salto | Network | Mask | P.Asignable | U.Asignable | Broadcast | Host Totales | Cantidad de host |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 10 | 62 | 192.168.24.0/26 | 255.255.255.192 | 192.168.24.1 | 192.168.24.62 | 192.168.24.63 | 62 | 1 | 
| 20 | 62 | 192.168.24.64/26 | 255.255.255.192 | 192.168.24.65 | 192.168.24.126 | 192.168.24.127 | 62 | 1 |
| 30 | 62 | 192.168.24.128/26 | 255.255.255.192 | 192.168.24.129 | 192.168.24.190 | 192.168.24.191 | 62 | 1 |
| 40 | 62 | 192.168.24.192/26 | 255.255.255.192 | 192.168.24.192 | 192.168.24.254 | 192.168.24.255 | 62 | 1 |


### Topologia 3
![](img/tp3.png "TP3")
### Cloud1 topologia 3
![](img/tp3_cloud1.png "c1_tp3")
### Cloud2 topologia 3
![](img/tp3_cloud2.png "c2_tp3")

### VPCS
### -Informatica
![](img/tp3_info1.png "info_tp3")
### -Contabilidad
![](img/tp3_conta1.png "info_tp3")
### -RRHH
![](img/tp3_rrhh1.png "info_tp3")
### -Ventas
![](img/tp3_ventas1.png "info_tp3")

### Router
![](img/tp3_router6.png "r6_tp3")
### ESW2
![](img/tp3_tr.png "esw2_tp3")
### VLANS
### Tabla resultante:
![](img/tp3_vlans.png "vlan_tp3")
### Tabla resultante:
| Vlan | Salto | Network | Mask | P.Asignable | U.Asignable | Broadcast | Host Totales | Cantidad de host |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| 10 | 62 | 192.168.25.0/26 | 255.255.255.192 | 192.168.25.1 | 192.168.25.62 | 192.168.25.63 | 62 | 1 | 
| 20 | 62 | 192.168.25.64/26 | 255.255.255.192 | 192.168.25.65 | 192.168.25.126 | 192.168.25.127 | 62 | 1 |
| 30 | 62 | 192.168.25.128/26 | 255.255.255.192 | 192.168.25.129 | 192.168.25.190 | 192.168.25.191 | 62 | 1 |
| 40 | 62 | 192.168.25.192/26 | 255.255.255.192 | 192.168.25.192 | 192.168.25.254 | 192.168.25.255 | 62 | 1 |
