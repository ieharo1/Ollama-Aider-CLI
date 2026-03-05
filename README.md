# 🤖 Ollama + Aider CLI

Tu propio "Claude Code" pero 100% gratis, local y multiplataforma desarrollado por **Isaac Esteban Haro Torres**.

---

## 📝 Descripción

Este repositorio documenta paso a paso cómo montar un CLI de Inteligencia Artificial para desarrollo usando Ollama + Aider, ideal para trabajar directamente sobre proyectos reales desde la terminal.

La idea es simple:
- ❌ Sin APIs de pago
- ❌ Sin límites artificiales
- ❌ Sin enviar tu código a terceros
- ✅ Todo corre local
- ✅ Funciona directo sobre tu repo

---

## 🎯 Para qué sirve

- Refactors grandes de código
- Análisis de proyectos locales
- Generación y modificación de código
- Proyectos que requieren privacidad
- Trabajo offline
- Asistencia de programación en terminal

---

## 🏗 Arquitectura

```
Tu Proyecto → Aider CLI → Ollama → Modelo LLM Local
              ↓
         Git (control de versiones)
```

---

## 🧠 ¿Qué es esto?

- **Ollama**: motor local para correr modelos LLM (DeepSeek, LLaMA, Mistral, etc.)
- **Aider**: CLI que conecta un LLM con tu repositorio Git para leer, analizar y modificar código

Combinados, tienes un asistente de programación en terminal que:
- Entiende la estructura de tu proyecto
- Analiza arquitectura
- Propone mejoras
- Genera y modifica código

---

## 💻 Requisitos

### Sistema

- Windows 10 / 11 (x64)
- macOS o Linux
- **RAM recomendada**: 8 GB mínimo, 16 GB ideal

### Software

- Git
- Python 3.10+
- Node.js (opcional)

---

## 🚀 Instalación

### 1️⃣ Instalar Ollama

Descarga e instala desde: https://ollama.com

Verifica:
```powershell
ollama list
```

### 2️⃣ Descargar modelos

**Modelo ligero (recomendado):**
```powershell
ollama pull deepseek-coder:latest
```

**Modelo más potente:**
```powershell
ollama pull deepseek-coder:6.7b
```

### 3️⃣ Configurar variable de entorno

```powershell
setx OLLAMA_API_BASE http://127.0.0.1:11434
```

### 4️⃣ Instalar Aider

```powershell
pip install aider-chat
```

Verifica:
```powershell
aider --version
```

---

## 💡 Uso

```powershell
# Entra al proyecto
cd ruta/a/tu/proyecto

# Activa entorno virtual (si aplica)
.venv\Scripts\activate

# Arranca Aider
aider --model ollama/deepseek-coder:latest --map-tokens 512 --no-auto-commit
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
- Refactors
- Mejoras de arquitectura
- Generación de features

---

## 🛠️ Comandos útiles

```powershell
# Ver modelos activos
ollama ps

# Probar Ollama directamente
ollama run deepseek-coder:latest

# Ver ayuda
aider --help
```

---

## ⚠️ Problemas comunes

### Error: puerto 11434 en uso
```
Only one usage of each socket address...
```
✅ No es un error - Ollama ya está corriendo

### Aider se queda en "Waiting for model"
- Reduce `--map-tokens`
- Usa `deepseek-coder:latest`
- Cierra apps pesadas

---

## 🆚 Cuándo usar esto vs CLI cloud

| Característica | Ollama + Aider | CLI Cloud |
|---------------|----------------|-----------|
| Costo | Gratis | Pago por uso |
| Privacidad | Total | Envía código |
| Offline | ✅ | ❌ |
| Velocidad | Depende HW | Rápido |
| Ideal para | Proyectos grandes | Queries rápidos |

---

## 📌 Conclusión

Este stack te da:
- Un CLI de IA estilo Claude Code
- Completamente gratis
- Control total sobre tu código
- Extensible y reutilizable

Ideal para desarrolladores que quieren potencia sin dependencia de APIs de pago.

---

## 👨‍💻 Desarrollado por Isaac Esteban Haro Torres

**Ingeniero en Sistemas · Full Stack · Automatización · Data**

- 📧 Email: zackharo1@gmail.com
- 📱 WhatsApp: 098805517
- 💻 GitHub: https://github.com/ieharo1
- 🌐 Portafolio: https://ieharo1.github.io/portafolio-isaac.haro/

---

© 2026 Isaac Esteban Haro Torres - Todos los derechos reservados.

