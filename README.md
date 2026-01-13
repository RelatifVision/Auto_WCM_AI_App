## Requisitos e Instalación

### 1. Clonar el repositorio

git clone https://github.com/RelatifVision/Auto_WCM_AI_App,git

### 2. Crear entorno virtual
python -m venv venv ia_wcm

### 3. Activar entorno virtual
source venv/bin/activate

### 4. Instalar dependencias
pip install -r requirements.txt

### 5. Instalar Pytesseract
pip install pytesseract

### 6. Instalar Spacy Spanish Large
python -m spacy download es_core_news_lg 

### 7. Instalar google OAuth
pip install --upgrade google-api-python-client google-auth-httplib2 google-auth-oauthlib

### 8. Configurar las APIs de Google
a) Google Cloud Console (Web)
  1. Ve a Google Cloud Console
  2. Crea un nuevo proyecto o selecciona uno existente
  3. Habilita las APIs:
    · Google Calendar API
    · Gmail API
  4. Crea credenciales OAuth 2.0:
    · Tipo de aplicación: Aplicación de escritorio
    · Descarga el archivo credentials.json y mover la ruta calendar_api_setting/credentials.json

b) Ve a Gmail Settings (Web)
  1. Ve a Google Cloud Console
  2. Habilita IMAP en la pestaña "Reenvío y correo POP/IMAP"
  3. Genera una Contraaseña de aplicación:
    · Ve a Google Account Security (Web)
    · Activa Verificación en dos pasos
    · Ve a Contraseñas de aplicaciones
    · Selecciona "Mail" y "Windows Computer"
    · Copia la contraseña de 16 dígitos

### 9. Modifica los valores comentados en 'config.py' ylo mismo con 'credentials.json' y 'service-account-file.json' tienen que tener vuestras credenciales con vuestos pass
  · # EMAIL_ADDRESS = "CORREO_ELECTRONICO" 
  · # APP_PASSWORD = "PASSWORD_APP" 
  · # CALENDAR_ID = 'ID_CALENDAR' 


### 10. Ejecutar la App
python main.py

Este repositorio no incluye modelos de spaCy debido a su tamaño. Sigue estas instrucciones para instalar el modelo que mejor se adapte a tus necesidades:  

### Modelos disponibles:  
- **Pequeño (sm):** `es_core_news_sm` (recomendado para dispositivos con pocos recursos)  
- **Mediano (md):** `es_core_news_md`  
- **Grande (lg):** `es_core_news_lg` (requiere más memoria)  
# Auto_WCM_AI_App

