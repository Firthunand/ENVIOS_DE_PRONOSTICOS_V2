# ENVIO DE PRONOSTICOS CLIMATICO POR SMS

Este proyecto es una aplicación que se conecta a la API de [WeatherAPI](https://www.weatherapi.com/api-explorer.aspx#forecast) para obtener el pronóstico del tiempo y envía un mensaje SMS con la información del clima utilizando [Twilio](https://www.twilio.com/).

## Requisitos Previos

Antes de ejecutar este proyecto, asegúrate de tener instalados los siguientes paquetes:

- Python 3.10 o superior
- `twilio`
- `requests`
- `pandas`
- `beautifulsoup4`
- `tqdm`

Puedes instalar estos paquetes utilizando `pip`:

```bash
pip install twilio requests pandas beautifulsoup4 tqdm
```

## Configuración

1. Twilio: Necesitarás una cuenta de Twilio y obtener las credenciales TWILIO_ACCOUNT_SID y TWILIO_AUTH_TOKEN. También necesitarás un número de teléfono de Twilio para enviar los mensajes SMS.

2. WeatherAPI: Necesitarás una clave API de WeatherAPI. Puedes obtenerla registrándote en WeatherAPI.

3. Configuración del archivo twilio_config.py: Crea un archivo llamado twilio_config.py en el mismo directorio que tu script y añade las siguientes variables con tus credenciales

    ```bash
        TWILIO_ACCOUNT_SID = 'your_account_sid'
        TWILIO_AUTH_TOKEN = 'your_auth_token'
        PHONE_NUMBER = 'your_twilio_phone_number'
        API_KEY_WAPI = 'your_weatherapi_key'
    ```

## Ejecución

Para ejecutar el script, simplemente ejecuta el archivo de Jupyter Notebook o el script de Python en tu entorno.

```bash
    jupyter notebook
```
O si estás ejecutando un script de Python:

```bash
    python nombre_del_script.py
```

## Descripción del Código

El script realiza las siguientes acciones:

1. Instalación de dependencias: Asegura que todas las dependencias necesarias estén instaladas.

2. Conexión a WeatherAPI: Obtiene el pronóstico del tiempo para una ubicación específica.

3. Procesamiento de datos: Extrae la información relevante del pronóstico y la organiza en un DataFrame de Pandas.

4. Filtrado de datos: Filtra las horas en las que se espera lluvia.

5. Envío de SMS: Utiliza Twilio para enviar un mensaje SMS con el pronóstico del tiempo.

## Ejemplo de Salida

Hola!

El pronóstico del tiempo hoy 2023-10-01 en limache es:

    Hora   Condicion
     7     Lluvia ligera
    12     Lluvia moderada
    18     Lluvia ligera

## Próximos Pasos

Para mejorar este proyecto, se pueden implementar las siguientes funcionalidades:

### Automatizar el Envío de SMS con AWS y EC2

1. Crear una instancia EC2 en AWS
2. Configurar el entorno en la instancia EC2
3. Subir el script a la instancia EC2
4. Programar la ejecución del script
5. Monitorear y gestionar la instancia
