Pruebas Automatizadas con Cypress
Repositorio de pruebas https://github.com/cmauriciocarrillo/TestDemoBlaze

Este archivo proporciona instrucciones para ejecutar las pruebas automatizadas utilizando Cypress. El código realiza pruebas tanto en una API como en una interfaz web para crear y autenticar usuarios.

1. Requisitos Previos
Antes de ejecutar las pruebas, asegúrate de tener los siguientes requisitos instalados:

Node.js: Debe estar instalado en tu sistema. Puedes descargarlo desde Node.js.
Cypress: La herramienta de pruebas automatizadas. Se instalará en el siguiente paso.

2. Configuración del Proyecto
Clona el Repositorio: Si aún no tienes el proyecto en tu máquina, clónalo desde tu repositorio (o crea un nuevo proyecto si estás configurando desde cero).


git clone <URL_DEL_REPOSITORIO>
cd <NOMBRE_DEL_DIRECTORIO>
Instala las Dependencias:

Asegúrate de que el archivo package.json esté presente en el directorio del proyecto. Luego, instala las dependencias necesarias:


npm install
Si encuentras errores relacionados con la instalación, asegúrate de que package.json esté correctamente configurado y que los permisos de archivo sean adecuados.

Instala Cypress:

Si Cypress no está listado en package.json, instálalo con el siguiente comando:


npm install cypress --save-dev
Configura Cypress:

Abre Cypress por primera vez para que genere la estructura de carpetas y archivos predeterminada:


npx cypress open
Esto creará un directorio cypress con subdirectorios y archivos predeterminados.

3. Ejecución de Pruebas
Guardar el Código de Prueba:

Crea un archivo en el directorio cypress/integration y copia el código de prueba proporcionado en este archivo. Por ejemplo, guarda el archivo como user_tests.js.

Ejecuta las Pruebas:

Para ejecutar las pruebas en modo interactivo, usa:

npx cypress open
Esto abrirá la interfaz de usuario de Cypress, donde podrás seleccionar y ejecutar las pruebas.

Para ejecutar las pruebas en modo headless (sin interfaz gráfica), usa:

npx cypress run
Verifica los Resultados:

Una vez que se ejecuten las pruebas, revisa los resultados en la interfaz de usuario de Cypress o en la salida de la consola (si ejecutaste en modo headless). Los resultados mostrarán si las pruebas pasaron o fallaron, junto con los detalles relevantes.

4. Detalles de las Pruebas
El código de prueba realiza las siguientes acciones:

Version API
Creación de un nuevo usuario en signup API:

Realiza una solicitud POST a la API de registro.
Verifica si el usuario fue creado exitosamente o si hubo un error.
Intento de creación de usuario ya existente en API:

Intenta crear un usuario con el mismo nombre.
Verifica si el sistema maneja el error correctamente.
Ingreso de usuario y password correcto en login API:

Realiza una solicitud POST para iniciar sesión con credenciales válidas.
Verifica si el inicio de sesión fue exitoso y si se recibió un token de autenticación.
Ingreso de usuario y password incorrecto en login API:

Intenta iniciar sesión con una contraseña incorrecta.
Verifica si el sistema devuelve un mensaje de error.
Version WEB
Creación de un nuevo usuario en signup WEB:

Navega a la página de registro y completa el formulario.
Verifica si el usuario fue creado correctamente en la interfaz web.
Intento de creación de usuario ya existente en WEB:

Intenta crear un usuario con el mismo nombre.
Verifica si el sistema maneja el error correctamente en la interfaz web.
Ingreso de usuario y password correcto en login WEB:

Navega a la página de inicio de sesión y completa el formulario.
Verifica si el inicio de sesión fue exitoso en la interfaz web.
Ingreso de usuario y password incorrecto en login WEB:

Intenta iniciar sesión con una contraseña incorrecta.
Verifica si el sistema devuelve un mensaje de error en la interfaz web.

5. Solución de Problemas
Errores de Instalación: Asegúrate de que package.json esté presente y que los permisos de archivo sean correctos. Intenta ejecutar npm cache clean --force y luego npm install.
Errores de Cypress: Revisa el archivo de log generado por Cypress para obtener detalles adicionales sobre los errores.
Para más información y soporte, consulta la documentación oficial de Cypress y el repositorio de problemas de Cypress en GitHub.