Casa M1(10.0.0.0):
AdministracionM = 10.0.0.1
RecursosM = 10.1.0.1
GerenciasM = 10.2.0.1
DesarolloM = 10.3.0.1
Invitados = 10.4.0.1

Casa M2(11.0.0.0):
A.Cliente = 11.0.0.1
D.Compras = 11.1.0.1
D.Publicidad = 11.2.0.1
D.Sistemas = 11.3.0.1
D.Logistica = 11.4.0.1
InvitadosM2 = 11.5.0.1

Localidades:
Ventas = x.0.0.1
Administracion = x.1.0.1
Gerencias = x.2.0.1
LogExp = x.3.0.1
Invitados = x.4.0.1

Santa Fe (12.x.x.x) SF
Rosario (13.x.x.x) ROS
La Plata(14.x.x.x) LP
Comodoro Rivadavia(15.x.x.x) CR
Cordoba(16.x.x.x) COR
Salta(17.x.x.x)SAL
Tucuman(18.x.x.x)TUC

Servidores:
DNS ServerCM1 = 10.0.0.2
ServerMail = 10.0.0.3
ServerCM2 = 11.0.0.2
ServerSistemas = 11.3.0.2 
ServerSF = 12.1.0.2
ServerROS = 13.1.0.2
ServerLP = 14.1.0.2
ServerCR = 15.1.0.2
ServerCOR = 16.1.0.2
ServerSAL = 17.1.0.2
ServerTUC = 18.1.0.2



COPIAR Y PEGAR EN CADA ROUTER (MAS ABAJO CONFIGURACION GENERAL ACL)

SANTA FE:
access-list 101 permit tcp 12.0.0.1 host 12.1.0.2 eq 443
access-list 101 permit tcp 12.1.0.1 host 12.1.0.2 eq 443
access-list 101 permit tcp 12.2.0.1 host 12.1.0.2 eq 443
access-list 101 permit tcp 12.3.0.1 host 12.1.0.2 eq 443
access-list 101 permit tcp 12.4.0.1 host 12.1.0.2 eq 443
access-list 101 permit tcp 12.2.0.1 host any eq 80
access-list 101 permit tcp 12.2.0.1 host any eq 443
access-list 101 permit tcp 12.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

ROSARIO:
access-list 101 permit tcp 13.0.0.1 host 13.1.0.2 eq 443
access-list 101 permit tcp 13.1.0.1 host 13.1.0.2 eq 443
access-list 101 permit tcp 13.2.0.1 host 13.1.0.2 eq 443
access-list 101 permit tcp 13.3.0.1 host 13.1.0.2 eq 443
access-list 101 permit tcp 13.4.0.1 host 13.1.0.2 eq 443
access-list 101 permit tcp 13.2.0.1 host any eq 80
access-list 101 permit tcp 13.2.0.1 host any eq 443
access-list 101 permit tcp 13.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

LA PLATA: 
access-list 101 permit tcp 14.0.0.1 host 14.1.0.2 eq 443
access-list 101 permit tcp 14.1.0.1 host 14.1.0.2 eq 443
access-list 101 permit tcp 14.2.0.1 host 14.1.0.2 eq 443
access-list 101 permit tcp 14.3.0.1 host 14.1.0.2 eq 443
access-list 101 permit tcp 14.4.0.1 host 14.1.0.2 eq 443
access-list 101 permit tcp 14.2.0.1 host any eq 80
access-list 101 permit tcp 14.2.0.1 host any eq 443
access-list 101 permit tcp 14.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

COMODORO RIVADAVIA: 
access-list 101 permit tcp 15.0.0.1 host 15.1.0.2 eq 443
access-list 101 permit tcp 15.1.0.1 host 15.1.0.2 eq 443
access-list 101 permit tcp 15.2.0.1 host 15.1.0.2 eq 443
access-list 101 permit tcp 15.3.0.1 host 15.1.0.2 eq 443
access-list 101 permit tcp 15.4.0.1 host 15.1.0.2 eq 443
access-list 101 permit tcp 15.2.0.1 host any eq 80
access-list 101 permit tcp 15.2.0.1 host any eq 443
access-list 101 permit tcp 15.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

