---
stoplight-id: 8cwjgwxdg720y
---

# ACH(PSE)

-  \_PSE_


Configuración general de los medios de pago

| Field Name | Required  | Description | Example | Observations |
 ----------- | --------- | ----------- | ------- | ------------ |
| financialEntity | YES |  | 16 |  || N/A| code | YES | Propiedad de la request de la api que determina el medio de pago | \_PSE_ |
| Order | NO | | 2 | Indica la prioridad que se tiene en caso de que exita la misma franquicia pero de diferentes redes procesadoras, es decir, si se tiene AMEX de redeban y credibanco, la que tenga la priodidad 1 es la que va a intentar procesar primero la transacción. |
| comissionModel | NO |  | F | Sus valores posibles son F y P , donde F representa Valor Fijo y P representa  Valor en Porcentaje |
| comissionValue | NO |  | 2.5 |  |
| accountNumber | NO | | 26546 |  |
| accountType | NO | | 2 | Sus valores posibles son 1, 2 y 3, donde  1 representa SAVINGS(Ahorros), 2 representa  CURRENT(Corriente), y 3 representa CREDIT CARD(Tarjeta de crédito) |
| entityCode | YES | Usualmente es el nit o la identificación de la empresa | 9002992280 | |
| serviceCode | YES | Código generado por el comercio en la plataforma de ACH | 001 ||

---------------------------------------------------

## Información por paises:

**Colombia**

Métodos de pago:

-  \_PSE_

Observaciones:

- No se debe configurar el certificado
- No permite threeDS
- No se usan reglas de crédito

Ejemplo objeto paymentMethod:

```json
{
  "code": "_PSE_",
  "commissionModel": "F",
  "commissionValue": 0,
  "accountNumber": "1234567811",
  "financialEntity": 16,
  "accountType": 1,
  "settings": {
      "entityCode": "170892",
      "serviceCode": "15916855-8"
      "isEcommerce": true
  },
  "threeDS": false
}
```

---------------------------------------------------


