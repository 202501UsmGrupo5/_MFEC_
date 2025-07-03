
# 🎨 Mi Fe en Colores (MFEC)

Proyecto final para el curso *ICN292 - Sistemas de Información para la Gestión* de la Universidad Técnica Federico Santa María.

## 📦 Descargar archivos del proyecto

Puedes descargar el paquete comprimido con todos los archivos desde aquí:

👉 [Descargar Codigo_MFEC.zip](Codigo_MFEC.zip)


Este software implementa un Sistema de Información para la Gestión (SIG) utilizando *Python, **MySQL* y *PyQt5*, permitiendo optimizar procesos de la organización a través de una interfaz gráfica.

---

## 🚀 Características principales
- Ventana de login conectada a MySQL
- Formularios GUI con PyQt5
- CRUD de datos directamente desde la interfaz
- Código modular para facilitar mantenibilidad

---

## 🧰 PASO 1: Requisitos previos

Asegúrate de tener instalados los siguientes programas:

| Herramienta            | Recomendación                        |
|------------------------|--------------------------------------|
| Python                 | 3.10 o superior                      |
| MySQL Server           | 8.0 o superior                       |
| MySQL Workbench        | Para gestionar gráficamente la BBDD |
| Qt Designer (Opcional) | Para editar interfaces .ui          |
| Git (opcional)         | Para versionar el proyecto          |
| VS Code                | Para editar código                  |


## 1.1: [Instalar Python](#instalar-python)
# ✅ Instalar Python

1. Ingresa a la página oficial:
   👉 https://www.python.org/downloads/

2. Descarga la última versión estable (3.10 o superior).

3. Durante la instalación, *marca la casilla*:
✅ Add Python to PATH

markdown
Copiar
Editar
y haz clic en *Install Now*.

4. Verifica la instalación abriendo una terminal (CMD o PowerShell):

##  Verifica la instalación de Python

Abre una terminal (CMD o PowerShell en Windows, o Terminal en macOS/Linux) y ejecuta:

``` bash
python --version
```
Deberías ver algo similar a:

Python 3.11.4

## 1.2: [Instalar MySQL Server y MySQL Workbench](#instalar-mysql-server-y-mysql-workbench)

✅ Instalar MySQL Server y MySQL Workbench
Descarga el instalador desde:
👉 https://dev.mysql.com/downloads/installer/

Ejecuta el instalador y selecciona la opción Custom.

En el menú de componentes:

En MySQL Servers, selecciona la última versión de MySQL Server.

En Applications, selecciona MySQL Workbench.

Haz clic en Next y luego en Execute para que descargue e instale.

Configura el servidor:

Deja los valores por defecto.

Define una contraseña sencilla para el usuario root (útil para el proyecto).

Haz clic en Next y Execute hasta completar el proceso.

Abre MySQL Workbench y conéctate usando:

Host: localhost

User: root

Password: tu contraseña configurada.


## 1.3: [Instalar Visual Studio Code](#instalar-visual-studio-code)

✅ Instalar Visual Studio Code
Descarga VS Code desde:
👉 https://code.visualstudio.com/

Instálalo con los valores predeterminados.

Al abrir VS Code, instala las extensiones recomendadas:

Python (de Microsoft)

Pylance (opcional, para autocompletado avanzado)

SQLTools (opcional, para gestionar la DB desde el editor)



## 1.4:  📦 Instalación de pip y dependencias del proyecto

Este proyecto requiere Python 3.6 o superior y algunos paquetes externos. Si aún no tienes `pip` instalado, sigue los pasos a continuación:


# Verificar si pip está instalado
pip --version
# o alternativamente:
python -m pip --version
python3 -m pip --version

# Si pip no está instalado, se puede instalar ingresando el siguiente código en la terminal:
python -m ensurepip --upgrade

# O bien, descarga el instalador desde:
# https://bootstrap.pypa.io/get-pip.py
# Y luego ejecuta:
python get-pip.py

# O bien, si usas Anaconda:
conda install pip



# Luego de tener instalar pip necesitas las siguientes librerías de Python:

`pip install PyQt5`
`pip install mysql-connector-python`
`pip install pandas`

## Las puedes instalar por separado o instalar todas juntas con el siguiente script:
`pip install PyQt5 mysql-connector-python pandas `

## 🗄️ PASO 2: Crear la base de datos en MySQL

1. Abre **MySQL Workbench** o la consola de comandos de MySQL.

2. Ejecuta las siguientes instrucciones para crear la base:


3. Si tienes el archivo `mfec.sql`:

   - Ve a `File > Open SQL Script` en MySQL Workbench
   - Carga el archivo `mfec.sql`
   - Presiona el rayo para ejecutar el script y crear todas las tablas necesarias

4. Asegúrate de que las siguientes tablas existan:

- `cliente`
- `producto`
- `pedido`
- `detallepedido`
- `ingreso`
- `egreso`

---

## 💾 PASO 3: Configurar el entorno del proyecto

1. Crea un entorno virtual (opcional pero recomendado):

```bash
python -m venv .venv
```

2. Actívalo:

- En Windows:
```bash
.venv\Scripts\activate
```

- En macOS/Linux:
```bash
source .venv/bin/activate
```

3. Instala las dependencias:

```bash
pip install PyQt5 mysql-connector-python

```

---


## 🖥️ PASO 4: Ejecutar la aplicación

1. Abre tu terminal o consola.
2. Navega a la carpeta raíz del proyecto:

```bash
cd /ruta/a/Codigo_MFEC
```

3. Ejecuta el programa principal:

```bash
python main.py
```

4. Se abrirá una ventana de **inicio de sesión**.

---

## ✅ PASO 5: Usar la interfaz gráfica

Una vez dentro del sistema, verás el **menú principal** con 2 opciones:

### 🔄 CRUD (Operaciones CRUD)

Aquí podrás:

- **Agregar** nuevos registros (clientes, productos, etc.)
- **Editar** datos existentes
- **Eliminar** registros
- **Buscar** por identificadores clave
- **Visualizar** todos los registros en una tabla

Las tablas disponibles son:

- Cliente
- Producto
- Pedido
- DetallePedido
- Ingreso
- Egreso

### 📊 Gestión General

Accede a:

- **Gestión de Pedidos**: Se debe ingresar el Pedido ID que se quiere visualizar, luego se puede imprimir los datos del cliente al que corresponde el Pedido ID ingresado
- **Gestión Financiera**: muestra ingresos, egresos y utilidad neta entre las fechas ingresadas

---

## 🔍 PASO 6: Verificación del funcionamiento

Para asegurarte de que todo funciona correctamente:

- Intenta **agregar un cliente** nuevo
- Luego, **crea un pedido** para ese cliente
- Añade productos al pedido desde `DetallePedido`
- Verifica que los registros aparezcan correctamente
- Registra un ingreso y un egreso
- Abre el módulo de **Gestión Financiera** y confirma los totales

---

---

## 🧪 Sugerencias

- Puedes extender el sistema agregando control de usuarios y contraseñas
- Agrega validaciones en los formularios para mayor robustez
- Implementa respaldos automáticos de la base de datos

