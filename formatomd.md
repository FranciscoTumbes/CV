---
title: Editor Profesional de Curriculum Vitae
version: 1.0
language: es
framework: HTML + CSS + JavaScript
architecture: SPA
purpose: Editor interactivo de Curriculum Vitae
author: Francisco Sanjinez Calderón
---

# Proyecto

## Objetivo

Aplicación web desarrollada completamente en HTML, CSS y JavaScript para crear,
editar y exportar un Curriculum Vitae profesional en formato PDF.

No requiere servidor.

---

# Arquitectura

## Tecnologías

- HTML5
- CSS3
- JavaScript ES6
- html2pdf.js

---

# Componentes principales

## Panel lateral

Responsabilidades:

- Editar información personal
- Administrar experiencias laborales
- Administrar educación
- Administrar habilidades
- Administrar idiomas
- Importar CSV
- Exportar CSV
- Descargar PDF

Elementos HTML relevantes

- #panel
- .panel-header
- .panel-body
- .panel-footer

---

## Documento CV

Contenedor:

#cv

Contiene:

- Portada
- Perfil Profesional
- Datos Personales
- Experiencia
- Educación
- Cursos
- Habilidades
- Idiomas
- Reconocimientos
- Referencias

---

# Modelo de Datos

## experience

```javascript
{
 role,
 org,
 period,
 desc,
 tags
}
```

---

## education

```javascript
{
 degree,
 institution,
 year,
 detail,
 icon
}
```

---

## courses

```javascript
{
 date,
 name,
 org,
 area
}
```

---

## recognitions

```javascript
{
 date,
 title,
 org
}
```

---

## references

```javascript
{
 name,
 role
}
```

---

# Funciones JavaScript

## render()

Responsabilidad

Actualizar completamente el CV cuando cambia cualquier dato.

Entrada

Todos los campos del formulario.

Salida

HTML actualizado.

---

## addExp()

Agrega una experiencia laboral.

Entrada

Formulario de experiencia.

Salida

Nuevo elemento en experiences[].

---

## deleteExp(index)

Elimina una experiencia.

---

## addEdu()

Agrega un estudio.

---

## deleteEdu(index)

Elimina un estudio.

---

## downloadCSV()

Exporta datos a CSV.

---

## importCSV()

Importa datos desde CSV.

---

## downloadPDF()

Convierte el CV en PDF mediante html2pdf.js.

---

# Flujo General

Usuario

↓

Edita información

↓

render()

↓

Actualiza HTML

↓

Visualización del CV

↓

Exportar PDF

---

# Dependencias

html2pdf.bundle.min.js

Utilizada para:

- generar PDF
- conservar estilos
- exportar varias páginas

---

# Diseño

Tema

Elegante

Colores

- Dorado
- Gris oscuro
- Beige

Tipografías

- Playfair Display
- DM Sans
- DM Mono

---

# Responsive

Incluye tres tamaños

Desktop

Tablet

Mobile

---

# Objetos Globales

experiences[]

educations[]

courses[]

recognitions[]

references[]

---

# Convenciones

Cada sección posee:

- editor
- modelo de datos
- renderizador

Todas las modificaciones llaman a

render()

---

# Mejoras futuras

- Guardado automático
- Base de datos SQLite
- Exportación DOCX
- Exportación Markdown
- Integración con GitHub
- Integración con IA
- Plantillas múltiples
- Historial de cambios
- Fotos del usuario
- Firma digital

---

# Resumen para IA

Tipo:

Editor de Curriculum Vitae

Arquitectura:

SPA

Frontend:

HTML CSS JavaScript

Persistencia:

Memoria del navegador

Exportación:

PDF
CSV

Dominio:

Recursos Humanos

Nivel de complejidad:

Alto

Patrón:

Manipulación del DOM

Estado:

Proyecto funcional listo para ampliaciones