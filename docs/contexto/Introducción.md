---
stoplight-id: ack1oaak4z0zr
tags: [contexto]
---

# Introducción

Kubrick es una API que permite crear recursos en multiples aplicativos (Rest, ThreeDS, Microsites)
enviando unicamente una [petición](reference/Kubrick.json/paths/\~1api\~1integration\~1create-from-merchant/post),
ya que internamente todos estos recursos solicitados se asocian entre si, evitando que el cliente API
consuma multiples servicios con diferentes autenticaciones y condiciones, permitiendo de esta manera el enrolamiento de nuevos comercios para el uso de la pasarela.

Adicional a lo anterior, la API cuenta con la posibilidad de crear tokens de ThreeDS para que el cliente API haga uso de ellos de forma individual.

La API cuenta con 3 ambientes [(DEV, UAT, PROD)](reference/Kubrick.json).
