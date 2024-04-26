# Instalación de Odoo 17 en macOS

Este es un tutorial paso a paso para instalar Odoo 17 en macOS. Odoo es una plataforma de código abierto para la gestión empresarial que incluye una variedad de aplicaciones empresariales.

## Requisitos previos

- Python 3
- Homebrew (opcional pero recomendado)

## Paso 1: Instalar dependencias

1. Abre la terminal.
2. Instala Python 3 y PostgreSQL utilizando Homebrew ejecutando los siguientes comandos:

brew install python3 postgresql
brew services start postgresql 


## Paso 2: Crear un entorno virtual

1. En la terminal, crea un entorno virtual para Odoo ejecutando el siguiente comando:

python3 -m venv odoo-venv

2. Activa el entorno virtual ejecutando:

source odoo-venv/bin/activate


## Paso 3: Instalar Odoo 17

1. Asegúrate de que estás en el entorno virtual activado.
2. Actualiza pip:

pip install --upgrade pip

3. Instala Odoo 17:

pip install odoo


## Paso 4: Configurar Odoo

1. Crea una base de datos PostgreSQL para Odoo ejecutando:

createdb -O username odoo

Reemplaza 'username' con tu nombre de usuario de PostgreSQL.

2. Copia un archivo de configuración de ejemplo de Odoo y personalízalo según tus necesidades:

cp ~/odoo-venv/lib/python3.x/site-packages/odoo/tools/config.py ~/odoo.conf


3. Abre el archivo de configuración en un editor de texto y configura los parámetros según tu entorno y preferencias.

## Paso 5: Ejecutar Odoo

1. Activa tu entorno virtual (si no lo has hecho ya) ejecutando:

source odoo-venv/bin/activate


2. Ejecuta Odoo con el siguiente comando, reemplazando '/ruta/a/tu/odoo.conf' con la ruta absoluta a tu archivo de configuración:

odoo -c /ruta/a/tu/odoo.conf


## Paso 6: Acceder a Odoo

1. Una vez que Odoo esté en funcionamiento, abre un navegador web y visita la dirección http://localhost:8069 (o la dirección y el puerto que hayas configurado en tu archivo de configuración) para acceder a la interfaz web de Odoo.

¡Listo! Ahora deberías tener Odoo 17 instalado y funcionando en tu sistema macOS.



