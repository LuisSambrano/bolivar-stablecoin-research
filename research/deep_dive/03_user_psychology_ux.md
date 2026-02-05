# Módulo 3: UX Research y Psicología del Usuario (El Factor Humano)

## 3.1 La Psicología de la Hiperinflación: "Mentalidad de Inmediatez"

En Venezuela, el dinero quema. El comportamiento del usuario está dictado por el trauma hiperinflacionario (2017-Presente).

- **Hot Potato Money**: El usuario no quiere "holdeal" bolívares ni 5 minutos.
  - _Implicación UX_: Cualquier función de "Swap a Dólares" debe ser instantánea (1-click). Si tarda >10 segundos, genera ansiedad.
- **Trust Markers (Marcadores de Confianza)**:
  - El usuario NO confía en garantías abstractas ("Algoritmos", "Reservas fraccionarias").
  - Solo confía en lo tangible: **"¿Puedo cambiar esto por Zelle/Efectivo YA?"**.
  - La marca "USD" o "Tether" tiene más peso psicológico que cualquier respaldo gubernamental.

## 3.2 Barreras de Entrada (UX Pain Points)

### 👴 La Brecha Gris (Digital Ageism)

- **Problema**: El diseño Fintech actual asume alfabetización digital alta (Seed phrases, Gas fees, Networks).
- **Realidad**: Gran parte de la riqueza está en manos de adultos mayores (+50) que no entienden "Switch Network to Celo".
- **Necesidad**: Abstracción TOTAL. "Email y Contraseña" es el límite de complejidad aceptable para el mercado masivo.

### 🐌 Infraestructura Hostil (Latency Kills)

- **Datos**: Velocidad móvil media ~12-14 Mbps, pero Latencia alta (~100ms) y paquetes perdidos frecuentes.
- **Consecuencia**: Apps pesadas (React Native sin optimizar) fallan en momentos críticos (pagar en caja).
- **Requisito Técnico**: "Offline First" o "Low Bandwidth Mode" no es un plus, es obligatorio. La app debe funcionar con Edge (2G/3G) inestable.

## 3.3 User Journey: El "Ciclo de la Remesa"

1.  **Recepción**: Llega USDT a Binance/Wallet (Alivio).
2.  **Conversión (El Dolor)**: Necesita Bs. para el mercado/bus. Entra a P2P.
    - _Ansiedad_: Buscar comerciante verificado → Miedo a estafa triangular → Esperar transferencia bancaria.
3.  **Gasto**: Paga con Pago Móvil (Bs.).
    - _Fricción_: Si sobra dinero en Bs., se devalúa.

**Oportunidad de Oro**: Una stablecoin que permita **pagar directamente en puntos de venta** (vía tarjeta o integración QR) sin pasar por el P2P manual eliminaría el 90% de la fricción actual.
