---
layout: default
title: Anuncios
---

> **Idiomas:** [English](./ads) · [Türkçe](./ads-tr) · **Español**

# Anuncios en Sudoku Arena Online

Sudoku Arena Online es gratuito. El trabajo detrás del generador de
puzles, el emparejamiento multijugador y el desafío diario se apoya
en publicidad. Esta página explica exactamente qué anuncios mostramos,
dónde aparecen y cómo los configuramos — en lenguaje claro, para que
pueda decidir con qué se siente cómodo antes de jugar.

Para la imagen completa de recopilación de datos, vea la
[Política de Privacidad](./privacy-policy-es). Para el lado
contractual, vea los [Términos del Servicio](./terms-of-service-es).

---

## Quién sirve los anuncios

Usamos **Google AdMob**, operado por Google LLC. Cada anuncio que ve
dentro de Sudoku Arena Online se entrega a través de la red de AdMob.
No incorporamos ningún otro SDK de publicidad — sin Meta Audience
Network, sin Unity Ads, sin IronSource, sin anuncios en webview
dentro de la app de ningún tipo.

Políticas de AdMob y cómo Google usa la información que recopila en
nuestro nombre:

- [Cómo Google utiliza la información de los sitios o apps que usan nuestros servicios](https://policies.google.com/technologies/partner-sites)
- [Prácticas de privacidad de Google AdMob y AdSense](https://support.google.com/admob/answer/6128543)

---

## Dónde aparecen los anuncios

Hay cuatro posibles ubicaciones de anuncios en la app. Si cada una
está activa lo controla un valor de configuración en tiempo de
ejecución (Firebase Remote Config) que podemos ajustar sin publicar
una nueva versión. En el lanzamiento entregamos la configuración más
conservadora posible — solo la ubicación recompensada está activa.

| Ubicación | Cuándo | Por defecto al lanzar |
|---|---|---|
| **Recompensado — "Ver anuncio por una pista extra"** | Tras gastar su pista gratuita, aparece un icono play opcional en el botón de pista. Tocarlo carga un breve vídeo recompensado; al completarlo recibe una pista adicional. Rechazar o cerrar el anuncio no hace nada. | **Activo** (solo iniciado por el usuario) |
| **Banner — Inicio y pantalla de resultado** | Un pequeño banner en la parte inferior de la pantalla de inicio y del modal de fin de partida. Nunca tapa el tablero ni ninguna UI tocable. | **Inactivo** al lanzar |
| **Banner — Dentro del juego** | Un pequeño banner debajo del teclado numérico mientras juega. Misma ubicación cuidadosa — nunca sobre el tablero. | **Inactivo** al lanzar |
| **Interstitial — Inicio de partida** | Un anuncio a pantalla completa antes de que comience una partida multijugador, con botón Cerrar visible. Como mucho una vez por partida. | **Inactivo** al lanzar |

Una actualización Pro sin anuncios está planificada para un
lanzamiento futuro; los detalles se confirmarán cuando salga.

---

## Qué información recibe AdMob

Hemos configurado AdMob para solicitar únicamente **anuncios no
personalizados** (`npa=1`). En la práctica eso significa:

- A AdMob se le indica que **no** use ningún identificador en su
  dispositivo para construir o actualizar un perfil de usted.
- Los anuncios que ve se eligen en base a señales contextuales — el
  tipo de app (juego de puzles), el país derivado de su dirección IP
  y el idioma del dispositivo. No en base a su comportamiento
  pasado.
- **No** mostramos el aviso de App Tracking Transparency de Apple
  porque la app no habilita rastreo entre apps. El aviso ATT es para
  apps que sí lo hacen.

AdMob sigue usando el identificador publicitario de su plataforma
(**Apple IDFA** en iOS o **Google AAID** en Android) para
**detección de fraude** y para el marco de atribución
[SKAdNetwork](https://developer.apple.com/documentation/storekit/skadnetwork)
de Apple. Este uso está atado a política — Google no puede usar
estos identificadores para anunciarle en otro lugar.

Puede:

- **iOS**: Ajustes → Privacidad y Seguridad → Publicidad de Apple →
  desactivar *Anuncios personalizados*, o restablecer su IDFA desde
  la misma pantalla.
- **Android**: Ajustes → Google → Anuncios → activar *Excluirse de
  la personalización de anuncios* y restablecer su ID Publicitario.

Cuando el rastreo publicitario está limitado, AdMob sigue sirviendo
anuncios no personalizados en la app — no pierde funcionalidad.

---

## Qué información vemos nosotros (el desarrollador)

El único dato relacionado con anuncios que recibimos de AdMob es el
**ingreso e impresiones agregadas** en la consola de AdMob — totales
como "X impresiones ayer, Y CPM, Z USD de ingreso", por ubicación,
por país. Nunca vemos nada sobre usted como individuo: ni los
anuncios que vio, ni si los tocó, ni a qué hora del día jugó.

---

## Cómo contactarnos

Si algo en esta página no está claro, o ha visto un anuncio que
parecía inadecuado para nuestra clasificación 4+, por favor escriba
a **nfvwzhbrbw@privaterelay.appleid.com** con una captura de
pantalla. AdMob nos permite bloquear anunciantes específicos por
categoría, y usamos esto regularmente para mantener la experiencia
limpia.

---

## Cambios en esta página

Los cambios materiales en la configuración de anuncios (por ejemplo,
añadir un nuevo SDK publicitario o activar una ubicación que
anteriormente estaba inactiva) se reflejarán primero aquí. La
[Política de Privacidad](./privacy-policy-es) se actualizará al mismo
tiempo, con la fecha de "Última actualización" arriba para que pueda
saber cuándo cambió algo.

Última actualización: 16 de mayo de 2026
