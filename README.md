# 📡 n8n Workflow: Búsqueda de Posts por Palabras Clave

Este flujo de trabajo de **n8n** permite buscar publicaciones (posts) de un usuario específico en la API pública [JSONPlaceholder](https://jsonplaceholder.typicode.com/), filtrarlas dinámicamente por palabras clave y enviar un email si se encuentran coincidencias. Está diseñado para aprender y aplicar conceptos esenciales de automatización con n8n.

---

## 🔧 Tecnologías

- [n8n](https://n8n.io/) (Low-code automation platform)
- API pública de [JSONPlaceholder](https://jsonplaceholder.typicode.com/)
- Node `Webhook`, `HTTP Request`, `Function`, `IF`, `Send Email`, `Console`

---

## 🚀 ¿Cómo funciona?

1. **Webhook**  
   El flujo comienza cuando se hace una solicitud `POST` a la ruta `/webhook/buscar-posts`, con un JSON como este:

   ```json
   {
     "userId": 1,
     "keywords": ["sunt", "qui", "et"]
   }
