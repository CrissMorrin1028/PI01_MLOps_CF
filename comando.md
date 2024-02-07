Comandos para activar **``FastAPI ``**
> Entrar al directorio

Activar un nuevo entorno virtual

```powershell
python -m venv venv

ls 
```

Activar el entorno virtual cuando terminemos el proceso
```powershell
.\venv\Scripts\Activate
```


Desactivar el entorno virtual
```powershell
deactivate
```

descargar fastapi **uvicorn** en el env
```powershell
pip install fastapi uvicorn
```

Abrir visual studio code
```powershell
code .
```
Crear un archivo **``main.py``** con la siguiente estructura basica para probar y guardamos el archivo ``ctrl`` + ``s``:
```python
from fastapi import FastAPI
app = FastAPI()

@app.get("/")

def message():
    return {"message": "Hello mundo"}
```
Activamos la aplicación 
```powershell
uvicorn main:app
```
Si queremos cambiar el puerto de **``8000``** a **``5000``**
```powershell
uvicorn main:app --port 5000
```
Mantener los cambios actualizandose automaticamente 
```powershell
uvicorn main:app --port 5000 --reload
```


---
Crear un archivo txt con las dependencias despues de instalar todas las librerias necesarias 
```powershell
pip freeze > requirements.txt
```
Observar los requerimientos desde la terminal
```powershell
type requirements.txt
```

### Librerias que se usaran en este proyecto en especifico
```powershell
pip install scikit-learn

pip install pandas 

pip install numpy

pip install pyarrow
```
Serían 
pandas
numpy
uvicorn
pyarrow
fastapi
scikit-learn


Requerimientos: **``requeriments.txt``**
annotated-types==0.6.0
anyio==4.2.0
click==8.1.7
colorama==0.4.6
cramjam==2.8.1
fastapi==0.109.1
fastparquet==2023.10.1
fsspec==2023.12.2
h11==0.14.0
idna==3.6
joblib==1.3.2
numpy==1.26.3
packaging==23.2
pandas==2.2.0
pyarrow==15.0.0
pydantic==2.6.0
pydantic_core==2.16.1
python-dateutil==2.8.2
pytz==2024.1
scikit-learn==1.4.0
scipy==1.12.0
six==1.16.0
sniffio==1.3.0
starlette==0.35.1
threadpoolctl==3.2.0
typing_extensions==4.9.0
tzdata==2023.4
uvicorn==0.27.0.post1

---
### Consejos utiles
Para matar un proceso en PowerShell, puedes seguir estos pasos:

1. Primero, necesitas encontrar el ID del proceso (PID) del servidor. Puedes hacer esto con el comando `Get-Process`. Si sabes que el nombre del proceso es `uvicorn`, puedes usar el siguiente comando para obtener su PID:

```powershell
Get-Process | Where-Object {$_.ProcessName -like "*uvicorn*"}
```

Esto te dará una lista de todos los procesos que tienen `uvicorn` en su nombre. Busca el PID del proceso que quieres matar.

2. Una vez que tienes el PID, puedes usar el comando `Stop-Process` para matar el proceso. Por ejemplo, si el PID es 1234, puedes matar el proceso con el siguiente comando:

```powershell
Stop-Process -Id 1234
```

Por favor, ten en cuenta que necesitarás reemplazar `1234` con el PID real de tu proceso. Además, es posible que necesites permisos de administrador para matar algunos procesos. Si recibes un error de permisos, intenta ejecutar PowerShell como administrador.

### Pasos cuando este creando la app en FastAPI
* Ejecuto los comandos anteriores 
* Desactivo el autoguardado
* Descargar las dependencias
* Probamos de forma basica la aplicacion y configuramos el entorno para la primera funcion
* 
