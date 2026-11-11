# MYPROYECT
DOCUMENTATION
# 🎓 Calculadora de Créditos Académicos — Universidad de Pamplona

Herramienta web para que los programas académicos de la **Universidad de Pamplona** puedan construir, validar y exportar su plan de estudios de pregrado de forma rápida, ordenada y sin errores de cálculo.

Desarrollada por la **Oficina de Autoevaluación y Acreditación Institucional**.

> ⚡ **Sin instalación. Funciona 100% en el navegador.**

---

## 🚀 Demo

👉 **Pruébala aquí:** https://Razor922.github.io/MYPROYECT/

> Si aún no la has publicado, actívala en **Settings → Pages → Branch: main → Save** y en 1 minuto tendrás la URL funcionando.

---

## ✨ Características principales

- 📚 **Gestión por semestres** — crea, edita y elimina semestres fácilmente.
- 🧮 **Cálculo automático** de horas teóricas (HT), prácticas (HP), contacto indirecto (HCI) y totales semestrales (HTS).
- ✅ **Validación de créditos** con semáforo visual (verde = correcto, rojo = error).
- 🏷️ **Clasificación por componentes** de formación: CSH, CFB, CFP y CP.
- 📅 **Períodos académicos flexibles**: 12, 16 o 18 semanas (incluye especializaciones).
- 📊 **Resumen por semestre** y **plan de estudios global** con totales consolidados.
- 🧩 **Distribución por componentes**: número de asignaturas, créditos y porcentajes.
- 💾 **Guardar y cargar progreso** en archivo JSON.
- 📄 **Exportación profesional** a **PDF** (A3 horizontal) y **Excel** (con formato, colores y hojas separadas).
- 🔒 **Protección de datos**: alerta antes de cerrar la pestaña con opción de guardar.
- 🌐 **Interfaz con identidad institucional** y tooltips guía en cada campo.

---

## 🧠 ¿Cómo funciona el cálculo?

La herramienta sigue el modelo de créditos académicos colombiano:

| Variable | Fórmula |
|----------|---------|
| **HT** (Horas Teóricas) | `T × semanas` |
| **HP** (Horas Prácticas) | `P × 3 × semanas` |
| **HCI** (Horas de Contacto Indirecto) | `T × 2 × semanas` |
| **HTS** (Horas Totales Semestrales) | `HT + HP + HCI` |
| **Crédito Validado** | `HTS / (semanas × 3)` |

> **1 crédito = 48 horas totales de trabajo académico.**

La herramienta **compara** el crédito ingresado por el usuario con el crédito validado y marca en **verde** si coinciden o en **rojo** si hay discrepancia.

---

## 🛠️ Tecnologías utilizadas

| Tecnología | Uso |
|------------|-----|
| **HTML5 + CSS3** | Estructura y estilos |
| **JavaScript (Vanilla)** | Lógica de negocio y cálculos |
| **[SheetJS (xlsx)](https://sheetjs.com/)** | Exportación a Excel con formato |
| **[html2pdf.js](https://github.com/eKoopmans/html2pdf.js)** | Generación de PDF |
| **GitHub Pages** | Hosting estático |

> No requiere backend, base de datos ni frameworks. Todo corre del lado del cliente.

---

## 📋 Cómo usar la herramienta

### 1️⃣ Ingresa a la aplicación
Pulsa **"INGRESAR"** en la pantalla de inicio.

### 2️⃣ Crea un semestre
Pulsa **"Agregar nuevo semestre"** y selecciona el período académico (12, 16 o 18 semanas).

### 3️⃣ Agrega asignaturas
En cada semestre, pulsa **"Agregar nueva materia"** y completa:
- Código (opcional)
- Nombre de la asignatura
- Créditos totales
- Créditos teóricos (T) y prácticos (P)
- Componente de formación
- Requisito (opcional)

### 4️⃣ Valida y genera
- El sistema calcula automáticamente HT, HP, HCI, HTS y el crédito validado.
- Si todo está en verde ✅, pulsa **"Generar semestre"**.

### 5️⃣ Calcula el plan de estudios
Cuando tengas **2 o más semestres generados**, pulsa **"Calcular Plan de Estudios"**.
> 🔁 El sistema **recalcula primero todos los semestres en orden (1 → N)** y **al final el plan de estudios**, para garantizar que cualquier cambio reciente se refleje en los totales.

### 6️⃣ Exporta
Pulsa **"Descargar PDF y Excel"** para obtener:
- Un **PDF** con todos los semestres, el plan de estudios y los componentes.
- Un **Excel** con hojas separadas: `Semestre 1`, `Semestre 2`… `Plan Estudios` y `Componentes`.

---

## 💾 Guardar y cargar progreso

- **Guardar:** pulsa **"Guardar progreso"** → se descarga un archivo `progreso_plan_estudios.json`.
- **Cargar:** pulsa **"Cargar progreso"** y selecciona el archivo `.json` previamente guardado.
- Si intentas cerrar la pestaña sin guardar, aparecerá una alerta con las opciones **Guardar y Salir**, **Salir sin Guardar** o **Cancelar**.

> ⚠️ **Recomendación:** guarda tu progreso con frecuencia. La herramienta no almacena datos en servidores.

---

## 📁 Estructura del proyecto

---

## 🗺️ Roadmap (próximas mejoras)

- [ ] Validar que `T + P = Crédito total`.
- [ ] Advertir si un semestre excede un máximo de créditos.
- [ ] Detectar códigos de asignatura duplicados.
- [ ] Vista responsive tipo "tarjeta" para móviles.
- [ ] Botón de **"Ayuda / Manual de uso"** dentro de la app.
- [ ] Escudo institucional en la pantalla de inicio.

> ¿Tienes una idea? Abre un **Issue** 🐛 o envía un **Pull Request** 🚀.

---

## 📄 Licencia

Este proyecto se distribuye bajo la licencia **MIT**.
Consulta el archivo [`LICENSE`](./LICENSE) para más detalles.

> Si la Universidad de Pamplona desea adoptarlo institucionalmente, se recomienda revisar las políticas de uso de imagen y nombre institucional.

---

## 👨‍💻 Autor

**Ing. Andrés Narváez**
Ingeniero mecatrónico
Universidad de Pamplona

- 🌐 GitHub: [@Razor922](https://github.com/Razor922)
- 📦 Repositorio: [Razor922/MYPROYECT](https://github.com/Razor922/MYPROYECT)
- 📧 Contacto: andresbecerra164@gmail.com

---

## 🙏 Agradecimientos

A la **Oficina de Autoevaluación y Acreditación Institucional** de la Universidad de Pamplona por impulsar herramientas que facilitan el trabajo académico y a todos los programas que participen en su validación.

---

<div align="center">

**© 2025 — Ing. Andrés Narváez**
**Universidad de Pamplona**
Hecho con ❤️ para la comunidad académica.

</div>