CORDOBA:
access-list 101 permit tcp 16.0.0.1 host 16.1.0.2 eq 443
access-list 101 permit tcp 16.1.0.1 host 16.1.0.2 eq 443
access-list 101 permit tcp 16.2.0.1 host 16.1.0.2 eq 443
access-list 101 permit tcp 16.3.0.1 host 16.1.0.2 eq 443
access-list 101 permit tcp 16.4.0.1 host 16.1.0.2 eq 443
access-list 101 permit tcp 16.2.0.1 host any eq 80
access-list 101 permit tcp 16.2.0.1 host any eq 443
access-list 101 permit tcp 16.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

SALTA: 
access-list 101 permit tcp 17.0.0.1 host 17.1.0.2 eq 443
access-list 101 permit tcp 17.1.0.1 host 17.1.0.2 eq 443
access-list 101 permit tcp 17.2.0.1 host 17.1.0.2 eq 443
access-list 101 permit tcp 17.3.0.1 host 17.1.0.2 eq 443
access-list 101 permit tcp 17.4.0.1 host 17.1.0.2 eq 443
access-list 101 permit tcp 17.2.0.1 host any eq 80
access-list 101 permit tcp 17.2.0.1 host any eq 443
access-list 101 permit tcp 17.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53

TUCUMAN:
access-list 101 permit tcp 18.0.0.1 host 18.1.0.2 eq 443
access-list 101 permit tcp 18.1.0.1 host 18.1.0.2 eq 443
access-list 101 permit tcp 18.2.0.1 host 18.1.0.2 eq 443
access-list 101 permit tcp 18.3.0.1 host 18.1.0.2 eq 443
access-list 101 permit tcp 18.4.0.1 host 18.1.0.2 eq 443
access-list 101 permit tcp 18.2.0.1 host any eq 80
access-list 101 permit tcp 18.2.0.1 host any eq 443
access-list 101 permit tcp 18.2.0.1 host any eq 53
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
access-list 101 permit tcp any host 10.0.0.2 eq 53



CONFIGURACION GENERAL ACL (NO COPIAR, SOLO PARA DESARROLLO)
SEGUIR ORDEN DE ACL COMO ESTA:

Cada uno de los departamentos, estén en cualquier Locación, tienen acceso https al sistema de su sector.
access-list 101 permit tcp x.0.0.1 host x.1.0.2 eq 443
access-list 101 permit tcp x.1.0.1 host x.1.0.2 eq 443
access-list 101 permit tcp x.2.0.1 host x.1.0.2 eq 443
access-list 101 permit tcp x.3.0.1 host x.1.0.2 eq 443
access-list 101 permit tcp x.4.0.1 host x.1.0.2 eq 443

Las terminales de Gerencia pueden acceder a cualquiera de los sistemas de los distintos departamentos.
(para añadir mas sistemas copiar linea y cambiar puerto por servicio requerido ej:(eq 200))
access-list 101 permit tcp x.2.0.1 host any eq 80
access-list 101 permit tcp x.2.0.1 host any eq 443
access-list 101 permit tcp x.2.0.1 host any eq 53

La organización cuenta con un correo electrónico que puede ser accedido de cualquier terminal
(activar mail en server dns o hacer otro server para mail)
access-list 101 permit tcp any host 10.0.0.2 eq 110
access-list 101 permit tcp any host 10.0.0.2 eq 587

Todas las terminales de la sucursales y casa Matriz puede navegar http y https por internet.
(activar en server dns el http y https):
access-list 101 permit tcp any host 10.0.0.2 eq 80
access-list 101 permit tcp any host 10.0.0.2 eq 443
(servicio adicional dns)
access-list 101 permit tcp any host 10.0.0.2 eq 53

