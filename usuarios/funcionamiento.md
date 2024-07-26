---
title: Cómo funciona Awala
description: Awala permite que las aplicaciones compatibles compartan datos con y sin Internet, y utilicen cifrado de punta a punta.
permalink: /usuarios/funcionamiento/
breadcrumbs:
- usuarios/index.md
---

# Cómo funciona Awala en términos simples

Ya sea que te interese mucho la privacidad o simplemente tengas curiosidad, este documento te ayudará a entender cómo funciona Awala con un mínimo de jerga técnica.
Si buscas una explicación precisa, es posible que prefieras leer la [descripción técnica (inglés) 🡵](https://awala.network/tech-overview).

Asumimos que has utilizado Awala o al menos has visto [la demostración](https://youtu.be/LL1Z9EGiMVc).

## Por qué las aplicaciones de Internet necesitan una conexión a Internet y las aplicaciones de Awala no

Las aplicaciones convencionales en tu teléfono o computadora, como Facebook y Google Chrome, requieren una conexión a Internet para enviar y recibir datos de un servidor porque la aplicación misma establece la conexión con el servidor remoto.

En contraste, las aplicaciones compatibles con Awala delegan esa responsabilidad a otros componentes, como la [aplicación Awala en tu teléfono o computadora]({% link usuarios/descarga.md %}). De esta manera, tus aplicaciones favoritas pueden dejar que Awala use el mejor transporte disponible para ti en cualquier momento, y pueden concentrarse en lo que hacen mejor.

Entre bastidores, tu aplicación Awala se conecta a una _puerta de enlace de Internet_, que es un servidor que actúa como puente entre tu dispositivo y el resto de Awala en Internet. Todos tus datos se enrutan a través de este servidor, por lo que puede retener los datos entrantes para ti mientras estás desconectado. Por defecto, estás emparejado con una puerta de enlace de Internet operada por Relaycorp, pero, en principio, puedes ejecutar la tuya propia.

La animación a continuación muestra cómo la aplicación de Facebook para Android podría permitir que un usuario envíe datos a través de mensajeros de Awala cuando Internet no está disponible:

{% include embed_mp4_video.html path="/assets/diagrams/non-tech-overview.mp4" %}

Si Internet estuviera disponible, la aplicación Awala simplemente enviaría el mensaje a la puerta de enlace de Internet sin involucrar a los mensajeros.

## Cifrado de punta a punta

Similar a cómo tus conversaciones de WhatsApp están [cifradas de punta a punta 🡵](https://ssd.eff.org/es/glossary/cifrado-de-punta-punta), asegurando que solo tú y tus contactos puedan acceder a ellas, todos los datos intercambiados a través de Awala también están cifrados de punta a punta. Como resultado, ni los [mensajeros]({% link mensajeros.md %}) ni las puertas de enlace de Internet pueden leer o cambiar tus datos durante el tránsito.

Awala también permite evitar servidores de terceros, como los operados por redes sociales, entregando datos directamente a los destinatarios sin que el desarrollador de terceros sea consciente de la comunicación. Esto significa que las aplicaciones de Awala pueden ser más descentralizadas que sus contrapartes de Internet.

Sin embargo, depende del desarrollador de la aplicación decidir qué tan descentralizada será su aplicación. Algunas pueden no estar completamente descentralizadas si un servidor es esencial para ciertas funciones. [Letro](https://letro.app/es/), por ejemplo, omite su servidor para entregar conversaciones, pero aún utiliza el servidor para crear cuentas y conectar usuarios entre sí.

## Tu privacidad es una prioridad

Awala asigna a tu dispositivo un identificador único que se utiliza para enrutar datos hacia él, entre otras cosas. Puedes pensar en él como una dirección IP, pero una que no está vinculada a tu identidad o ubicación geográfica. Cualquiera en la red (por ejemplo, mensajeros, puertas de enlace de Internet, tus contactos de Letro) puede ver este identificador.

Dado que tus datos pasan por una puerta de enlace de Internet, ni tus socios de comunicación ni los desarrolladores de aplicaciones de terceros pueden determinar tu dirección IP, a menos que también operen tu puerta de enlace de Internet elegida.

Relaycorp está comprometida a proteger tu privacidad, por lo que solo guardamos la mínima cantidad de datos necesarios para operar nuestras puertas de enlace de Internet. Registramos las direcciones IP con fines de solución de problemas y prevención de abusos, pero no rastreamos a los usuarios ni compartimos lo poco que sabemos con terceros. Para más información, consulta [nuestra política de privacidad 🡵](https://awala.network/legal/).

También hacemos público todo el código fuente de Awala, incluidos los sistemas que utilizamos para publicar automáticamente el software que usas. Esto significa que cualquier persona con las habilidades técnicas relevantes puede verificar independientemente nuestras afirmaciones, así que no tienes que confiar solo en nuestra palabra.

## Las limitaciones que debes tener en cuenta

**Awala debe considerarse experimental**. No solo debes esperar que las cosas se rompan ocasionalmente, sino que también debes tener en cuenta que puede haber problemas de seguridad de los que aún no somos conscientes. Sin embargo, en el momento de escribir esto, estamos solicitando una auditoría de seguridad exhaustiva y esperamos publicar los resultados a mediados de 2024.

Independientemente de cualquier problema de seguridad presente en Awala, aún debes ser consciente de las siguientes limitaciones que se aplican a Awala y a cualquier otra cosa en tu dispositivo:

- Si el dispositivo está comprometido, el atacante podría comprometer los datos de tus aplicaciones, incluidos los de Awala.
- Un atacante puede distribuir aplicaciones que parecen ser Awala o una aplicación compatible con Awala, pero que en realidad son maliciosas, por lo que solo debes [instalar Awala de fuentes confiables]({% link usuarios/descarga.md %}).
