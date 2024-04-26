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
