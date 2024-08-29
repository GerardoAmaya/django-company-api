
# FakeCompany

FakeCompany es un sistema de gestión de procedimientos diseñado para facilitar y optimizar la administración de procesos en una organización. Este proyecto está construido utilizando Django, un framework web de alto nivel en Python.

## Características

- **Gestión de Usuarios:** Registro, inicio de sesión, y recuperación de contraseñas.
- **Administración de Procedimientos:** Permite la creación, edición, y seguimiento de procedimientos.
- **Sistema de Notificaciones:** Envía notificaciones por correo electrónico para confirmar acciones y actualizaciones importantes.
- **Panel de Administración:** Un panel de administración integrado para gestionar los datos de la aplicación.

## Requisitos Previos

Antes de empezar, asegúrate de tener los siguientes requisitos previos instalados:

- **Python 3.12+**
- **Django 5.1+**
- **MySQL**
- **Git**
- **Un entorno virtual para Python** (virtualenv recomendado)

## Instalación

Sigue estos pasos para configurar el proyecto en tu máquina local:

### 1. Clona el Repositorio

\`\`\`bash
git clone git@github.com:GerardoAmaya/fake-company.git
cd fakecompany
\`\`\`

### 2. Configura el Entorno Virtual

\`\`\`bash
python3 -m venv myenv
source myenv/bin/activate  # En Windows usa \`myenv\Scripts\activate\`
\`\`\`

### 3. Instala las Dependencias

\`\`\`bash
pip install -r requirements.txt
\`\`\`

### 4. Configura la Base de Datos

Crea una base de datos MySQL llamada \`fakecompany\` y configura las credenciales en el archivo \`settings.py\`.

\`\`\`sql
CREATE DATABASE fakecompany;
\`\`\`

Asegúrate de configurar la conexión a MySQL en \`settings.py\`:

\`\`\`python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'fakecompany',
        'USER': 'tu_usuario',
        'PASSWORD': 'tu_contraseña',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
\`\`\`

### 5. Realiza las Migraciones

\`\`\`bash
python manage.py makemigrations
python manage.py migrate
\`\`\`

### 6. Crea un Superusuario

\`\`\`bash
python manage.py createsuperuser
\`\`\`

### 7. Ejecuta el Servidor de Desarrollo

\`\`\`bash
python manage.py runserver
\`\`\`

Visita \`http://127.0.0.1:8000\` en tu navegador para ver la aplicación en funcionamiento.

## Uso

Después de iniciar el servidor, puedes acceder a las siguientes funcionalidades:

- **/register/** - Registro de nuevos usuarios.
- **/login/** - Inicio de sesión para usuarios registrados.
- **/home/** - Panel principal para usuarios autenticados.
- **/logout/** - Cerrar sesión.

## Autor

**Gerardo Amaya**
[gerardoamayasv2000@gmail.com](mailto:gerardoamayasv2000@gmail.com)

## Licencia

Este proyecto está bajo la licencia MIT. Consulta el archivo \`LICENSE\` para más detalles.
