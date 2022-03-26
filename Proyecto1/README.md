# Proyecto 1
---------------
## Integrantes
|Carne | Nombre | Perfil |
|-----|-----|-----|
|201901510| Pablo Daniel Rivas Marroquin| https://github.com/PabloRivas201901510 |
|201903850 |Adrian Samuel Molina Cabrera| https://github.com/AdrianMolina2000 |
|201807160 | Saul Absalon Barillas Argueta| https://github.com/SaulB10 |
|201902934 |German Jose Paz Cordon| https://github.com/GermanJosePazCordon |


## TOPOLOGIA 1
![](img/TP1.png "TP1")

### ESW1

#### VLANS 
![](img/ESW1_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW1_VTP.png "VTP")


#### PUERTOS
```
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
```
![](img/ESW1_TR.png "Puertos")


### ESW2

#### VLANS 
![](img/ESW2_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW2_VTP.png "VTP")


#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 10
exit
exit

conf t
int f1/1
switchport mode access
switchport access vlan 30
exit
exit

conf t
int f1/2
switchport mode access
switchport access vlan 10
exit
exit

conf t
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

sh vlan-sw
sh int tr
```
![](img/ESW2_TR.png "Puertos")



### ESW3

#### VLANS 
![](img/ESW3_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW3_VTP.png "VTP")


#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 20
exit
exit

conf t
int f1/1
switchport mode access
switchport access vlan 40
exit
exit

conf t
int f1/2
switchport mode access
switchport access vlan 30
exit
exit

conf t
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

sh vlan-sw
sh int tr
```
![](img/ESW3_TR.png "Puertos")


## TOPOLOGIA 2
![](img/TP2.png "TP2")

### ESW4

#### VLANS 
```
conf t
vlan 10
name RRHH
vlan 20
name Informatica
vlan 30
name Contabilidad
vlan 40
name Ventas
```
![](img/ESW4_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW4_VTP.png "VTP")

#### PUERTOS
```
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW4_TR.png "Puertos")

#### STP
```
spanning-tree vlan 10 root primary
spanning-tree vlan 20 root primary
spanning-tree vlan 30 root primary
spanning-tree vlan 40 root primary
```
![](img/ESW4_SP.png "STP")

### ESW5
#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode client
vtp version 2
```
![](img/ESW5_VTP.png "VTP")

#### PUERTOS
```
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW5_TR.png "Puertos")

#### VLANS
![](img/ESW5_VLANS.png "Vlans")

### ESW6
#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode client
vtp version 2
```
![](img/ESW6_VTP.png "VTP")

#### PUERTOS
```
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW6_TR.png "Puertos")

#### VLANS
![](img/ESW6_VLANS.png "Vlans")

### ESW7
#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode client
vtp version 2
```
![](img/ESW7_VTP.png "VTP")

#### PUERTOS
```
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005

int f1/3
switchport mode acces
switchport acces vlan 20
```
![](img/ESW7_TR.png "Puertos")

#### VLANS
![](img/ESW7_VLANS.png "Vlans")

## TOPOLOGIA 3
![](img/tp3.png "tp3")

### ESW8

#### VLANS 
![](img/ESW8_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW8_VTP.png "VTP")

#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 40
exit

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW8_TR.png "Puertos")

### ESW9

#### VLANS 
![](img/ESW9_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW9_VTP.png "VTP")

#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 30
exit

int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit

int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW9_TR.png "Puertos")

### ESW10

#### VLANS 
![](img/ESW10_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW10_VTP.png "VTP")

#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 10
exit

int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit

int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
![](img/ESW10_TR.png "Puertos")

### ESW11

#### VLANS 
![](img/ESW11_VLANS.png "VLANS")

#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp mode server
vtp version 2
```
![](img/ESW11_VTP.png "VTP")

#### PUERTOS
```
conf t
int f1/0
switchport mode access
switchport access vlan 20
exit

int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit

int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
```
#### TOPOLOGIA1 :
#### CONFIGUARACION DEL VTP CLIENT
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp version 2
vtp mode client
exit
sh vtp st
write
```
#### CONEXION ENTRE ROUTERS EWS2 Y EW3
```
conf t
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
sh int tr
write
```
#### CONEXION ENTRE ROUTERS - EWS1
```
conf t
int f1/0
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

conf t
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit

sh int tr

write
```

#### CONEXION ENTRE ROUTER -> VPC EWS2
```
conf t
int f1/0
switchport mode access
switchport access vlan 10
exit
exit

conf t
int f1/1
switchport mode access
switchport access vlan 30
exit
exit

conf t
int f1/2
switchport mode access
switchport access vlan 10
exit
exit
sh vlan-sw
write
```


#### CONEXION ENTRE ROUTER -> VPC EWS3
```
conf t
int f1/0
switchport mode access
switchport access vlan 20
exit
exit

conf t
int f1/1
switchport mode access
switchport access vlan 40
exit
exit

conf t
int f1/2
switchport mode access
switchport access vlan 30
exit
exit
```
#### VPCS
```
RRHH_1
ip 192.168.21.10/24 255.255.255.0 192.168.21.1
save

CONTA_1
ip 192.168.23.10/24 255.255.255.0 192.168.23.1
save

RRHH_2
ip 192.168.21.20/24 255.255.255.0 192.168.21.1
save

CONTA_2
ip 192.168.23.20/24 255.255.255.0 192.168.23.1
save

VENTAS_1
ip 192.168.24.10/24 255.255.255.0 192.168.24.1
save

INFORMATICA
ip 192.168.22.10/24 255.255.255.0 192.168.22.1
save
```
### TOPOLOGIA 3:
  #### SHOW
```
sh vlan-sw
sh interface trunk
sh spanning-tree brief
sh spanning-tree root
```
   #### VPC
```
ip 192.168.2X.30/24 192.168.2X.1
save
```
#### VTP
```
conf t
vtp domain GRUPO2
vtp password grupo2
vtp version 2
vtp mode client
exit 
sh vtp status
write
```
#### ESW9
```
conf t
int f1/0
switchport mode access
switchport access vlan 30
exit
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
write
```
#### ESW8

```
conf t
int f1/0
switchport mode access
switchport access vlan 40
exit
int f1/1
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
write
```
#### ESW10
```
conf t
int f1/0
switchport mode access
switchport access vlan 10
exit
int f1/2
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
write
```

#### ESW11

```
conf t
int f1/0
switchport mode access
switchport access vlan 20
exit
int f1/3
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
int f1/4
switchport mode trunk
switchport trunk allowed vlan 1,10,20,30,40,1002-1005
exit
exit
write
```
