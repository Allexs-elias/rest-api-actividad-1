REST API - Actividad 1
Proyecto base de una REST API hecha con Django y Django REST Framework, siguiendo una estructura más ordenada y usando variables de entorno para manejar la configuración de forma segura.
Esta actividad corresponde a la Actividad 1: Arquitectura y configuración de una REST API.

🚀 Tecnologías usadas


Python 3


Django


Django REST Framework


python-dotenv


dj-database-url



📂 Estructura del proyecto
rest_api_project/├── api/├── apps/├── config/│   ├── settings/│   │   ├── base.py│   │   ├── development.py│   │   └── production.py├── .env.example├── .gitignore├── manage.py└── requirements.txt

⚙️ Instalación
Primero clona el repositorio:
git clone https://github.com/Allexs-elias/rest-api-actividad-1.gitcd rest-api-actividad-1
Después crea y activa el entorno virtual:
Windows
python -m venv venvvenv\Scripts\activate
Mac/Linux
python -m venv venvsource venv/bin/activate
Instala las dependencias:
pip install -r requirements.txt
Copia el archivo .env.example para crear tu archivo .env:
copy .env.example .env
Genera una nueva SECRET_KEY:
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"
Luego ejecuta las migraciones:
python manage.py migrate
Y finalmente inicia el servidor:
python manage.py runserver

🔐 Variables de entorno
El proyecto usa variables de entorno para guardar datos importantes como:


SECRET_KEY


DEBUG


ALLOWED_HOSTS


DATABASE_URL


El archivo .env está ignorado en Git para evitar subir información sensible al repositorio.

🛡️ Seguridad
Se separaron las configuraciones de desarrollo y producción para tener un mejor control del proyecto. También se agregaron configuraciones básicas de seguridad para producción, como cookies seguras y redirección HTTPS.

📝 Autor
Alejandro
Actividad académica - REST API con Django