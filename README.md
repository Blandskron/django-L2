# Lección 2 - Proyecto Django

Este proyecto corresponde a una práctica básica de Django donde se crea un entorno virtual, se instala Django, se genera un proyecto, se crea una aplicación y se sube el código a GitHub.

---

## 1. Crear el repositorio en GitHub

1. Entrar a GitHub.
2. Presionar **New repository**.
3. Asignar un nombre al repositorio, por ejemplo:

```bash
leccion2-django
````

4. Seleccionar si será público o privado.
5. Crear el repositorio incluyendo Readme y .gitignore (python).
6. Copiar la URL del repositorio.

Ejemplo:

```bash
git clone https://github.com/usuario/leccion2-django.git
```

---

## 2. Entrar a la carpeta del proyecto

```bash
cd leccion2-django
```

---

## 3. Crear entorno virtual

```bash
python -m venv venv
```

Esto crea una carpeta llamada `venv`, donde se instalarán las dependencias del proyecto.

---

## 4. Activar entorno virtual

En Windows:

```bash
venv\Scripts\activate
```

Cuando esté activo, deberías ver algo como:

```bash
(venv)
```

---

## 5. Instalar Django

```bash
pip install django
```

---

## 6. Guardar dependencias

```bash
pip freeze > requirements.txt
```

Este comando crea el archivo `requirements.txt`, donde quedan registradas las librerías instaladas.

---

## 7. Crear proyecto Django

```bash
django-admin startproject leccion2
```

Esto genera la estructura base del proyecto Django.

---

## 8. Entrar a la carpeta del proyecto

```bash
cd leccion2
```

---

## 9. Ejecutar migraciones

```bash
python manage.py makemigrations
```

```bash
python manage.py migrate
```

Las migraciones preparan la base de datos inicial de Django.

---

## 10. Crear superusuario

```bash
python manage.py createsuperuser
```

Django pedirá:

```bash
Username:
Email address:
Password:
Password again:
```

Este usuario permite ingresar al panel de administración.

---

## 11. Ejecutar servidor

```bash
python manage.py runserver
```

Abrir en el navegador:

```bash
http://127.0.0.1:8000/
```

Panel de administración:

```bash
http://127.0.0.1:8000/admin/
```

---

## 12. Crear aplicación cliente

```bash
python manage.py startapp cliente
```

Esto crea una app llamada `cliente`.

Luego se debe registrar en `settings.py`:

```python
INSTALLED_APPS = [
    ...
    'cliente',
]
```

---

## 13. Instalar dependencias desde requirements.txt

Cuando otra persona descargue el proyecto, debe instalar las dependencias con:

```bash
pip install -r requirements.txt
```

---

## 14. Git - Subir proyecto a GitHub

Agregar archivos:

```bash
git add .
```

Crear commit:

```bash
git commit -m "leccion 2"
```

Subir a GitHub:

```bash
git push origin main
```

---
