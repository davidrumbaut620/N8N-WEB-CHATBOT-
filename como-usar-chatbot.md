# Guía de Implementación del Chatbot

Esta guía explica cómo implementar fácilmente el chatbot en tu sitio web.

## Requisitos previos

- Un webhook de n8n configurado para tu chatbot
- Un servidor web para alojar tu sitio

## Pasos para la implementación

### 1. Incluye los archivos necesarios

Añade los siguientes elementos en la sección `<head>` de tu HTML:

```html
<link href="chatbot.css" rel="stylesheet" />
<script type="module">
    import { createChat } from 'chatbot.js';

    createChat({
        webhookUrl: 'TU_URL_DE_WEBHOOK_AQUÍ',
        showWindowCloseButton: true
    });
</script>
```

### 2. Personaliza la URL del webhook

Lo único que necesitas cambiar es la URL del webhook por la de tu propio chatbot:

```javascript
webhookUrl: 'TU_URL_DE_WEBHOOK_AQUÍ'
```

Por ejemplo:
```javascript
webhookUrl: 'https://n8n-production-b68b.up.railway.app/webhook/tu-id-único/chat'
```

### 3. Opciones adicionales

Puedes personalizar el comportamiento del chatbot con estas opciones:

| Opción | Descripción | Valor predeterminado |
|--------|-------------|---------------------|
| `showWindowCloseButton` | Muestra u oculta el botón de cerrar | `true` |
| `mode` | Modo de visualización (`"window"` o `"fullscreen"`) | `"window"` |
| `title` | Título del chatbot | `"Chat"` |

## Ejemplo completo

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mi Sitio con Chatbot</title>
    <link href="chatbot.css" rel="stylesheet" />
    <script type="module">
        import { createChat } from 'chatbot.js';

        createChat({
            webhookUrl: 'https://n8n-production-b68b.up.railway.app/webhook/tu-id-único/chat',
            showWindowCloseButton: true
        });
    </script>
</head>
<body>
    <h1>Bienvenido a mi sitio</h1>
    <p>El chatbot aparecerá automáticamente en la esquina inferior derecha.</p>
</body>
</html>
```

## Solución de problemas

- Asegúrate de que los archivos `chatbot.js` y `chatbot.css` estén correctamente referenciados
- Verifica que la URL del webhook sea válida y esté activa
- Comprueba la consola del navegador para ver posibles errores

---

¡Y eso es todo! Con estos simples pasos, tendrás tu chatbot funcionando en tu sitio web.
