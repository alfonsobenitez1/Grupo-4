*****************************************************************
*                                                               *
*   GUÍA DE CONFIGURACIÓN DE ENTORNO DE DESARROLLO WEB (LAMP)   *
*                                                               *
*****************************************************************

A continuación, se detallan los pasos para verificar y configurar un entorno de desarrollo web completo.

==================================
1. Sistema Operativo Actualizado
==================================

Objetivo: Asegurar que el sistema operativo tiene los últimos parches de seguridad y rendimiento.

---> Windows:
     1. Ve a Inicio > Configuración.
     2. Selecciona "Actualización y seguridad".
     3. Haz clic en "Windows Update" y luego en "Buscar actualizaciones".

---> macOS:
     1. Ve al Menú Apple > Ajustes del Sistema.
     2. Haz clic en "General" y luego en "Actualización de Software".
     3. Instala las actualizaciones disponibles.

---> Linux (Debian/Ubuntu):
     1. Abre una terminal.
     2. Ejecuta: sudo apt update
     3. Ejecuta: sudo apt upgrade


=================================
2. Apache Instalado y Funcionando
=================================

Objetivo: Verificar que el servidor web está activo.

---> Verificación:
     - Abre tu navegador web y visita la dirección: http://localhost
     - Deberías ver una página de bienvenida de Apache o de tu paquete (XAMPP, WAMP, etc.).


==============================
3. PHP Instalado Correctamente
==============================

Objetivo: Comprobar que PHP está procesando los scripts correctamente.

---> Verificación:
     1. Crea un archivo llamado "info.php" en la carpeta raíz de tu servidor web (ej. C:\xampp\htdocs\).
     2. Escribe dentro del archivo: <?php phpinfo(); ?>
     3. Guarda el archivo.
     4. Abre en tu navegador: http://localhost/info.php
     5. Deberías ver una página con toda la información de la configuración de PHP.


=========================
4. MySQL/MariaDB Operativo
=========================

Objetivo: Asegurar que el servicio de la base de datos está en ejecución.

---> Verificación:
     - Usando un panel de control como XAMPP, verifica que el servicio de MySQL/MariaDB esté "Iniciado" (en verde).
     - Desde una terminal, puedes intentar conectar con: mysql -u root -p


=======================
5. phpMyAdmin Accesible
=======================

Objetivo: Poder gestionar las bases de datos desde una interfaz web.

---> Verificación:
     - Abre tu navegador y visita: http://localhost/phpmyadmin
     - Deberías ver la pantalla de inicio de sesión de phpMyAdmin.


=================================
6. Base de Datos "proyecto_web" Creada
=================================

Objetivo: Tener una base de datos lista para tu proyecto.

---> Instrucciones:
     1. Inicia sesión en phpMyAdmin.
     2. En el menú de la izquierda, haz clic en "Nueva".
     3. En "Nombre de la base de datos", escribe: proyecto_web
     4. Como cotejamiento, elige "utf8_spanish2_ci".
     5. Haz clic en el botón "Crear".


=========================
7. VS Code Instalado
=========================

Objetivo: Tener un editor de código moderno y configurado.

---> Instrucciones:
     1. Descarga e instala VS Code desde su web oficial.
     2. Abre VS Code.
     3. Ve a la pestaña de Extensiones (icono de bloques).
     4. Busca e instala extensiones útiles como:
        - PHP Intelephense
        - Prettier - Code formatter
        - Live Server
        - GitLens


==================
8. Git Instalado
==================

Objetivo: Tener el sistema de control de versiones listo para usar.

---> Verificación:
     1. Abre una terminal o Símbolo del sistema.
     2. Escribe el comando: git --version
     3. Debería aparecer la versión de Git instalada (ej. "git version 2.39.2.windows.1").


==============================
9. Repositorio Git Inicializado
==============================

Objetivo: Empezar a controlar las versiones de los archivos de tu proyecto.

---> Instrucciones:
     1. Crea la carpeta de tu proyecto (ej. "miweb") dentro de la carpeta raíz de tu servidor (ej. "htdocs").
     2. Abre una terminal dentro de esa carpeta ("miweb").
     3. Ejecuta el comando: git init
     4. Esto creará una carpeta oculta ".git" y ya podrás empezar a usar comandos de Git.


===========================
10. Prueba de Servidor Web
===========================

Objetivo: Asegurarse de que el servidor puede mostrar la carpeta de tu proyecto.

---> Verificación:
     1. Dentro de la carpeta "miweb", crea un archivo llamado "index.html".
     2. Escribe dentro: <h1>Mi proyecto funciona</h1>
     3. Guarda el archivo.
     4. Abre en tu navegador: http://localhost/miweb/
     5. Deberías ver el texto "Mi proyecto funciona".


============================================
11. Usuario y Contraseña de DB Personalizados
============================================

Objetivo: Evitar usar el usuario "root" en tu aplicación por seguridad.

---> Instrucciones:
     1. Entra en phpMyAdmin.
     2. Ve a la pestaña "Cuentas de usuario".
     3. Haz clic en "Agregar cuenta de usuario".
     4. Rellena los campos:
        - Nombre de usuario: (ej. "usuario_proyecto")
        - Contraseña: (genera una contraseña segura)
     5. Marca la casilla "Crear base de datos con el mismo nombre y otorgar todos los privilegios".
     6. Haz clic en "Continuar".