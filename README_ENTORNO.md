# Guía de Uso del Entorno Virtual

## ✅ Instalación Completada

Se ha creado exitosamente un entorno virtual para este proyecto con todas las dependencias instaladas.

## 📦 Paquetes Instalados

- **Ciencia de Datos**: numpy 2.3.1, pandas 2.3.1, scipy 1.16.0, pyarrow 20.0.0
- **Machine Learning**: scikit-learn 1.7.0
- **Jupyter**: ipykernel 6.29.5, ipython 9.4.0, jupyter_client 8.6.3
- **Web Framework**: fastapi 0.122.0, uvicorn 0.38.0
- **Utilidades**: requests 2.32.5, y más...

## 🚀 Cómo Activar el Entorno Virtual

### En PowerShell:
```powershell
.\venv\Scripts\Activate.ps1
```

### En CMD:
```cmd
.\venv\Scripts\activate.bat
```

### En Git Bash:
```bash
source venv/Scripts/activate
```

## 🔧 Cómo Usar el Entorno

### 1. Ejecutar scripts de Python:
```powershell
# Activar el entorno primero
.\venv\Scripts\Activate.ps1

# Luego ejecutar tu script
python tu_script.py
```

### 2. Usar Jupyter Notebook:
```powershell
# Activar el entorno
.\venv\Scripts\Activate.ps1

# Instalar el kernel de Jupyter (solo la primera vez)
python -m ipykernel install --user --name=producto-datos-lab --display-name "Python (producto-datos-lab)"

# Iniciar Jupyter
jupyter notebook
```

### 3. Ejecutar FastAPI:
```powershell
# Activar el entorno
.\venv\Scripts\Activate.ps1

# Ejecutar el servidor (ajusta el nombre del archivo según tu proyecto)
uvicorn main:app --reload
```

## 📝 Comandos Útiles

### Verificar paquetes instalados:
```powershell
.\venv\Scripts\python.exe -m pip list
```

### Instalar paquetes adicionales:
```powershell
.\venv\Scripts\python.exe -m pip install nombre_paquete
```

### Actualizar requirements.txt:
```powershell
.\venv\Scripts\python.exe -m pip freeze > requirements.txt
```

### Desactivar el entorno:
```powershell
deactivate
```

## ⚠️ Importante

- **Siempre activa el entorno virtual** antes de trabajar en el proyecto
- Este entorno es **independiente** de tu instalación global de Python/Anaconda
- No hay conflictos con otros paquetes instalados en tu sistema
- El entorno está ubicado en: `.\venv\`

## 🔄 Reinstalar desde cero

Si necesitas reinstalar todo:
```powershell
# Eliminar el entorno actual
Remove-Item -Recurse -Force .\venv

# Crear nuevo entorno
python -m venv venv

# Activar
.\venv\Scripts\Activate.ps1

# Instalar dependencias
pip install -r requirements.txt
```

## 📌 Notas Adicionales

- El archivo `.gitignore` debería incluir `venv/` para no subir el entorno a Git
- Si trabajas en equipo, solo comparte el `requirements.txt`, no el directorio `venv/`
