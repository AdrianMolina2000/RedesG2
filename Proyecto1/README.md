# Practica 1
---------------
## Integrantes
|Carne | Nombre | Perfil |
|-----|-----|-----|
|201901510| Pablo Daniel Rivas Marroquin| https://github.com/PabloRivas201901510 |
|201903850 |Adrian Samuel Molina Cabrera| https://github.com/AdrianMolina2000 |
|201807160 | Saul Absalon Barillas Argueta| https://github.com/SaulB10 |
|201902934 |German Jose Paz Cordon| https://github.com/GermanJosePazCordon |


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

### ESW5
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

