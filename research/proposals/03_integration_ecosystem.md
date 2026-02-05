# Ecosistema de Integración Técnica

## 1. El Stack de Celo: Por Qué es la Base

La elección de Celo no es ideológica, es pragmática para mercados emergentes.

### 1.1 MiniPay (Distribución)

- **Qué es**: Una wallet ultraligera (2MB) integrada en el navegador Opera Mini.
- **Valor Estratégico**: Opera Mini tiene +100M usuarios en África y está creciendo en LATAM. Resuelve el problema de "bajar una app de 50MB" con datos lentos.
- **Integración**: La "Invisible Gateway" viviría como una Mini-App dentro de este ecosistema, aprovechando la autenticación de Google de Opera.

### 1.2 SocialConnect (Identidad)

- **Problema**: Nadie en un mercado popular va a copiar/pegar `0x7a2...`.
- **Solución**: SocialConnect mapea `+58 412 1234567` -> `Wallet Address`.
- **UX**: "Enviar pago al 0412-1234567". El protocolo resuelve la dirección en segundo plano.

## 2. Oráculos y Datos (RedStone / Mento)

Para que la "Pasarela Invisible" funcione, el precio del Bolívar debe ser irrefutable.

- **Tasa del Día**: Se necesita un oráculo que alimente el contrato con la tasa **Paralela** (la real de la calle) y la **BCV** (Oficial).
- **Fuentes de Datos**: APIs de "Monitor Dolar" (DolarAPI) y BCV.
- **Mecanismo**: El Smart Contract usa esta tasa para calcular cuántos cUSD se deben liquidar para cubrir el monto en Bolívares.

## 3. Diagrama de Flujo de Datos

```mermaid
graph TD
    User[Usuario (MiniPay)] -->|1. Input: 100 Bs| App
    App -->|2. Get Rate (50 Bs/$)| Oracle[Oráculo Tasa]
    App -->|3. Lock $2.00 cUSD| Contract[Smart Contract]
    Contract -->|4. Signal Liquidity| LP[Market Maker]
    LP -->|5. Fiat Transfer (Pago Móvil)| Merchant[Comercio]
    Merchant -->|6. Confirm Receipt| App
```

## 4. Requisitos de Infraestructura Local

Aunque la tecnología es global, se necesitan "rieles" locales mínimos:

- **Nodos de Liquidez**: Entidades jurídicas con cuentas en bancos clave (Venezuela, Banesco, Mercantil) para ejecutar los Pagos Móviles en <30 segundos.
