---
layout: default
title: Política de Privacidad
---

> **Idiomas:** [English](./privacy-policy) · [Türkçe](./privacy-policy-tr) · **Español**

# Política de Privacidad

**Fecha de entrada en vigor:** 16 de mayo de 2026
**Última actualización:** 16 de mayo de 2026

Esta Política de Privacidad explica cómo **Sudoku Arena Online** ("la
App", "nosotros") recopila, utiliza y protege la información cuando
usa nuestra aplicación móvil. La App es operada por **Murat Kul** ("el
desarrollador"), con sede en Estambul, Türkiye.

Al usar la App acepta las prácticas descritas a continuación. Si no
está de acuerdo, por favor no use la App.

---

## 1. Quiénes somos

| | |
|---|---|
| Nombre de la App | Sudoku Arena Online |
| Desarrollador | Murat Kul |
| País | Türkiye |
| Contacto | nfvwzhbrbw@privaterelay.appleid.com |

Este es un proyecto independiente. Los proveedores de infraestructura
listados en la sección 4 (Firebase / Google AdMob) son los únicos
terceros que procesan datos en nuestro nombre.

---

## 2. Qué recopilamos

Recopilamos únicamente lo necesario para que la App funcione y para
servir anuncios no personalizados. **No** recopilamos contactos,
fotos, ubicación, datos de salud ni datos financieros.

### 2.1 Datos de cuenta

Cuando inicia sesión con **Google** o **Apple** recibimos lo siguiente
del proveedor de identidad:

- Un identificador único de usuario (Firebase UID)
- Nombre visible
- Dirección de correo electrónico (Apple puede devolver una dirección
  de Private Relay)
- URL de la foto de perfil (una referencia, no los bytes de la imagen)

Si elige **Continuar como invitado**, solo generamos un Firebase UID
anónimo. No se recopila nombre, correo ni foto.

### 2.2 Datos de juego

Para ejecutar el servicio multijugador almacenamos en Firestore:

- Partidas activas en las que participa: puzle, estado, jugadores,
  errores, número de celdas rellenadas, tiempo de finalización, UID
  ganador
- Ticket de emparejamiento mientras busca un rival: su UID, nombre
  visible, URL de foto, modo, dificultad, marca de tiempo
- Una referencia a su partida activa (`currentMatchId`) en su
  documento de usuario

### 2.3 Datos en el dispositivo

Lo siguiente permanece solo en su dispositivo y nunca se envía a
nuestros servidores:

- Su sesión de un jugador guardada ("Continuar") y los ajustes de
  juego, en la base de datos local Hive
- Tema, idioma, vibración y otras preferencias, en
  SharedPreferences

### 2.4 Datos publicitarios

La App utiliza Google AdMob para servir anuncios. AdMob puede
recopilar o procesar lo siguiente en nuestro nombre:

- **Identificador Publicitario de Apple (IDFA)** en iOS — AdMob lo
  utiliza para prevenir fraude publicitario y atribuir instalaciones
  mediante el marco SKAdNetwork de Apple. Solicitamos únicamente
  **anuncios no personalizados** (`npa=1`), lo que significa que
  AdMob **no** utiliza el IDFA para construir un perfil publicitario
  de usted. No mostramos el aviso de App Tracking Transparency porque
  no habilitamos el rastreo entre apps.
- **Google Advertising ID (AAID)** en Android — papel equivalente al
  IDFA, con la misma configuración no personalizada.
- **Señales generales** que AdMob necesita para cumplir con COPPA /
  GDPR / IAB TCF (p. ej. país, modelo de dispositivo, versión del SO,
  dirección IP usada solo para derivar el país). Estas son procesadas
  por Google y nunca llegan a nosotros como desarrolladores.
- **Señales de recompensa** cuando elige ver un anuncio recompensado
  a cambio de una pista extra — limitadas a "¿el usuario completó la
  visualización?", nunca el contenido del anuncio.

Puede desactivar el rastreo publicitario en iOS (Ajustes → Privacidad
y Seguridad → Publicidad de Apple) o restablecer su ID Publicitario
en Android (Ajustes → Google → Anuncios). Cuando el rastreo está
limitado, AdMob sigue sirviendo anuncios no personalizados con
señales de detección de fraude reducidas.

---

## 3. Por qué lo recopilamos

| Finalidad | Datos utilizados |
|---|---|
| Iniciar sesión e identificar sus partidas | Datos de cuenta |
| Emparejarle con otro jugador | Ticket de emparejamiento, datos de cuenta |
| Ejecutar una partida y permitir que su rival vea su progreso | Datos de juego |
| Mostrar su tarjeta "Continuar" en la pantalla de inicio | Datos en el dispositivo |
| Servir anuncios no personalizados + comprobar fraude | Datos publicitarios |
| Atribuir instalaciones mediante SKAdNetwork de Apple | Datos publicitarios |
| Diagnosticar y corregir fallos | Datos de diagnóstico de fallos (Crashlytics) |

No vendemos sus datos personales ni creamos un perfil de marketing a
partir de ellos. Los identificadores publicitarios listados en la
sección 2.4 se utilizan **únicamente para anuncios no personalizados
y detección de fraude**; no hemos habilitado ningún SDK de rastreo,
SDK de atribución ni función de segmentación de audiencias.

---

## 4. Servicios de terceros

La App utiliza **Firebase**, operado por Google LLC, como backend:

- **Firebase Authentication** — gestiona el inicio de sesión con
  Google, Apple o modo anónimo.
- **Cloud Firestore** — almacena documentos de partida y registros de
  usuario.
- **Firebase Remote Config** — obtiene configuración en tiempo de
  ejecución (tiempos de emparejamiento, flags de ubicación de
  anuncios, etc.). No se envía dato personal — solo un identificador
  genérico de instalación para que Google entregue el payload de
  configuración correcto.
- **Firebase Crashlytics** — registra diagnósticos de fallos no
  personalizados, enviados solo cuando la App falla.
- **Google Sign-In** y **Sign in with Apple** — proveedores federados
  de identidad.

La App también incorpora **Google AdMob** (operado por Google LLC)
para servir anuncios. Vea la sección 2.4 para saber qué recopila AdMob
y cómo está configurado.

Estos servicios actúan como **encargados del tratamiento** en nuestro
nombre. No son propietarios de sus datos. Sus prácticas de privacidad
están descritas en:

- [Política de Privacidad de Google](https://policies.google.com/privacy)
- [Cómo Google utiliza la información de los sitios o apps que usan nuestros servicios](https://policies.google.com/technologies/partner-sites)
- [Política de Privacidad de Apple](https://www.apple.com/legal/privacy/)

La lista de servicios de terceros puede cambiar en futuras versiones;
la sección 11 cubre cómo comunicamos esas actualizaciones.

---

## 5. Ubicación y seguridad de los datos

Los datos se almacenan en regiones de Google Cloud utilizadas por
Firebase (típicamente `us-central1` u otra región seleccionada por
Firebase). Todo el tráfico entre la App y Firebase usa cifrado TLS.
Firestore cifra los datos en reposo por defecto.

---

## 6. Retención

Conservamos sus datos solo mientras su cuenta esté activa:

- **Registro de cuenta** (`users/{uid}`) — hasta que elimine su
  cuenta.
- **Ticket de emparejamiento** — eliminado en 30 segundos (tiempo de
  espera) o inmediatamente cuando se encuentra una partida / cancela.
- **Documentos de partida** — conservados indefinidamente para que
  ambos participantes puedan ver su historial. No contienen
  información más allá de UID, nombre visible y las métricas listadas
  en la sección 2.2.
- **Datos en el dispositivo** — hasta que desinstale la App.

---

## 7. Sus derechos

Si está en el Espacio Económico Europeo, Reino Unido o España bajo el
RGPD/LOPDGDD, tiene derecho a:

- Acceder a los datos personales que tenemos sobre usted
- Corregir datos inexactos
- Eliminar sus datos ("derecho al olvido")
- Exportar sus datos en un formato portable
- Oponerse o restringir el tratamiento
- Presentar una reclamación ante su autoridad local de protección de
  datos (en España, la Agencia Española de Protección de Datos)

Para ejercer cualquiera de estos derechos, escriba a
**nfvwzhbrbw@privaterelay.appleid.com**. Respondemos en un plazo de
30 días.

---

## 8. Eliminación de cuenta

Puede eliminar su cuenta en cualquier momento desde dentro de la App:

> **Ajustes → Eliminar cuenta**

Esto:

1. Le reautenticará con su proveedor de inicio de sesión
   (comprobación de seguridad).
2. Eliminará permanentemente su registro de usuario y cualquier
   ticket de emparejamiento pendiente de Firestore.
3. Eliminará permanentemente su usuario de Firebase Authentication.
4. Cerrará su sesión.

Tras la eliminación, su UID puede seguir apareciendo dentro de los
documentos de partida históricos en los que participó, junto con el
nombre visible y la URL de foto que eran visibles para su rival
durante el juego. Esos documentos de partida no son personalmente
identificables por sí mismos.

Si no puede acceder a la opción en la app por cualquier motivo,
escríbanos a **nfvwzhbrbw@privaterelay.appleid.com** y eliminaremos
su cuenta manualmente en un plazo de 30 días.

---

## 9. Menores

La App **no está dirigida a menores de 13 años** (o la edad mínima
equivalente en su jurisdicción). No recopilamos datos de menores a
sabiendas. Si cree que un menor nos ha facilitado datos personales,
contáctenos y los eliminaremos.

---

## 10. Transferencias internacionales

La App se desarrolla en Türkiye, pero la infraestructura subyacente
(Google Firebase) puede transferir datos fuera de Türkiye y del EEE.
La infraestructura de Google utiliza cláusulas contractuales estándar
aprobadas por la Comisión Europea para estas transferencias.

---

## 11. Cambios en esta política

Podemos actualizar esta Política de Privacidad de vez en cuando. La
"Fecha de entrada en vigor" arriba refleja la versión más reciente.
Para cambios materiales publicaremos un aviso en la App al menos 7
días antes de que la nueva política entre en vigor.

---

## 12. Contacto

Para cualquier pregunta, solicitud o reclamación sobre privacidad:

> **Murat Kul**
> nfvwzhbrbw@privaterelay.appleid.com
> Estambul, Türkiye
