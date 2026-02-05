# Hipótesis de Arquitectura Inicial (v0.1)

## Resumen Ejecutivo

Para lograr una stablecoin del Bolívar (BsD) que sea viable transaccionalmente (bajos costos, alta velocidad) y ofrezca garantías mínimas de confianza, proponemos explorar una arquitectura híbrida: emisión centralizada (o federada) con liquidación en cadena pública de alto rendimiento.

## Stack Tecnológico Propuesto (A Evaluar)

### Capa de Liquidación (Blockchain)

- **Opción A: Solana (SPL Token)**
  - _Pros_: Costos de tx despreciables ($0.00025), finalidad sub-segundo.
  - _Contras_: Curva de aprendizaje (Rust), requisitos de hardware para nodos.
- **Opción B: Ethereum L2 (Optimism/Base - EVM)**
  - _Pros_: Compatibilidad total con herramientas Ethereum (Metamask, etc.), ecosistema DeFi maduro.
  - _Contras_: Costos ligeramente mayores que Solana, fragmentación de liquidez.

### Modelo de Emisión (Issuance)

- **Fiat-Backed (1:1)**:
  - El usuario deposita Bs. en cuenta custodia → Oráculo/Admin mintea BsD.
  - El usuario quema BsD → Admin libera Bs. a cuenta bancaria.
  - _Requisito Crítico_: Auditoría en tiempo real de las reservas (Proof of Reserves de Chainlink).

### Privacidad (Investigación Futura)

- Explorar **ERC-5564 (Stealth Addresses)** para ocultar el receptor.
- Explorar Pools de privacidad (ej. Privacy Pools 0.1) para separar fondos lícitos de ilícitos sin sacrificar privacidad total.

## Diagrama de Flujo Básico (Mermaid)

```mermaid
graph TD
    User[Usuario Final] -->|1. Envía Pago Móvil| Custody[Cuenta Custodia (Banco)]
    Custody -->|2. Confirma recepción| Issuer[Nodo Emisor (Off-chain)]
    Issuer -->|3. Mint BsD| Wallet[Wallet del Usuario]

    subgraph Blockchain
    Wallet -->|4. Transferencia BsD| Merchant[Comerciante]
    end

    Merchant -->|5. Request Redeem| Issuer
    Issuer -->|6. Burn BsD| Issuer
    Custody -->|7. Paga Bs. (Pago Móvil)| Merchant
```

## Próximos Pasos (Prototipo)

1.  Crear contrato ERC-20 estándar (OpenZeppelin) con funciones `mint` y `burn` controladas por roles (`AccessControl`).
2.  Desplegar en **Base Sepolia** (Testnet) para pruebas de costo y velocidad.
