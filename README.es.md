<![CDATA[<div align="center">

<!-- HEADER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,6,11&height=200&section=header&text=Pasarela%20Invisible&fontSize=50&fontColor=fff&animation=twinkling&fontAlignY=35&desc=Investigación%20%7C%20Venezuela%20%7C%20Resiliencia%20Financiera&descSize=18&descAlignY=55"/>

<!-- BADGES -->
<p>
  <a href="#-resumen-ejecutivo"><img src="https://img.shields.io/badge/Fase-Investigación-blueviolet?style=for-the-badge" alt="Fase: Investigación"/></a>
  <a href="./manifesto.md"><img src="https://img.shields.io/badge/Ética-Investigación_Neutral-green?style=for-the-badge" alt="Ética"/></a>
  <a href="#-licencia"><img src="https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge" alt="Licencia"/></a>
</p>

<!-- LANGUAGE SWITCHER -->
<p>
  <a href="./README.md"><img src="https://img.shields.io/badge/🇺🇸_English-Available-lightgrey?style=flat-square" alt="English"/></a>
  <a href="./README.es.md"><img src="https://img.shields.io/badge/🇪🇸_Español-Seleccionado-blue?style=flat-square" alt="Español"/></a>
  <a href="./README.pt.md"><img src="https://img.shields.io/badge/🇧🇷_Português-Available-lightgrey?style=flat-square" alt="Português"/></a>
</p>

---

**De "Stablecoin" a "Infraestructura de Resiliencia"**  
_Un viaje de investigación riguroso que documenta por qué pivotamos de construir un token a construir un puente._

</div>

---

## 🎯 Resumen Ejecutivo

Este repositorio documenta **+12 meses de investigación** sobre la viabilidad de una stablecoin pegada al Bolívar para Venezuela. La conclusión fue contraintuitiva:

> **El mercado no necesita otra moneda. Necesita infraestructura invisible.**

Descubrimos que los venezolanos ya adoptaron USDT (el "Dólar Binance") como su moneda de reserva de facto. El verdadero punto de dolor no es _almacenar valor_—es **gastarlo de forma segura** sin bloqueos bancarios, estafas P2P o cierres de plataformas.

**Este repositorio captura:**
- ❌ Por qué una "Stablecoin del Bolívar" era un callejón sin salida (fragilidad algorítmica, riesgo legal)
- ✅ Por qué una "Pasarela Invisible" (holdear USD, gastar Bs. automáticamente) es el camino viable
- 📊 Prompts de investigación profunda para validación cuantitativa
- 🏗️ Arquitectura conceptual para integración Celo + MiniPay

---

## 🗂️ Estructura del Repositorio

```
bolivar-stablecoin-research/
│
├── 📜 manifesto.md                    # Ética y principios de investigación
│
├── 🔬 research/
│   ├── viability_analysis.md          # Hipótesis original (pre-pivote)
│   │
│   ├── deep_dive/                     # Fase 1: Investigación Profunda
│   │   ├── 01_fundamentals_and_global_context.md
│   │   ├── 02_venezuela_market_context.md
│   │   ├── 03_user_psychology_ux.md
│   │   └── 04_final_viability_verdict.md
│   │
│   ├── proposals/                     # Fase 2: Pivote Estratégico
│   │   ├── 01_invisible_gateway_architecture.md
│   │   ├── 02_compliance_user_flows.md
│   │   ├── 03_integration_ecosystem.md
│   │   └── 04_whitepaper_lite.md
│   │
│   ├── prompts/                       # Prompts para Gemini Deep Research
│   │   └── [6 prompts de investigación]
│   │
│   ├── data/                          # Resultados de investigación cuantitativa
│   ├── appendix/                      # Documentos de soporte
│   └── case_studies/                  # Análisis de casos externos
│
├── 🏛️ architecture/
│   └── initial_hypothesis.md          # Propuesta técnica original
│
├── ⚖️ legal/                           # Análisis regulatorio
│
├── 📐 docs/
│   ├── diagrams/                      # Diagramas Mermaid y arquitectura
│   └── assets/                        # Imágenes y media
│
└── 🧪 prototypes/                      # Futuro: Código POC (Fase 3)
```

---

## 📖 El Viaje de Investigación

### Fase 1: La Pregunta Ingenua
> _"¿Por qué no crear una stablecoin pegada al Bolívar?"_

Comenzamos analizando un hilo viral en X proponiendo esta idea. El análisis de viabilidad inicial reveló:
- ⚠️ **Riesgo Técnico**: Las stablecoins algorítmicas (modelo Terra) son frágiles
- ⚠️ **Riesgo Legal**: SUNACRIP y el colapso del Petro dejaron un vacío regulatorio
- ⚠️ **Realidad del Mercado**: Los venezolanos no confían en el Bolívar—punto

📄 Ver: [viability_analysis.md](./research/viability_analysis.md)

### Fase 2: La Investigación Profunda
Realizamos investigación exhaustiva en 8 dimensiones:
1. Fundamentos de stablecoins y mecanismos de colateralización
2. Panorama regulatorio global (MiCA, Ley GENIUS)
3. Casos de estudio: éxito de USDC vs. fracaso de Terra
4. Contexto del mercado venezolano (cierre de El Dorado, dominio P2P)
5. Escucha social y sentimiento del usuario
6. Puntos de dolor UX (bloqueos de cuentas, ansiedad por estafas)
7. Psicología del consumidor bajo hiperinflación
8. Síntesis final de viabilidad

📄 Ver: [research/deep_dive/](./research/deep_dive/)

### Fase 3: El Pivote
La investigación llevó a un pivote estratégico:

| Idea Original | Estrategia Pivotada |
|---------------|---------------------|
| Emitir un nuevo token (`BsD`) | Usar stablecoins existentes (`cUSD/USDT`) |
| Competir con USDT | Construir infraestructura _encima_ de USDT |
| Crear una moneda | Crear un **riel de pago** |

**El concepto "Pasarela Invisible":**
- Usuario holdea cUSD (estable, sus llaves)
- Usuario paga en Bolívares (vía Market Makers automatizados)
- Sin crypto visible en extractos bancarios (compliance-safe)

📄 Ver: [research/proposals/04_whitepaper_lite.md](./research/proposals/04_whitepaper_lite.md)

---

## 🛡️ Ética de Investigación

Este proyecto sigue estrictas guías éticas documentadas en [manifesto.md](./manifesto.md):

- **Neutralidad**: Sin afiliación política
- **Privacidad**: Protección de datos de usuario por diseño
- **Open Source**: Todos los hallazgos son públicos (Licencia MIT)
- **Sandbox**: Ejercicio teórico, no consejo de inversión

---

## 🚀 Hoja de Ruta

- [x] **Fase 1**: Hipótesis inicial y análisis de viabilidad
- [x] **Fase 2**: Investigación profunda (8 módulos)
- [x] **Fase 3**: Pivote estratégico y propuesta de arquitectura
- [ ] **Fase 4**: Recolección de datos cuantitativos (prompts)
- [ ] **Fase 5**: Prototipo en Celo Alfajores (testnet)
- [ ] **Fase 6**: Validación de usuario (integración MiniPay)

---

## 📜 Licencia

MIT License - Ver [LICENSE](./LICENSE) para detalles.

---

<div align="center">

_Gestionado por el Protocolo Agéntico **Antigravity**_

<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=2,6,11&height=100&section=footer"/>

</div>
]]>
