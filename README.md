Tutorial para la instalación de Java 8, configuración de Java y ejecución de Certifica.jar en Mac.

## Índice
1. [Introducción: ¿Qué vamos a hacer?](#introducción-qué-vamos-a-hacer)
2. [¿Qué es Java y por qué es seguro instalarlo?](#qué-es-java-y-por-qué-es-seguro-instalarlo)
3. [Instalación de SDKMAN en Mac](#instalación-de-sdkman-en-mac)
4. [Instalación de Java 8.0.452-zulu](#instalación-de-java-80452-zulu)
5. [Verificación de la instalación](#verificación-de-la-instalación)
6. [Descarga del archivo Certifica.jar](#descarga-del-archivo-certificajar)
7. [Ejecución del archivo Certifica.jar](#ejecución-del-archivo-certificajar)
8. [Solución de problemas comunes](#solución-de-problemas-comunes)
9. [Información adicional: Instalación y cambio entre diferentes versiones de Java](#información-adicional-instalación-y-cambio-entre-diferentes-versiones-de-java)

## Introducción: ¿Qué vamos a hacer?

En este tutorial, te guiaré paso a paso para ejecutar el programa `Certifica.jar` en tu Mac. Este programa requiere una versión específica de Java para funcionar correctamente. No necesitas ser un experto en tecnología, simplemente sigue las instrucciones para poder ejecutar el programa.

## ¿Qué es Java y por qué es seguro instalarlo?

Java es uno de los lenguajes de programación más utilizados en el mundo, desarrollado originalmente por Sun Microsystems (ahora parte de Oracle Corporation). Muchas aplicaciones y servicios que usamos diariamente dependen de Java para funcionar, incluyendo:

- Aplicaciones gubernamentales y bancarias
- Programas de gestión empresarial
- Aplicaciones de declaración de impuestos
- Sistemas de facturación electrónica

*¿Por qué es seguro instalar Java?*

- Java es utilizado por millones de empresas y usuarios en todo el mundo
- Es un estándar en la industria tecnológica desde hace más de 25 años
- La versión que instalaremos (Zulu) es mantenida por Azul Systems, un proveedor oficialmente reconocido y de confianza

Puedes verificar la legitimidad de Java en el sitio oficial de Oracle: [https://www.java.com](https://www.java.com)

O la versión Zulu que utilizaremos en este tutorial, mantenida por Azul Systems: [https://www.azul.com/downloads/?package=jdk](https://www.azul.com/downloads/?package=jdk)

## Instalación de SDKMAN en Mac

Primero, necesitamos instalar una herramienta que nos ayudará a configurar correctamente tu Mac:

1. Abre la aplicación "Terminal" en tu Mac:
   
   - Puedes encontrarla en la carpeta "Aplicaciones" > "Utilidades" > "Terminal"
   - O puedes buscarla presionando `Cmd`+`Espacio` y escribiendo "Terminal"

3. Cuando se abra la Terminal, copia y pega este comando exactamente como está:
   ```bash
   curl -s "[https://get.sdkman.io](https://get.sdkman.io)" | bash
   ```
4. Presiona Enter y espera a que termine la instalación.

Lo que deberías ver:

Verás varias líneas de texto apareciendo en la Terminal. Al final, deberías ver un mensaje similar a:

>All done!

>Please open a new terminal, or run the following in the existing one:

>    source "$HOME/.sdkman/bin/sdkman-init.sh"

>Then start using SDKMAN!

4. Cuando termine, copia y pega este otro comando:
```bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```
5. Presiona Enter nuevamente.

Lo que deberías ver:

No verás mucho, tal vez un breve mensaje como:

>Initializing SDKMAN...

6. Para confirmar que SDKMAN se instaló correctamente, escribe:
```bash
sdk version
```
Lo que deberías ver:

Deberías ver un mensaje indicando la versión de SDKMAN, algo como:

>SDKMAN 5.18.2

## Instalación de Java 8.0.452-zulu

Ahora vamos a instalar la versión específica de Java que necesita Certifica.jar:

1. En la misma ventana de Terminal, copia y pega este comando:
```bash
sdk install java 8.0.452-zulu
```
2. Presiona Enter y espera a que termine la descarga e instalación.

Lo que deberías ver:

Verás cómo comienza la descarga:

>Downloading: java 8.0.452-zulu
>In progress...

La descarga puede tardar varios minutos dependiendo de tu conexión a Internet.

3. Si te pregunta si quieres establecer esta versión como predeterminada, escribe "Y" (sin comillas) y presiona Enter.

Lo que deberías ver:

Un mensaje similar a:

>Do you want java 8.0.452-zulu to be set as default? (Y/n): Y

>Setting java 8.0.452-zulu as default.

Al finalizar la instalación, verás un mensaje como:

>Done installing!

## Verificación de la instalación

Vamos a comprobar que todo se instaló correctamente:

1. En la misma ventana de Terminal, escribe:
```bash
java -version
```
2. Presiona Enter.

Lo que deberías ver:

Deberías ver un texto similar a este (los números exactos pueden variar):

>openjdk version "1.8.0_452"
>OpenJDK Runtime Environment (Zulu 8.84.0.13-CA-macosx) (build 1.8.0_452-b13)
>OpenJDK 64-Bit Server VM (Zulu 8.84.0.13-CA-macosx) (build 25.452-b13, mixed mode)

Lo importante es que muestre "1.8.0_452" que indica que es Java 8.

## Descarga del archivo Certifica.jar

Antes de ejecutar el programa, necesitamos asegurarnos de que tienes el archivo Certifica.jar correcto.

Abre tu navegador web preferido (Safari, Chrome, Firefox, etc.).
Dirígete a la siguiente dirección web:

https://portalsat.plataforma.sat.gob.mx/certifica/

En la página, busca la opción para descargar el instalador de "Certifica". Es importante que descargues la versión de 64 bits.

## Ejecución del archivo Certifica.jar

Ahora estás listo para ejecutar el programa Certifica.jar:

1. Primero, necesitas saber dónde está guardado el archivo Certifica.jar en tu Mac.

2. Supongamos que el archivo está en tu carpeta "Descargas". En la Terminal, escribe:
```bash
cd /Users/TuNombreDeUsuario/Descargas
```
Reemplaza "TuNombreDeUsuario" con tu nombre de usuario en Mac. Si no sabes cuál es, puedes escribir pwd en la Terminal y verás la ruta de tu directorio actual, que debería incluir tu nombre de usuario.

Ejemplo:

>cd /Users/maro/Descargas

3. Presiona Enter.

Lo que deberías ver:

La Terminal simplemente cambiará al directorio indicado. No verás ningún mensaje especial, pero la línea de comandos cambiará para mostrar que ahora estás en la carpeta "Descargas".

4. Para verificar que el archivo Certifica.jar está en este directorio, escribe:
```bash
ls
```
Lo que deberías ver:
   
Una lista de todos los archivos en tu carpeta de Descargas. Deberías ver "Certifica.jar" (o como se llame exactamente tu archivo) en la lista.

5. Ahora, ejecuta el programa con este comando:
```bash
java -jar Certifica.jar
```
6. Presiona Enter.

Lo que deberías ver:

<img width="1440" alt="certifica" src="https://github.com/user-attachments/assets/e3e54da8-7a36-463c-9f8c-92840158c300" />

Si todo funciona correctamente, debería abrirse la interfaz gráfica del programa Certifica.jar. Es posible que no veas nada nuevo en la Terminal, ya que el programa se ejecutará en una ventana separada.

Si el programa no tiene interfaz gráfica, verás su salida directamente en la Terminal.

## Solución de problemas comunes

El programa no se abre o muestra mensajes de error

Si después de seguir todos los pasos anteriores el programa no se abre correctamente:

1. Asegúrate de que estás en el directorio correcto donde se encuentra el archivo Certifica.jar. Puedes verificar los archivos del directorio actual con:
```bash
ls
```
Lo que deberías ver:

>El nombre del archivo "Certifica.jar" debe aparecer en la lista.

2. Verifica que el nombre del archivo es exactamente "Certifica.jar" (respetando mayúsculas y minúsculas). Si es diferente, usa el nombre correcto en el comando.

3. Si ves un mensaje de error, intenta ejecutar el programa con este comando alternativo:
```bash
java -Xmx512m -jar Certifica.jar
```
Lo que deberías ver:

Igual que antes, debería abrirse la interfaz gráfica del programa si todo funciona correctamente.

La Terminal no reconoce el comando "sdk"

Si al escribir un comando que comienza con "sdk" aparece "command not found", ejecuta:
```bash
source "$HOME/.sdkman/bin/sdkman-init.sh"
```
Lo que deberías ver:

Posiblemente nada o un breve mensaje de inicialización.

Mensajes de seguridad en Mac

Si Mac muestra un mensaje de seguridad que impide abrir el programa:

1. Verás una ventana emergente con un mensaje como "Certifica.jar no puede abrirse porque el desarrollador no puede ser verificado."

2. Ve a "Preferencias del Sistema" > "Seguridad y privacidad"

3. En la pestaña "General", deberías ver un mensaje sobre el programa bloqueado y un botón que dice "Abrir de todos modos" o "Permitir". Haz clic en ese botón.

## Información adicional: Instalación y cambio entre diferentes versiones de Java

Esta sección es sólo para usuarios avanzados que necesiten gestionar varias versiones de Java en su sistema.

Instalación de otras versiones de Java

Si necesitas instalar otras versiones de Java:

1. Para ver todas las versiones disponibles:
```bash
sdk list java
```
Lo que deberías ver:

Una larga lista de versiones de Java disponibles para instalar. Las versiones ya instaladas estarán marcadas.

2. Para instalar una versión específica:
```bash
sdk install java [identificador-de-versión]
```
Reemplaza "[identificador-de-versión]" con el código de la versión que deseas instalar.

Cambio entre versiones de Java

Si tienes varias versiones instaladas y necesitas cambiar entre ellas:

1. Para cambiar temporalmente (sólo para la sesión actual):
```bash
sdk use java [identificador-de-versión]
```
2. Para establecer una versión como predeterminada:
```bash
sdk default java [identificador-de-versión]
```
3. Para ver qué versión está activa actualmente:
```bash
sdk current java
```
Lo que deberías ver:

Una lista de versiones de Java instaladas, con la versión activa marcada con ">" al inicio de la línea.

Con estas instrucciones deberías poder ejecutar correctamente el programa Certifica.jar en tu Mac. Si sigues teniendo problemas, es posible que necesites contactar con el soporte técnico del proveedor del programa.
