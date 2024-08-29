
# FakeCompany Project

Este es un proyecto de Django que incluye funcionalidades de registro, login y recuperación de contraseñas, utilizando MySQL como base de datos.

## Pasos para Configurar y Ejecutar el Proyecto

### 1. Clona el Repositorio

```bash
git clone git@github.com:GerardoAmaya/fake-company.git
cd fakecompany
```

### 2. Configura el Entorno Virtual

```bash
python3 -m venv myenv
source myenv/bin/activate  # En Windows usa `myenv\Scripts\activate`
```

### 3. Instala las Dependencias

```bash
pip install -r requirements.txt
```

### 4. Configura la Base de Datos

Crea una base de datos MySQL llamada `fakecompany` y configura las credenciales en el archivo `settings.py`.

```sql
CREATE DATABASE fakecompany;
```

Asegúrate de configurar la conexión a MySQL en `settings.py`:

```python
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
```

### 5. Realiza las Migraciones

```bash
python manage.py makemigrations
python manage.py migrate
```

### 6. Crea un Superusuario

```bash
python manage.py createsuperuser
```

### 7. Ejecuta el Servidor

```bash
python manage.py runserver
```

Ahora deberías poder visitar las rutas `/login/`, `/register/`, y `/home/` para ver las funcionalidades básicas de registro, login, y logout en acción.

## Autor

- **Gerardo Amaya** - *Desarrollador* - [gerardoamaya@example.com](mailto:gerardoamaya@example.com)
