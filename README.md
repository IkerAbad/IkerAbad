# Iker Abad

**[Live demo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — European options, eight Greeks and an SVI surface in Rust and WebAssembly. 33 KB binary, 6.3-8.0 ms median recalculation. Nothing to install.

## Systems and performance

- **[db-engine](https://github.com/IkerAbad/db-engine)** — SQL engine in C++23 with 4 KB pages, a B+tree, a write-ahead log and crash recovery. 25 unit tests and 44 crash scenarios.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — limit order book and matching engine in C++23 with price-time priority. 51.2 ns per event in the pooled implementation, 3.1x the map version.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — CDCL SAT solver in C++23. 3.479 s on 14 instances against MiniSat 2.2.1 at 3.516 s.

## Quant and finance

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — European, American, Asian and barrier options in Python. Black-Scholes, Black-76, Monte Carlo, SVI and SSVI surfaces, path-dependent Greeks by likelihood ratio, and a five-day BTC stability study. 142 tests and 93 % line coverage with branch checking enabled.
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — event-driven backtesting with a Rust core and Python strategies. The look-ahead detector finds 780 future reads in the trap strategy.
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — execution cost for large orders against finite-depth books. Almgren-Chriss cuts risk-adjusted cost 24.91 % against TWAP at λ = 10⁻⁶.
- **[feature-store](https://github.com/IkerAbad/feature-store)** — incremental financial features with point-in-time correctness and versioned Parquet. 29.74x lower cost per tick than recomputing a 500-tick window.
- **[market-sim](https://github.com/IkerAbad/market-sim)** — agent-based market simulator. Kurtosis 5.488 and four-sigma tails 32.21x more frequent than normal, over 100,000 observations.
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — Binance spot ingestion into Parquet with a FastAPI API and a dashboard. Recovers the 5 trades lost in a 5-second cut.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — the demo above in repository form: eight Greeks and an SVI surface on canvas. 33 KB binary, 6.3-8.0 ms median recalculation.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — one-day VaR and CVaR with a rolling backtest. 120 breaches in 2,012 forecasts with the 95 % historical VaR.

## Mathematics and algorithms

- **[numlib](https://github.com/IkerAbad/numlib)** — numerical linear algebra from scratch in Python: LU, QR, SVD, eigenvalues and least squares. Largest relative eigenvalue error 2.47e-15 against NumPy.
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex with Bland's rule, Mehrotra interior point and convex QP. 36 comparisons against HiGHS, largest objective gap 1.16e-9.
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — elliptic-curve cryptography from scratch: secp256k1, RFC 6979 ECDSA and BIP32. 476 Wycheproof cases run in CI, 75 vendored (30 valid and 45 invalid).

## Tools

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — local panel for the Steam family library, with a packaged executable. 162 common tests, 58 browser tests and 4 platform tests. Latest release v3.0.1.
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — game inventory with GB per hour, a deletion plan and history in an Excel workbook. 259 tests.

## Packages

On PyPI:

- [`options-pricer` 1.1.0](https://pypi.org/project/options-pricer/) — `pip install options-pricer`. Published 23 November 2026.
- [`backtest-engine` 0.2.0](https://pypi.org/project/backtest-engine/) — `pip install backtest-engine`. Published 23 November 2026.
- [`numlib-linalg` 0.1.0](https://pypi.org/project/numlib-linalg/) — `pip install numlib-linalg`, imported as `numlib`. Repository `numlib`.
- [`iker-opt-solver` 0.1.0](https://pypi.org/project/iker-opt-solver/) — `pip install iker-opt-solver`. Repository `opt-solver`.
- [`execution-simulator` 0.1.0](https://pypi.org/project/execution-simulator/) — `pip install execution-simulator`.
- [`incremental-feature-store` 0.1.0](https://pypi.org/project/incremental-feature-store/) — `pip install incremental-feature-store`. Repository `feature-store`.

Not on PyPI:

- `market-sim` 1.0.0 — the name is too similar to an existing PyPI project.
- `game-inventory` 1.0.0 — same reason. Distributed from the GitHub release.
- `risk-lab` 1.1.0 — release published, PyPI upload pending because the account is rate-limited on new projects.

The bare names `numlib`, `opt-solver`, `market-sim` and `game-inventory` are taken or blocked on PyPI, hence the distribution names above.

## Stack

C++23 · Rust · Python · Kotlin · TypeScript · Java · C#

Last updated: 23 November 2026.

---

## Español

**[Demo en vivo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — opciones europeas, ocho griegas y una superficie SVI en Rust y WebAssembly. Binario de 33 KB, recálculo mediano de 6,3-8,0 ms. Sin instalar nada.

### Sistemas y rendimiento

- **[db-engine](https://github.com/IkerAbad/db-engine)** — motor SQL en C++23 con páginas de 4 KB, B+tree, WAL y recuperación tras caídas. 25 tests unitarios y 44 escenarios de caída.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — libro de órdenes y motor de matching en C++23 con prioridad precio-tiempo. 51,2 ns por evento en la implementación con pool, 3,1 veces la del mapa.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — solver SAT CDCL en C++23. 3,479 s en 14 instancias frente a 3,516 s de MiniSat 2.2.1.

### Quant y finanzas

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — opciones europeas, americanas, asiáticas y de barrera en Python. Superficies SVI y SSVI, griegas de trayectoria por likelihood ratio y un estudio de estabilidad de cinco días de BTC. 142 tests y 93 % de cobertura de líneas con comprobación de ramas activada.
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — backtesting event-driven con núcleo en Rust y estrategias en Python. El detector de look-ahead encuentra las 780 lecturas futuras de la estrategia trampa.
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — coste de ejecución de órdenes grandes contra libros de profundidad finita. Almgren-Chriss baja el coste ajustado por riesgo un 24,91 % frente a TWAP con λ = 10⁻⁶.
- **[feature-store](https://github.com/IkerAbad/feature-store)** — features financieras incrementales con corrección point-in-time y versiones en Parquet. 29,74 veces menos coste por tick que recalcular la ventana de 500.
- **[market-sim](https://github.com/IkerAbad/market-sim)** — simulador de mercado basado en agentes. Curtosis de 5,488 y colas de cuatro sigmas 32,21 veces más frecuentes que en una normal, sobre 100.000 observaciones.
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — ingesta de Binance a Parquet con API FastAPI y dashboard. Recupera los 5 trades perdidos en un corte de 5 segundos.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — la demo de arriba en forma de repositorio: ocho griegas y una superficie SVI en canvas. Binario de 33 KB, recálculo mediano de 6,3-8,0 ms.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — VaR y CVaR a un día con backtest rodante. 120 excesos en 2.012 previsiones con el VaR histórico al 95 %.

### Matemáticas y algoritmos

- **[numlib](https://github.com/IkerAbad/numlib)** — álgebra lineal numérica desde cero en Python: LU, QR, SVD, autovalores y mínimos cuadrados. Error relativo máximo de autovalores de 2,47e-15 frente a NumPy.
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex con la regla de Bland, punto interior de Mehrotra y QP convexo. 36 comparaciones contra HiGHS, brecha máxima de 1,16e-9 en el objetivo.
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — criptografía de curva elíptica desde cero: secp256k1, ECDSA con RFC 6979 y BIP32. 476 casos de Wycheproof ejecutados en CI, 75 vendorizados (30 válidos y 45 inválidos).

### Herramientas

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — panel local para la biblioteca familiar de Steam, con ejecutable empaquetado. 162 pruebas comunes, 58 de navegador y 4 de plataforma. Última release, v3.0.1.
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — inventario de juegos con GB por hora, plan de borrado e histórico en un libro de Excel. 259 tests.

### Paquetes

En PyPI:

- [`options-pricer` 1.1.0](https://pypi.org/project/options-pricer/) — `pip install options-pricer`. Publicado el 23 de noviembre de 2026.
- [`backtest-engine` 0.2.0](https://pypi.org/project/backtest-engine/) — `pip install backtest-engine`. Publicado el 23 de noviembre de 2026.
- [`numlib-linalg` 0.1.0](https://pypi.org/project/numlib-linalg/) — `pip install numlib-linalg`, se importa como `numlib`. Repositorio `numlib`.
- [`iker-opt-solver` 0.1.0](https://pypi.org/project/iker-opt-solver/) — `pip install iker-opt-solver`. Repositorio `opt-solver`.
- [`execution-simulator` 0.1.0](https://pypi.org/project/execution-simulator/) — `pip install execution-simulator`.
- [`incremental-feature-store` 0.1.0](https://pypi.org/project/incremental-feature-store/) — `pip install incremental-feature-store`. Repositorio `feature-store`.

Fuera de PyPI:

- `market-sim` 1.0.0 — el nombre es demasiado parecido a un proyecto existente en PyPI.
- `game-inventory` 1.0.0 — por el mismo motivo. Se distribuye desde la release de GitHub.
- `risk-lab` 1.1.0 — release publicada, subida a PyPI pendiente porque la cuenta tiene el límite de proyectos nuevos activo.

Los nombres simples `numlib`, `opt-solver`, `market-sim` y `game-inventory` están ocupados o bloqueados en PyPI, de ahí los nombres de distribución de arriba.

Última actualización: 23 de noviembre de 2026.
