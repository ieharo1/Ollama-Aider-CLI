# 🚀 Ollama + Aider CLI

> **Tu propio "Claude Code" pero 100% gratis, local y multiplataforma**

Este repositorio documenta paso a paso cómo montar un **CLI de Inteligencia Artificial para desarrollo** usando **Ollama + Aider**, ideal para trabajar directamente sobre proyectos reales (Django, Python, JS, etc.) desde la terminal.

La idea es simple:

* ❌ Sin APIs de pago
* ❌ Sin límites artificiales
* ❌ Sin enviar tu código a terceros
* ✅ Todo corre local
* ✅ Funciona directo sobre tu repo

---

## 🧠 ¿Qué es esto?

* **Ollama**: motor local para correr modelos LLM (DeepSeek, LLaMA, etc.)
* **Aider**: CLI que conecta un LLM con tu repositorio Git para leer, analizar y modificar código

Combinados, tienes un **asistente de programación en terminal** que:

* entiende la estructura de tu proyecto
* analiza arquitectura
* propone mejoras
* genera y modifica código

---

## 🧩 Requisitos

### Sistema

* Windows 10 / 11 (x64)
* macOS o Linux (también funciona)
* **RAM recomendada**:

  * mínimo: 8 GB
  * ideal: 16 GB

### Software

* Git
* Python 3.10+
* Node.js (opcional)

---

## 1️⃣ Instalar Ollama

Descarga e instala Ollama desde:

👉 [https://ollama.com](https://ollama.com)

> En Windows, Ollama se ejecuta como servicio automáticamente.

Verifica instalación:

```powershell
ollama list
```

---

## 2️⃣ Descargar modelos recomendados

### Modelo ligero (recomendado para empezar)

```powershell
ollama pull deepseek-coder:latest
```

### Modelo más potente (opcional)

```powershell
ollama pull deepseek-coder:6.7b
```

Verifica:

```powershell
ollama list
```

---

## 3️⃣ Configurar variable de entorno (IMPORTANTE)

Aider necesita saber dónde está Ollama:

```powershell
setx OLLAMA_API_BASE http://127.0.0.1:11434
```

Luego:

* cierra todas las terminales
* abre una nueva

Verifica:

```powershell
echo $env:OLLAMA_API_BASE
```

---

## 4️⃣ Instalar Aider

Dentro de tu entorno Python (recomendado usar venv):

```powershell
pip install aider-chat
```

Verifica:

```powershell
aider --version
```

---

## 5️⃣ Usar Aider en tu proyecto

### 1. Entra al proyecto

```powershell
cd ruta/a/tu/proyecto
```

### 2. Activa el entorno virtual (si aplica)

```powershell
.venv\Scripts\activate
```

### 3. Arranca Aider (configuración estable)

```powershell
aider --model ollama/deepseek-coder:latest --map-tokens 512 --no-auto-commit --no-show-model-warnings
```

---

## 🧪 Prompt inicial recomendado

Usa prompts pequeños al inicio:

```
lista únicamente:
- estructura de carpetas principal
- apps detectadas

no hagas cambios
```

Luego puedes avanzar a:

* refactors
* mejoras de arquitectura
* generación de features

---

## 🛠️ Comandos útiles

### Ver modelos activos

```powershell
ollama ps
```

### Probar Ollama directamente

```powershell
ollama run deepseek-coder:latest
```

---

## ⚠️ Problemas comunes

### ❌ Error: puerto 11434 en uso

```
Only one usage of each socket address...
```

✔ No es un error
✔ Ollama ya está corriendo
✔ NO ejecutes `ollama serve`

---

### ❌ Aider se queda en "Waiting for model"

Soluciones:

* reduce `--map-tokens`
* usa `deepseek-coder:latest`
* cierra apps pesadas

---

## 📌 ¿Cuándo usar esto?

✔ Refactors grandes
✔ Proyectos locales
✔ Código sensible
✔ Trabajo offline

Para proyectos pequeños o rapidez extrema, un CLI cloud (ej: Gemini CLI) puede ser más veloz.

---

## ⭐ Conclusión

Este stack te da:

* un **CLI de IA estilo Claude Code**
* completamente gratis
* control total sobre tu código
* extensible y reutilizable

Ideal para desarrolladores que quieren **potencia sin dependencia de APIs de pago**.

---

## 🧑‍💻 Autor

Isaac Haro
Ingeniero en Sistemas · Full Stack · Automatización & Data

---

## 📄 Licencia

MIT — úsalo, modifícalo y compártelo 🚀
