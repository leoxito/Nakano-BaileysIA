# 🌸 Las Quintillizas - Bot de WhatsApp (BaileysV6)

<div align="center">
  
![Banner](https://qu.ax/VhZMq.jpg)

[![GitHub Stars](https://img.shields.io/github/stars/tu-usuario/quintillizas-bot?style=social)](https://github.com/tu-usuario/quintillizas-bot)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Baileys](https://img.shields.io/badge/Baileys-V6-green.svg)](https://github.com/WhiskeySockets/Baileys)
[![Node.js](https://img.shields.io/badge/Node.js-18+-green.svg)](https://nodejs.org/)
[![WhatsApp](https://img.shields.io/badge/WhatsApp-Compatible-25D366.svg)](https://www.whatsapp.com/)

### *Bot Avanzado de WhatsApp con Soporte Completo para Botones e Imágenes*

[Características](#-características) • [Instalación](#-instalación) • [Uso](#-uso) • [Comandos](#-comandos) • [Contribuir](#-contribuir)

</div>

---

## 📋 Descripción

**Las Quintillizas Bot** es un bot de WhatsApp de última generación construido con **Baileys V6**, la biblioteca más actualizada y estable para WhatsApp Web. Este bot está optimizado para las últimas actualizaciones de WhatsApp y ofrece una experiencia fluida con soporte completo para botones interactivos, imágenes, listas y mucho más.

## ✨ Características Destacadas

### 🎯 Soporte Completo de Botones Interactivos
- ✅ Botones de respuesta rápida
- ✅ Botones con imágenes incorporadas
- ✅ Botones de llamada a la acción
- ✅ Listas interactivas con múltiples secciones
- ✅ Botones de URL externos

### 🖼️ Sistema Avanzado de Imágenes
- 📸 Envío de imágenes con botones
- 🎨 Imágenes en mensajes de lista
- 🖼️ Soporte para múltiples formatos (JPG, PNG, WEBP)
- 📦 Compresión automática de imágenes
- 🔗 Soporte para imágenes desde URL

### ⚡ Arquitectura Fluida y Optimizada
- 🚀 Respuestas instantáneas
- 💾 Sistema de caché inteligente
- 🔄 Reconexión automática
- 🛡️ Anti-crash con recuperación automática
- 📊 Manejo eficiente de memoria

### 🔮 Compatible con Futuras Actualizaciones
- 🆕 Soporte para las últimas versiones de WhatsApp
- 🔄 Actualización automática de protocolos
- 📱 Multi-dispositivo nativo
- 🔐 Autenticación segura con QR

## 🚀 Instalación

### Requisitos Previos

Asegúrate de tener instalado:

```bash
Node.js: v18.x o superior
NPM: v9.x o superior (incluido con Node.js)
Git: Para clonar el repositorio
```

### Instalación Rápida

```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/quintillizas-bot.git

# 2. Entrar al directorio
cd quintillizas-bot

# 3. Instalar dependencias
npm install

# 4. Configurar el bot
cp config.example.json config.json
nano config.json  # O usa tu editor favorito

# 5. Iniciar el bot
npm start
```

### Instalación Detallada

<details>
<summary>👉 Click para ver instalación paso a paso</summary>

#### 1. Clonar el Repositorio
```bash
git clone https://github.com/tu-usuario/quintillizas-bot.git
cd quintillizas-bot
```

#### 2. Instalar Dependencias
```bash
npm install
```

#### 3. Configuración Inicial
Crea tu archivo de configuración:
```bash
cp config.example.json config.json
```

Edita `config.json` con tus preferencias:
```json
{
  "ownerNumber": "521234567890",
  "botName": "Las Quintillizas Bot",
  "prefix": ".",
  "language": "es",
  "autoRead": true,
  "autoTyping": false
}
```

#### 4. Iniciar el Bot
```bash
npm start
```

#### 5. Escanear Código QR
Escanea el código QR que aparece en la terminal con tu WhatsApp:
- Abre WhatsApp en tu teléfono
- Ve a **Configuración** > **Dispositivos Vinculados**
- Toca en **Vincular un Dispositivo**
- Escanea el código QR

</details>

## 📱 Uso

### Comandos Básicos

```bash
# Iniciar el bot
npm start

# Modo desarrollo (auto-reinicio)
npm run dev

# Ver logs
npm run logs

# Limpiar sesión
npm run clean
```

### Ejemplo de Uso con Botones

```javascript
// Enviar mensaje con botones e imagen
await sock.sendMessage(chatId, {
  image: { url: 'https://example.com/image.jpg' },
  caption: '¡Elige una opción!',
  footer: 'Las Quintillizas Bot',
  buttons: [
    { buttonId: 'opcion1', buttonText: { displayText: '✅ Opción 1' }, type: 1 },
    { buttonId: 'opcion2', buttonText: { displayText: '❌ Opción 2' }, type: 1 }
  ],
  headerType: 4
});
```

### Ejemplo con Listas Interactivas

```javascript
// Enviar lista con imagen
await sock.sendMessage(chatId, {
  text: 'Selecciona del menú:',
  footer: 'Las Quintillizas Bot',
  title: '📋 Menú Principal',
  buttonText: 'Ver opciones',
  sections: [
    {
      title: '🎮 Diversión',
      rows: [
        { title: 'Memes', description: 'Obtén memes divertidos', rowId: 'memes' },
        { title: 'Juegos', description: 'Juega con el bot', rowId: 'games' }
      ]
    },
    {
      title: '🛠️ Utilidades',
      rows: [
        { title: 'Stickers', description: 'Crea stickers', rowId: 'sticker' },
        { title: 'Descargas', description: 'Descarga contenido', rowId: 'download' }
      ]
    }
  ]
});
```

## 🎮 Comandos del Bot

### Comandos Generales
| Comando | Descripción | Uso |
|---------|-------------|-----|
| `.menu` | Muestra el menú principal con botones | `.menu` |
| `.help` | Ayuda detallada | `.help [comando]` |
| `.info` | Información del bot | `.info` |
| `.ping` | Verifica la latencia | `.ping` |

### Comandos de Diversión
| Comando | Descripción | Uso |
|---------|-------------|-----|
| `.meme` | Genera un meme aleatorio | `.meme` |
| `.waifu` | Imagen anime aleatoria | `.waifu` |
| `.quote` | Frase motivacional | `.quote` |

### Comandos de Utilidad
| Comando | Descripción | Uso |
|---------|-------------|-----|
| `.sticker` | Crea sticker de imagen/video | `.sticker [responde a imagen]` |
| `.toimg` | Convierte sticker a imagen | `.toimg [responde a sticker]` |
| `.clima` | Información del clima | `.clima [ciudad]` |

### Comandos de Descargas
| Comando | Descripción | Uso |
|---------|-------------|-----|
| `.ytmp3` | Descarga audio de YouTube | `.ytmp3 [url]` |
| `.ytmp4` | Descarga video de YouTube | `.ytmp4 [url]` |
| `.tiktok` | Descarga videos de TikTok | `.tiktok [url]` |
| `.instagram` | Descarga de Instagram | `.instagram [url]` |

### Comandos de Administración (Solo Owner)
| Comando | Descripción | Uso |
|---------|-------------|-----|
| `.broadcast` | Mensaje a todos los chats | `.broadcast [mensaje]` |
| `.join` | Unirse a grupo | `.join [link]` |
| `.leave` | Salir del grupo | `.leave` |
| `.ban` | Banear usuario | `.ban [@usuario]` |

## 🔧 Configuración Avanzada

### Archivo config.json

```json
{
  "ownerNumber": "521234567890",
  "botName": "Las Quintillizas Bot",
  "prefix": ".",
  "language": "es",
  "autoRead": true,
  "autoTyping": false,
  "maxButtons": 3,
  "maxListSections": 10,
  "imageQuality": 80,
  "antiSpam": {
    "enabled": true,
    "maxMessages": 5,
    "timeWindow": 10000
  },
  "groups": {
    "antiLink": true,
    "welcome": true,
    "goodbye": true
  }
}
```

## 🎨 Personalización

### Agregar Comandos Personalizados

Crea un archivo en `plugins/tucomando.js`:

```javascript
export default {
  name: 'micomando',
  aliases: ['mc', 'comando'],
  category: 'general',
  description: 'Descripción de tu comando',
  
  async execute(sock, msg, args) {
    // Tu código aquí
    await sock.sendMessage(msg.key.remoteJid, {
      text: '¡Hola desde mi comando!',
      buttons: [
        { buttonId: 'btn1', buttonText: { displayText: '👍 Me gusta' }, type: 1 }
      ],
      footer: 'Las Quintillizas Bot'
    });
  }
};
```

### Personalizar Botones

```javascript
// Botones con imágenes
const buttons = [
  {
    buttonId: 'id1',
    buttonText: { displayText: '✅ Aceptar' },
    type: 1
  },
  {
    buttonId: 'id2',
    buttonText: { displayText: '❌ Cancelar' },
    type: 1
  }
];

await sock.sendMessage(chatId, {
  image: { url: './media/banner.jpg' },
  caption: 'Mensaje con imagen y botones',
  footer: 'Pie de página',
  buttons: buttons,
  headerType: 4
});
```

## 🛠️ Solución de Problemas

### Problema: El bot no responde a comandos
**Solución:**
- Verifica que el prefijo sea correcto en `config.json`
- Asegúrate de que el bot no esté en modo de solo lectura
- Revisa los logs con `npm run logs`

### Problema: Los botones no aparecen
**Solución:**
- Actualiza Baileys: `npm update @whiskeysockets/baileys`
- Verifica que tu versión de WhatsApp sea la más reciente
- Algunos dispositivos antiguos no soportan botones

### Problema: Errores de conexión
**Solución:**
```bash
# Limpiar sesión y reconectar
npm run clean
npm start
```

### Problema: Las imágenes no se envían
**Solución:**
- Verifica que la URL de la imagen sea accesible
- Comprueba el formato de imagen (JPG, PNG, WEBP)
- Reduce el tamaño de la imagen si es muy grande

## 🔄 Actualizaciones

### Mantener el Bot Actualizado

```bash
# Actualizar a la última versión
git pull origin main
npm install
npm start
```

### Changelog

#### v2.0.0 (Actual)
- ✅ Soporte completo para Baileys V6
- ✅ Botones interactivos con imágenes
- ✅ Listas mejoradas
- ✅ Sistema anti-crash optimizado
- ✅ Compatibilidad con últimas actualizaciones de WhatsApp

#### v1.5.0
- Mejoras en estabilidad
- Nuevos comandos de descarga
- Corrección de bugs

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Si quieres mejorar el bot:

1. **Fork** el repositorio
2. Crea una **rama** para tu función (`git checkout -b feature/nuevaFuncion`)
3. **Commit** tus cambios (`git commit -m 'Añadir nueva función'`)
4. **Push** a la rama (`git push origin feature/nuevaFuncion`)
5. Abre un **Pull Request**

### Guías de Contribución

- Mantén el código limpio y comentado
- Sigue el estilo de código existente
- Actualiza la documentación si es necesario
- Prueba tus cambios antes de enviarlos

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - mira el archivo [LICENSE](LICENSE) para más detalles.

## 👥 Autores

- **Tu Nombre** - *Trabajo Inicial* - [@tu-usuario](https://github.com/tu-usuario)

## 🌟 Agradecimientos

- [Baileys](https://github.com/WhiskeySockets/Baileys) - Por la increíble biblioteca
- Comunidad de desarrolladores de bots de WhatsApp
- Todos los contribuidores del proyecto

## 📞 Soporte

¿Necesitas ayuda? Aquí hay algunas opciones:

- 📧 Email: soporte@tudominio.com
- 💬 [Grupo de WhatsApp](https://chat.whatsapp.com/tu-grupo)
- 🐛 [Reportar un bug](https://github.com/tu-usuario/quintillizas-bot/issues)
- 💡 [Sugerir una función](https://github.com/tu-usuario/quintillizas-bot/issues)

## ⭐ Dale una Estrella

Si este proyecto te fue útil, ¡considera darle una estrella en GitHub! ⭐

---

<div align="center">

**[⬆ Volver arriba](#-las-quintillizas---bot-de-whatsapp-baileysv6)**

Hecho con ❤️ por [Tu Nombre](https://github.com/tu-usuario)

</div>