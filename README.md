# Iker Abad

**[Live demo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — European options, eight Greeks and an SVI surface in Rust and WebAssembly. 33 KB binary, 7-12 ms median recalculation. Nothing to install.

## Systems and performance

- **[db-engine](https://github.com/IkerAbad/db-engine)** — SQL engine in C++23 with 4 KB pages, a B+tree, a write-ahead log and crash recovery. 25 unit tests and 44 crash scenarios.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — limit order book and matching engine in C++23 with price-time priority. 51.2 ns per event in the pooled implementation, 3.1x the map version.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — CDCL SAT solver in C++23. 2.826 s on 14 instances against MiniSat 2.2.1 at 3.053 s.

## Quant and finance

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — European, American, Asian and barrier options in Python. Black-Scholes, Black-76, Monte Carlo, SVI on BTC and ETH snapshots, and SSVI on the full BTC surface. 134 tests and 94 % line coverage. On PyPI.
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — event-driven backtesting with a Rust core and Python strategies. The look-ahead detector finds 780 future reads in the trap strategy.
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — execution cost for large orders against finite-depth books. Almgren-Chriss cuts risk-adjusted cost 24.91 % against TWAP at λ = 10⁻⁶.
- **[feature-store](https://github.com/IkerAbad/feature-store)** — incremental financial features with point-in-time correctness and versioned Parquet. 25.82x lower cost per tick than recomputing a 500-tick window.
- **[market-sim](https://github.com/IkerAbad/market-sim)** — agent-based market simulator. Kurtosis 5.488 and four-sigma tails 32.21x more frequent than normal, over 100,000 observations.
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — Binance spot ingestion into Parquet with a FastAPI API and a dashboard. Recovers the 5 trades lost in a 5-second cut.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — the demo above in repository form: eight Greeks and an SVI surface on canvas. 33 KB binary, 7-12 ms median recalculation.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — one-day VaR and CVaR with a rolling backtest. 120 breaches in 2,012 days with the 95 % historical VaR.

## Mathematics and algorithms

- **[numlib](https://github.com/IkerAbad/numlib)** — numerical linear algebra from scratch in Python: LU, QR, SVD, eigenvalues and least squares. LU error 1.8e-15 at order 20 against LAPACK's 1.3e-15.
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex with Bland's rule, Mehrotra interior point and convex QP. 36 comparisons against HiGHS, largest objective gap 1.16e-9.
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — elliptic-curve cryptography from scratch: secp256k1, RFC 6979 ECDSA and BIP32. 476 Wycheproof cases, 168 valid and 308 invalid.

## Tools

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — local panel for the Steam family library, with a packaged executable. 118 offline tests and 55 browser tests. Latest release v2.10.0.
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — game inventory with GB per hour, a deletion plan and history in an Excel workbook. CI requires 98 % coverage.

## Packages

- [`options-pricer` 0.8.0](https://pypi.org/project/options-pricer/) — `pip install options-pricer`. Published 23 November 2026.

## Stack

C++23 · Rust · Python · Kotlin · TypeScript · Java · C#

Last updated: 23 November 2026.

---

## Español

**[Demo en vivo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — opciones europeas, ocho griegas y una superficie SVI en Rust y WebAssembly. Binario de 33 KB, recálculo mediano de 7-12 ms. Sin instalar nada.

### Sistemas y rendimiento

- **[db-engine](https://github.com/IkerAbad/db-engine)** — motor SQL en C++23 con páginas de 4 KB, B+tree, WAL y recuperación tras caídas. 25 tests unitarios y 44 escenarios de caída.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — libro de órdenes y motor de matching en C++23 con prioridad precio-tiempo. 51,2 ns por evento en la implementación con pool, 3,1 veces la del mapa.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — solver SAT CDCL en C++23. 2,826 s en 14 instancias frente a 3,053 s de MiniSat 2.2.1.

### Quant y finanzas

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — opciones europeas, americanas, asiáticas y de barrera en Python. Black-Scholes, Black-76, Monte Carlo, SVI sobre snapshots de BTC y ETH, y SSVI sobre la superficie completa de BTC. 134 tests y 94 % de cobertura de líneas. En PyPI.
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — backtesting event-driven con núcleo en Rust y estrategias en Python. El detector de look-ahead encuentra las 780 lecturas futuras de la estrategia trampa.
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — coste de ejecución de órdenes grandes contra libros de profundidad finita. Almgren-Chriss baja el coste ajustado por riesgo un 24,91 % frente a TWAP con λ = 10⁻⁶.
- **[feature-store](https://github.com/IkerAbad/feature-store)** — features financieras incrementales con corrección point-in-time y versiones en Parquet. 25,82 veces menos coste por tick que recalcular la ventana de 500.
- **[market-sim](https://github.com/IkerAbad/market-sim)** — simulador de mercado basado en agentes. Curtosis de 5,488 y colas de cuatro sigmas 32,21 veces más frecuentes que en una normal, sobre 100.000 observaciones.
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — ingesta de Binance a Parquet con API FastAPI y dashboard. Recupera los 5 trades perdidos en un corte de 5 segundos.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — la demo de arriba en forma de repositorio: ocho griegas y una superficie SVI en canvas. Binario de 33 KB, recálculo mediano de 7-12 ms.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — VaR y CVaR a un día con backtest rodante. 120 excesos en 2.012 días con el VaR histórico al 95 %.

### Matemáticas y algoritmos

- **[numlib](https://github.com/IkerAbad/numlib)** — álgebra lineal numérica desde cero en Python: LU, QR, SVD, autovalores y mínimos cuadrados. Error de 1,8e-15 en LU de orden 20 frente a 1,3e-15 de LAPACK.
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex con la regla de Bland, punto interior de Mehrotra y QP convexo. 36 comparaciones contra HiGHS, brecha máxima de 1,16e-9 en el objetivo.
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — criptografía de curva elíptica desde cero: secp256k1, ECDSA con RFC 6979 y BIP32. 476 casos de Wycheproof, 168 válidos y 308 inválidos.

### Herramientas

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — panel local para la biblioteca familiar de Steam, con ejecutable empaquetado. 118 pruebas sin red y 55 de navegador. Última release, v2.10.0.
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — inventario de juegos con GB por hora, plan de borrado e histórico en un libro de Excel. El CI exige un 98 % de cobertura.

### Paquetes

- [`options-pricer` 0.8.0](https://pypi.org/project/options-pricer/) — `pip install options-pricer`. Publicado el 23 de noviembre de 2026.

Última actualización: 23 de noviembre de 2026.
