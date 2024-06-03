# Recovering a Privileged Account: Privilege Escalation Threat?

## Objetivo
La posibilidad de promocionar una cuenta con permisos mínimos es un tipo de ataque conocido como "Escalada de Privilegios Vertical". El objetivo de este proyecto es la de usar una cuenta con privilegios mínimos dentro y fuera de un dominio corporativo y comprobar si es posible promorcionarla para que obtenga permisos de administrador. 

## Habilidades empleadas
- Análisis de Vulnerabilidades
- Escalado de Privilegios
- Administración de Sistemas
- Investigación y Mitigación
- Documentación y Reporte

## Desarrollo Paso a Paso

### Ordenador fuera del dominio corporativo
Para usar como muestra de control, empezamos usando un ordenador que está fuera del dominio. Con este ordenador realizaremos todo el proceso de promoción de la cuenta de usuario para poder hacer la comparación con otro ordenador que sí está dentro del dominio y tiene un usuario con permisos de usuario.

Supongamos que en nuestro ordenador teníamos previamente 2 cuentas: una de administrador, que llamaremos “Admin”, la cual hemos borrado por despiste, y una de usuario llamada “User”.
Si queremos evitar el tener que formatear el ordenador y reinstalar el SO, lo que vamos a buscar es elevar la cuenta “User” de usuario a Administrador. Para ello, debemos hacer lo siguiente: 

1.	Una vez nos logueamos como User, Inicio -> Configuración -> Actualización y Seguridad -> Recuperación. Dentro de esta ventana, nos vamos a la opción Inicio Avanzado y clickamos el botón Reiniciar Ahora.
![image](https://github.com/JoseManuelMdlV/Recovering-a-Privileged-Account-Privilege-Escalation-Threat/assets/83475119/7795aa7c-ddff-4c29-b0c5-d525f8402333)

2.	En el menú que nos saldrá una vez reiniciemos el ordenador, le damos a Solucionar Problemas -> Opciones Avanzadas -> Configuración de Inicio y le damos al botón “Reiniciar”.
 ![image](https://github.com/JoseManuelMdlV/Recovering-a-Privileged-Account-Privilege-Escalation-Threat/assets/83475119/e01af29d-e8cb-4925-b5b3-129a754aac10)

3.	Entramos en el “Modo Seguro” presionando la tecla F4 y nos logueamos como User de forma normal.

4.	una vez logueados como User, hacemos click derecho en el logo de Windows de nuestra barra de herramientas y seleccionamos “Administrador de Tareas”.
![image](https://github.com/JoseManuelMdlV/Recovering-a-Privileged-Account-Privilege-Escalation-Threat/assets/83475119/a532415e-3483-4038-be50-cf41dc87e8cd)

5.	En el administrador vamos a la pestaña Usuarios y, en el usuario que aparece hacemos click derecho y Administrar cuenta de Usuario
![image](https://github.com/JoseManuelMdlV/Recovering-a-Privileged-Account-Privilege-Escalation-Threat/assets/83475119/ffd60a5e-9adc-49d5-bc6d-12ea811b3808)

6.	En la ventana que se nos abre, clickamos en “Cambiar Tipo de Cuenta”. Nos saldrá una ventana pidiendo una contraseña de “Administrador” para poder acceder. Dicha contraseña no es realmente necesaria y basta con darle a “Sí”.

7.	Una vez dentro, bastará con cambiar el tipo de cuenta a “Administrador” como se muestra en la imagen de abajo. Guardamos cambios y reiniciamos el ordenador.

![image](https://github.com/JoseManuelMdlV/Recovering-a-Privileged-Account-Privilege-Escalation-Threat/assets/83475119/9087c11d-59ba-49e1-ba7a-f750581a725d)

