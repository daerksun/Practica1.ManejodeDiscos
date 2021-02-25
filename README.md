# Practica1.ManejodeDiscois

1. **Identificar y describir las diferencias entre hda, sda y vda, además explicar qué significa la letra y el número al final de los identificadores (no requiere captura de pantalla).**





2. **¿Cómo montar y desmontar un usb en el sistema por terminal?**

sudo mount [dispositivo] [destino]
sudo unmount [direccion]

![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/1.png "Im1")

3. **Enlistar la información de los dispositivos de bloque conectados aunque no estén montados en terminal.**

lsblk
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/2.png "Im2")

4. **Mostrar la tabla de particiones del disco donde está instalado el sistema operativo en terminal.**

sudo fdisk -l
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/5.png "Im5")

5. **Conectar una memoria usb (“usb”) y mostrar su tabla de particiones en terminal (hacer respaldo antes porque se va a borrar toda la información dentro del usb en pasos posteriores).**

sudo fdisk -l /dev/sdc
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/7.png "Im7")

6. **Borrar todas las particiones del “usb” en terminal.**

unmount
fdiks /dev/sdc
d - delete
w - write
fdisk -l /dev/sdc
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/8.png "Im8")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/9.png "Im9")


7.** Crear en el “usb” tres particiones físicas y una extendida en terminal.**

fdisk /dev/sdc
n - nueva particion
p - tipo de particion (primaria)
Primer Sector
Ultimo sector
se repite 3 veces
n
e - particion extendida
Primer Sector
Ultimo Sector
w
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/11.png "Im11")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/12.png "Im12")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/13.png "Im13")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/14.png "Im14")

8. **Crear una partición dentro de la partición extendida del “usb” en terminal.**

fdisk /dev/sdc
l - particion lógica w

![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/15.png "Im15")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/16.png "Im16")

9. **En la interfaz gráfica de la aplicación disks, borrar las particiones para que sólo exista una
partición que abarque toda la “usb”.**
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/18.png "Im18")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/19.png "Im19")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/20.png "Im20")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/21.png "Im21")
![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/22.png "Im22")

10. **Copiar un archivo .iso de distribución live de linux a la usb por medio del comando "dd".**

![alt text](https://github.com/daerksun/Practica1.ManejodeDiscos/blob/main/Imagenes/24.png "Im24")
