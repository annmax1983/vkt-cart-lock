# VKT Cart Lock

[English](../README.md) | [中文](README_zh.md) | [Deutsch](README_de.md) | Español | [日本語](README_ja.md) | [Français](README_fr.md)

**Un candado de reflexión estricto para tu carrito.** Haz clic en pagar y el temporizador empieza. El pago permanece bloqueado hasta que termina el temporizador, y entonces se abre por sí solo.

También conocido como **冷静锁** en chino.

> Chromium · Manifest V3 · 6 idiomas · Sin rastreo · Primero local

---

## ¿Por qué VKT Cart Lock?

La mayoría de las herramientas contra la "compra impulsiva" dejan una puerta abierta: posponer, saltar, desbloquear antes de tiempo. VKT Cart Lock no. La idea es proteger la decisión que ya tomaste de la versión de ti que mira fijamente un botón de pago a medianoche.

- **Sin saltar, sin posponer, sin desbloqueo anticipado.** Desinstalar la extensión es la única forma de evitarlo.
- **El temporizador sigue corriendo fuera de la página.** Cierra la pestaña, reinicia el navegador, vuelve mañana: el candado sigue ahí.
- **El vencimiento es silencioso por defecto.** El pago simplemente vuelve a abrirse. Premium puede añadir una confirmación final.
- **Una compra completada inicia un nuevo candado.** Comprar no reinicia el hábito.
- **Primero local.** Temporizadores, ajustes, mensajes y estadísticas se quedan en tu navegador. Sin analíticas, sin anuncios, el historial de navegación no sale del dispositivo.

---

## Funciones

### Gratis

| Función | Descripción |
|---------|-------------|
| Candado estricto de pago | Se interceptan clics, enlaces de pago, envíos de formularios y páginas de pago |
| 24 ajustes predefinidos + coincidencia genérica | Reglas ajustadas a mano para las grandes tiendas, más alternativas por texto y selectores en el resto |
| Preajustes de enfriamiento | 1 hora, 6 horas, 24 horas o 72 horas |
| Temporizadores por sitio | Un candado activo por sitio, iniciado por el primer clic de pago |
| Mensajes personalizados | Hasta 20 líneas, con visualización fija, rotatoria o aleatoria |
| Tres sonidos | Golpe, campanilla o suave, más un interruptor de silencio |
| Exención de pedidos pequeños | Deja pasar lo esencial por debajo de un importe elegido |
| Lista de permitidos y sitios con bloqueo forzado | Omite una tienda de confianza o fuerza la protección en una pequeña tienda independiente |
| Periodo de calma en rebajas | Black Friday, Prime Day y el Doble 11 extienden automáticamente el enfriamiento a 72 horas |
| Ajustes protegidos por contraseña | Un PIN de 4 a 8 caracteres protege la página de ajustes |
| Etiquetas de emoción | Etiqueta el momento: de madrugada, rebajas, enfadado, aburrido, solo lo quiero |
| Comentarios de bloqueos erróneos | Marca un falso positivo y excluye ese elemento la próxima vez |
| Cuenta atrás en el icono | El icono de la barra muestra las horas o los minutos restantes |
| Libro básico | Total de pagos bloqueados e importe retenido, incluido el mes actual |

### Premium

| Función | Descripción |
|---------|-------------|
| Enfriamientos personalizados | De 10 minutos a 30 días |
| Temporizadores por artículo | Un candado por producto en lugar de por sitio |
| Inicio al añadir al carrito | El temporizador empieza cuando un artículo entra en el carrito |
| Mensajes ilimitados | Limitados solo por el presupuesto de sincronización entre dispositivos (unas 60 líneas) |
| Horas de silencio | Sin sonido durante las horas elegidas; el candado sigue funcionando |
| Confirmar tras el vencimiento | Un último clic de "todavía lo quiero" tras el fin del temporizador |
| Sincronización entre dispositivos | Ajustes y temporizadores siguen tu cuenta de Chrome / Edge |
| Informes de 12 meses | Tendencia mensual, ranking de sitios y desglose de emociones |
| Exportación CSV | Lleva el historial a una hoja de cálculo |
| Copia de seguridad JSON | Exportación e importación completas de ajustes, mensajes, temporizadores y estadísticas |

La activación de Premium es opcional. Todo lo que está por encima de la línea Premium funciona sin cuenta ni clave de licencia.

---

## Cómo funciona

1. **Primer clic en pagar.** La protección intercepta el clic, inicia el temporizador y muestra la pantalla de bloqueo. El pedido no se envía.
2. **Cada intento posterior.** El pago permanece bloqueado y la superposición cuenta atrás el tiempo restante.
3. **El temporizador manda.** Vive en el almacenamiento de la extensión, no en la pestaña. Cerrar la página, reabrir la tienda o reiniciar el navegador no lo acorta.
4. **Cuando se acaba el tiempo.** El candado se libera en silencio y el pago vuelve a estar permitido. Los usuarios Premium pueden exigir antes un clic de confirmación.
5. **Después de una compra.** Un pedido completado inicia un nuevo enfriamiento, de modo que la siguiente compra pasa por la misma pausa.

