# Flujos de Usuario y Capa de Cumplimiento (Compliance Layer)

## 1. Filosofía "No-KYC" (Tiered Access)

Para maximizar la adopción en la base de la pirámide, el sistema debe permitir operar montos bajos sin fricción burocrática, reservando el KYC estricto para volúmenes altos.

### Niveles de Acceso (Propuesta)

| Tier                 | Requisito                  | Límite Diario | Límite Mensual | Caso de Uso                   |
| :------------------- | :------------------------- | :------------ | :------------- | :---------------------------- |
| **Tier 0 (Anónimo)** | Solo Teléfono (SMS OTP)    | $10 USD       | $50 USD        | Micro-pagos, Pasaje, Pan      |
| **Tier 1 (Light)**   | Cédula + Selfie (Liveness) | $100 USD      | $500 USD       | Mercado semanal, Servicios    |
| **Tier 2 (Full)**    | RIF + Residencia           | $2,000 USD+   | Sin límite     | Comerciantes, Remesas grandes |

## 2. User Journey: El "Pago Invisible"

### Escenario: Pago de Mercado (Tier 1)

**Actor**: María (Jubilada). Tiene $50 cUSD en su MiniPay.
**Objetivo**: Pagar 250 Bs en la carnicería.

#### Paso 1: Iniciación (6 segundos)

1.  María abre MiniPay.
2.  Escanea el QR de Pago Móvil del carnicero (Estándar C2P venezolano).
3.  La App detecta: "Pago Móvil: V-1234567, Banco Venezuela, Monto: 250 Bs".
4.  La App calcula: "Son $5.00 cUSD (Tasa 50)".

#### Paso 2: Ejecución "Off-Ramp Invisible" (10-30 segundos)

5.  María confirma con su huella (Biometría).
6.  **Smart Contract**: Envía $5.00 cUSD + Fee al "Liquidity Pool".
7.  **Proveedor de Liquidez (LP)**:
    - Recibe los cUSD instantáneamente.
    - Ejecuta un Pago Móvil desde _su_ cuenta bancaria corporativa a la cuenta del carnicero.
    - _Seguridad_: La cuenta bancaria del LP está constituida como "Procesadora de Pagos", reduciendo riesgo de bloqueo.

#### Paso 3: Confirmación (3 segundos)

8.  El carnicero recibe SMS del banco: "Recibiste 250 Bs de Procesadora Pagos C.A.".
9.  María recibe notificación en MiniPay: "Pago Exitoso".

## 3. Mitigación de Riesgos (Risk Engine)

Para proteger la red de actores maliciosos y bloqueos bancarios:

1.  **Rotación de Cuentas Emisoras**: Los LPs no usan una sola cuenta bancaria. Rotan entre múltiples cuentas jurídicas para no saturar límites ni levantar alertas de velocidad.
2.  **Límites de Velocidad de Usuario**: Si María intenta hacer 50 pagos en 1 hora, se bloquea temporalmente (Patrón de "Pitufeo" o lavado).
3.  **Blacklist de Destinos**: Si un número de cédula destino reporta fraudes, se bloquea en la red.

## 4. Ventaja Psicológica

María **nunca "vendió" sus dólares**. Ella sintió que _pagó_ con dólares. Mentalmente, eliminó el paso de "Cambiar a Bolívares".
