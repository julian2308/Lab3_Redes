# Lab #3 - Subneteo, Configuración y simulación de LAN basada en IPv4.

## Presentado por: Julián(Alvarado + Durán + Pinilla).

### CONTEXTO DEL PROBLEMA.
La Universidad de los Julianes solicita el montaje y establecimiento de una red para el funcionamiento de la institución universitaria, con unos parámetros específios, como lo son la división de la red principal en distintas VLAN's para la segmentación de tráfico y control de acceso, estas son las siguientes: VLAN 35. Biblioteca; VLAN20. Estudiantes; VLAN40. Cuerpo docente: y VLAN55. Servicio técnico.

### MONTAJE.

#### Tabla de direccionamiento en base a la topología de red.
![image](https://user-images.githubusercontent.com/64561271/236713817-83a2477a-6888-4633-b49d-52c06f0a0dec.png)

#### Cableado estructurado
![image](https://user-images.githubusercontent.com/64561271/236714182-a845e1fd-0849-407a-a388-a9f3353b0b0a.png)
![image](https://user-images.githubusercontent.com/64561271/236714240-31508c51-d655-4171-bdbc-a7eacbd28038.png)




### METODOLOGÍA SEGUIDA.

* Red LAN: "Se conoce como red LAN (siglas del inglés: Local Área Network, que traduce Red de Área Local) a una red informática cuyo alcance se limita a un espacio físico reducido, como una casa, un departamento o a lo sumo un edificio" [1].
* VLAN: "Las VLAN o también conocidas como «Virtual LAN» nos permite crear redes lógicamente independientes dentro de la misma red física, haciendo uso de switches gestionables que soportan VLANs para segmentar adecuadamente la red" [2]. Básicamente permiten segmentar una misma red apartir de un Switch, y tener distintas subredes.
* IPv4: "(Internet Protocol versión 4) es el formato de dirección estándar que permite que todas las máquinas en Internet se comuniquen entre sí. IPv4 se escribe como una cadena de dígitos de 32 bits y una dirección IPv4 se compone de cuatro números entre 0 y 255, separados por puntos" [3].
* Spanning Tree: "Spanning Tree Protocol (STP) es un protocolo de capa dos publicado en la especificación IEEE 802.1.
El objetivo de STP es mantener una red libre de bucles. Un camino libre de bucles se consigue cuando un dispositivo es capaz de reconocer un bucle en la topología y bloquear uno o más puertos redundantes" [4].
* Subneteo: "Hace referencia a la subdivisión de una red en varias subredes. El subneteo permite a los administradores de red, por ejemplo, dividir una red empresarial en varias subredes sin hacerlo público en Internet. Esto se traduce en que el router que establece la conexión entre la red e Internet se especifica como dirección única, aunque puede que haya varios hosts ocultos. Así, el número de hosts que están a disposición del administrador aumenta considerablemente" [5].

### RESPUESTAS.

#### 4. Topología.
![image](https://user-images.githubusercontent.com/64561271/236714304-37d601de-2ba9-4122-928f-c5442c8770d7.png)


#### 4. show ip interface brief.

![image](https://user-images.githubusercontent.com/64561271/236714157-6e2d0677-59ca-4100-b3b8-d9c0f4076a75.png)

#### 5. 
![image](https://user-images.githubusercontent.com/64561271/236714388-ce6c4c30-78a2-4a93-8db1-af8a36991aaf.png)
![image](https://user-images.githubusercontent.com/64561271/236714398-4d2428ec-16f7-469e-acda-d75282499af4.png)

#### 7. show vlan 
![image](https://user-images.githubusercontent.com/64561271/236714699-9619a449-88c1-4f73-afb0-7be96d922827.png)

#### 8. interface fa0/0.x.  encapsulation dot1q xx
![image](https://user-images.githubusercontent.com/64561271/236714728-738ab1e6-db81-48f8-94a5-20711cc15a4e.png)

#### 9.
![image](https://user-images.githubusercontent.com/64561271/236714850-29d6fbe0-8025-4ee6-a130-16166c5f8d51.png) 
##### pc a su default gateway
![image](https://user-images.githubusercontent.com/64561271/236714973-1630c64e-8ce2-4105-a51c-9f9045bb304b.png) 
##### pc 0 al pc4 (misma vlan)
![image](https://user-images.githubusercontent.com/64561271/236714980-c1f47257-ed3c-4f22-8360-64c39f8d2878.png) 
##### pc0 a pc 7 (diferente vlan)



#### 10.
![image](https://user-images.githubusercontent.com/64561271/236714864-4309cd21-a443-4fd8-a17d-276740f11d23.png)
![image](https://user-images.githubusercontent.com/64561271/236714871-1a849a1c-d029-4a9a-b4fe-4c60dc8a89de.png)


### RETOS.
En primera instancia, se nos facilitó la repartición de roles en el equipo y pudimos empezar con anterioridad a plantear nuestra solución en base a nuestros requerimientos. Sin embargo, para nuestra segunda reunión enfrentamos problemas en nuestro montaje ya que en un principio los computadores no se lograban comunicar con otros, ya sea pertenecientes a la misma o diferentes Vlans. Acudimos a hacer un repaso capa por capa hasta encontrar el error, permitiendonos ir paso a paso y verificando que el montaje estuviese bine planteado. En primera instancia, algunos puertos de los switches no se econtraban cableados correctamente. Por otro lado, el modo de la Vlan 99, que su función era de truncamiento, estaba mal configurada, causando que la conexion de los computadores no fuese posible. 

### CONCLUSIONES Y RECOMENDACIONES.
Fue de muchísima ayuda tener una repartición y seguimiento de las tareas, facilitó mucho el trabajo en general, y nos permitió realizar un buen trabajo. Nos quedó pendiente aún intentar implementar el sistema de versionamiento con Git, ya que como los archivos que genera Packet Tracer no son archivos de texto plano, no se puede hacer uso de Git de una forma fácil, pero tampoco buscamos muchas más opciones de hacerlo.


### REFERENCIAS
* [1] Fragmento tomado de: "https://concepto.de/red-lan/#ixzz7xxuZ6gL7"
* [2] Fragmento tomado de: "https://www.redeszone.net/tutoriales/redes-cable/vlan-tipos-configuracion/"
* [3] Fragmento tomado de: "https://www.avg.com/es/signal/ipv4-vs-ipv6#:~:text=IPv4%20(Internet%20Protocol%20versi%C3%B3n%204,y%20255%2C%20separados%20por%20puntos."
* [4] Fragmento tomado de: "https://aprenderedes.com/2019/11/protocolo-de-arbol-de-extensionstp/"
* [5] Fragmento tomado de: "https://www.ionos.es/digitalguide/servidores/know-how/subnetting-como-funcionan-las-subredes/"
* Curso de Skills For All Networking Essentials. Módulo 17 y 18. "https://skillsforall.com/launch?id=104c1536-83d6-47db-b7a1-6007327b3134"