La protección solo funciona en la página. Nunca engancha peticiones de red y nunca toca iframes de pago ni páginas de proveedores de pago (Stripe, PayPal, Adyen, checkout.com, Braintree y hosts similares están excluidos).

---

## Instalación

1. Abre `chrome://extensions/` en Chrome o `edge://extensions/` en Edge.
2. Activa el **modo de desarrollador**.
3. Haz clic en **Cargar descomprimida** y selecciona esta carpeta.
4. Ancla la extensión a la barra de herramientas.

Para una compilación empaquetada, usa el zip de `publish/` o carga la carpeta manualmente durante el desarrollo.

---

## Uso

- **Configura un enfriamiento.** Abre las opciones de la extensión y elige un preajuste, o una duración personalizada con Premium.
- **Escribe tu propia frase.** La pantalla de bloqueo puede mostrar tus palabras en lugar de las citas integradas. El modo rotatorio evita que se convierta en papel pintado.
- **Añade reglas.** Pon un supermercado en la lista de permitidos, fuerza el candado en una tienda pequeña o exime pedidos por debajo de un importe.
- **Mira el icono.** La cuenta atrás de la barra es el recordatorio silencioso de que el candado sigue activo.
- **Revisa el libro.** El panel muestra qué se bloqueó, cuánto habría costado, qué sitios y estados de ánimo provocan más pagos, y una tendencia de 12 meses.
- **Haz copia de seguridad (Premium).** Usa la exportación JSON antes de cambiar de equipo. La sincronización restaura ajustes y temporizadores, pero las estadísticas locales no viajan.

Desinstalar la extensión borra sus datos locales. Si la sincronización Premium está activada, los mensajes y los ajustes vuelven tras reinstalar; las estadísticas y el historial local, no.

---

## Sitios compatibles

Los preajustes ajustados a mano cubren 24 tiendas, entre ellas Amazon, eBay, Etsy, Walmart, Target, Best Buy, Home Depot, Lowe's, Newegg, Wayfair, Mercari, AliExpress, Temu, Alibaba, DHgate, Shopee, Lazada, Rakuten, SHEIN, TikTok Shop, bol.com, Allegro, Otto y Cdiscount.

Cualquier otra tienda queda cubierta por la coincidencia genérica de textos y selectores de botones de pago. Si un sitio cambia su marcado, la nota de autocomprobación del menú emergente te dice que la protección quizá necesite otra revisión.

---

## Navegadores compatibles

| Navegador | Estado |
|---------|--------|
| Google Chrome | Totalmente compatible |
| Microsoft Edge | Totalmente compatible |
| Otros navegadores basados en Chromium | Debería funcionar |

---

## Datos y privacidad

- **Almacenado localmente:** ajustes, temporizadores, estadísticas, notas de autocomprobación, el PIN opcional de ajustes (solo hash SHA-256 con sal) y el registro de licencia Premium.
- **Sincronizado (Premium, opcional):** ajustes, mensajes personalizados y registros ligeros de temporizadores mediante `chrome.storage.sync`. El PIN de ajustes nunca se sincroniza.
- **Enviado al servidor de licencias:** solo al activar, validar o desactivar Premium: la clave de licencia, un ID de instalación aleatorio, el ID del plugin y metadatos básicos del navegador (versión, idioma, zona horaria, agente de usuario).
- **No se recopila:** contenido de páginas, historial de navegación, contenido del carrito, datos de pago, pulsaciones ni analíticas.

No hay cuenta, ni publicidad, ni venta de datos. Desinstalar la extensión elimina los datos locales; los registros de licencia del servidor pueden eliminarse desactivando antes la licencia.

Consulta la política completa en [privacy-policy.html](../privacy-policy.html).

---

## Permisos

| Permiso | Por qué es necesario |
|------------|------------------|
| `storage` | Guardar ajustes, temporizadores y estadísticas localmente; sincronizarlos para Premium |
| `alarms` | Mantener precisa la cuenta atrás y liberar los candados a tiempo |
| `notifications` | Mostrar un aviso local de escritorio cuando empieza un candado nuevo |
| `host_permissions: <all_urls>` | Detectar un botón de pago en cualquier tienda, ya que usan dominios arbitrarios |
| `host_permissions: api.annmax1983.com` | Activar y validar una licencia Premium opcional |

El script de contenido se ejecuta en todos los marcos para captar botones de pago dentro de los widgets de las tiendas, pero los hosts de proveedores de pago quedan explícitamente excluidos.

---

## Idiomas

English, 简体中文, 日本語, Deutsch, Español y Français. La interfaz, las citas integradas y las descripciones de tiendas están localizadas.

---

## Licencia

VKT Cart Lock es una extensión comercial. El nivel Gratis se puede usar sin licencia. Las funciones Premium requieren una clave de licencia activa de [annmax1983.com](https://www.annmax1983.com/).
