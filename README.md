# Iker Abad

I build systems and research tools where the maths matters: market microstructure, numerical methods and data pipelines. Everything below is public, tested and reproducible.

**[Live demo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — European options, eight Greeks and an SVI surface in Rust and WebAssembly. 33 KB binary, 6.3-8.0 ms median recalculation. Nothing to install.

## Systems and performance

- **[db-engine](https://github.com/IkerAbad/db-engine)** — SQL engine in C++23 with 4 KB pages, a B+tree, a write-ahead log and crash recovery. 32 unit tests and 44 crash scenarios.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — limit order book and matching engine in C++23 with price-time priority. 74.6 ns per event in the pooled implementation, 2.4x the map version.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — CDCL SAT solver in C++23. 2.674 s on 14 instances against MiniSat 2.2.1 at 3.053 s.

## Quant and finance

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — European, American, Asian and barrier options in Python. Black-Scholes, Black-76, Monte Carlo, SVI and SSVI surfaces, path-dependent Greeks by likelihood ratio, and a five-day BTC stability study. 142 tests and 93 % line coverage with branch checking enabled. · [PyPI](https://pypi.org/project/options-pricer/)
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — event-driven backtesting with a Rust core and Python strategies. The look-ahead detector finds 780 future reads in the trap strategy. · [PyPI](https://pypi.org/project/backtest-engine/)
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — execution cost for large orders against finite-depth books. Almgren-Chriss cuts risk-adjusted cost 24.91 % against TWAP at λ = 10⁻⁶. · [PyPI](https://pypi.org/project/execution-simulator/)
- **[feature-store](https://github.com/IkerAbad/feature-store)** — incremental financial features with point-in-time correctness and versioned Parquet. 29.74x lower cost per tick than recomputing a 500-tick window. · [PyPI](https://pypi.org/project/incremental-feature-store/)
- **[market-sim](https://github.com/IkerAbad/market-sim)** — agent-based market simulator. Kurtosis 5.488 and four-sigma tails 32.21x more frequent than normal, over 100,000 observations. · [PyPI](https://pypi.org/project/abm-market/)
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — Binance spot ingestion into Parquet with a FastAPI API and a dashboard. Recovers the 5 trades lost in a 5-second cut.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — the demo above in repository form: eight Greeks and an SVI surface on canvas. 33 KB binary, 6.3-8.0 ms median recalculation.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — one-day VaR and CVaR with a rolling backtest. 120 breaches in 2,012 forecasts with the 95 % historical VaR. · [PyPI](https://pypi.org/project/var-cvar/)

## Mathematics and algorithms

- **[numlib](https://github.com/IkerAbad/numlib)** — numerical linear algebra from scratch in Python: LU, QR, SVD, eigenvalues and least squares. Largest relative eigenvalue error 2.47e-15 against NumPy. · [PyPI](https://pypi.org/project/numlib-linalg/)
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex with Bland's rule, Mehrotra interior point and convex QP. 36 comparisons against HiGHS, largest objective gap 1.16e-9. · [PyPI](https://pypi.org/project/optkit/)
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — elliptic-curve cryptography from scratch: secp256k1, RFC 6979 ECDSA and BIP32. 476 Wycheproof cases run in CI, 75 vendored (30 valid and 45 invalid).

## Tools

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — local panel for the Steam family library, with a packaged executable. 162 common tests, 58 browser tests and 4 platform tests. Latest release v3.1.2, also installable as the `steam-families-library` distribution. · [PyPI](https://pypi.org/project/steam-families-library/)
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — game inventory with GB per hour, a deletion plan and history in an Excel workbook. 259 tests. · [PyPI](https://pypi.org/project/gamesize/)

## Packages

Every project with a package links to it above. To install all of them:

```
pip install options-pricer
pip install backtest-engine
pip install numlib-linalg
pip install execution-simulator
pip install incremental-feature-store
pip install var-cvar
pip install abm-market
pip install gamesize
pip install optkit
pip install steam-families-library
```

Several names differ from their repository because the plain names were taken or blocked on PyPI: `numlib-linalg`, `incremental-feature-store`, `var-cvar`, `abm-market`, `gamesize`, `optkit` and `steam-families-library`. The import package and the command keep their original names.

Last updated: 25 November 2026.

---

## Español

Construyo sistemas y herramientas de investigación donde las matemáticas importan: microestructura de mercado, métodos numéricos y pipelines de datos. Todo lo de abajo es público, está probado y se puede reproducir.

**[Demo en vivo: wasm-pricer](https://ikerabad.github.io/wasm-pricer/)** — opciones europeas, ocho griegas y una superficie SVI en Rust y WebAssembly. Binario de 33 KB, recálculo mediano de 6,3-8,0 ms. Sin instalar nada.

### Sistemas y rendimiento

- **[db-engine](https://github.com/IkerAbad/db-engine)** — motor SQL en C++23 con páginas de 4 KB, B+tree, WAL y recuperación tras caídas. 32 tests unitarios y 44 escenarios de caída.
- **[orderbook](https://github.com/IkerAbad/orderbook)** — libro de órdenes y motor de matching en C++23 con prioridad precio-tiempo. 74,6 ns por evento en la implementación con pool, 2,4 veces la del mapa.
- **[sat-solver](https://github.com/IkerAbad/sat-solver)** — solver SAT CDCL en C++23. 2,674 s en 14 instancias frente a 3,053 s de MiniSat 2.2.1.

### Quant y finanzas

- **[options-pricer](https://github.com/IkerAbad/options-pricer)** — opciones europeas, americanas, asiáticas y de barrera en Python. Superficies SVI y SSVI, griegas de trayectoria por likelihood ratio y un estudio de estabilidad de cinco días de BTC. 142 tests y 93 % de cobertura de líneas con comprobación de ramas activada. · [PyPI](https://pypi.org/project/options-pricer/)
- **[backtest-engine](https://github.com/IkerAbad/backtest-engine)** — backtesting event-driven con núcleo en Rust y estrategias en Python. El detector de look-ahead encuentra las 780 lecturas futuras de la estrategia trampa. · [PyPI](https://pypi.org/project/backtest-engine/)
- **[execution-simulator](https://github.com/IkerAbad/execution-simulator)** — coste de ejecución de órdenes grandes contra libros de profundidad finita. Almgren-Chriss baja el coste ajustado por riesgo un 24,91 % frente a TWAP con λ = 10⁻⁶. · [PyPI](https://pypi.org/project/execution-simulator/)
- **[feature-store](https://github.com/IkerAbad/feature-store)** — features financieras incrementales con corrección point-in-time y versiones en Parquet. 29,74 veces menos coste por tick que recalcular la ventana de 500. · [PyPI](https://pypi.org/project/incremental-feature-store/)
- **[market-sim](https://github.com/IkerAbad/market-sim)** — simulador de mercado basado en agentes. Curtosis de 5,488 y colas de cuatro sigmas 32,21 veces más frecuentes que en una normal, sobre 100.000 observaciones. · [PyPI](https://pypi.org/project/abm-market/)
- **[market-data-service](https://github.com/IkerAbad/market-data-service)** — ingesta de Binance a Parquet con API FastAPI y dashboard. Recupera los 5 trades perdidos en un corte de 5 segundos.
- **[wasm-pricer](https://github.com/IkerAbad/wasm-pricer)** — la demo de arriba en forma de repositorio: ocho griegas y una superficie SVI en canvas. Binario de 33 KB, recálculo mediano de 6,3-8,0 ms.
- **[risk-lab](https://github.com/IkerAbad/risk-lab)** — VaR y CVaR a un día con backtest rodante. 120 excesos en 2.012 previsiones con el VaR histórico al 95 %. · [PyPI](https://pypi.org/project/var-cvar/)

### Matemáticas y algoritmos

- **[numlib](https://github.com/IkerAbad/numlib)** — álgebra lineal numérica desde cero en Python: LU, QR, SVD, autovalores y mínimos cuadrados. Error relativo máximo de autovalores de 2,47e-15 frente a NumPy. · [PyPI](https://pypi.org/project/numlib-linalg/)
- **[opt-solver](https://github.com/IkerAbad/opt-solver)** — simplex con la regla de Bland, punto interior de Mehrotra y QP convexo. 36 comparaciones contra HiGHS, brecha máxima de 1,16e-9 en el objetivo. · [PyPI](https://pypi.org/project/optkit/)
- **[crypto-lab](https://github.com/IkerAbad/crypto-lab)** — criptografía de curva elíptica desde cero: secp256k1, ECDSA con RFC 6979 y BIP32. 476 casos de Wycheproof ejecutados en CI, 75 vendorizados (30 válidos y 45 inválidos).

### Herramientas

- **[steam-family-library](https://github.com/IkerAbad/steam-family-library)** — panel local para la biblioteca familiar de Steam, con ejecutable empaquetado. 162 pruebas comunes, 58 de navegador y 4 de plataforma. Última release, v3.1.2, también instalable como distribución `steam-families-library`. · [PyPI](https://pypi.org/project/steam-families-library/)
- **[game-inventory](https://github.com/IkerAbad/game-inventory)** — inventario de juegos con GB por hora, plan de borrado e histórico en un libro de Excel. 259 tests. · [PyPI](https://pypi.org/project/gamesize/)

### Paquetes

Cada proyecto con paquete lo enlaza arriba. Para instalarlos todos:

```
pip install options-pricer
pip install backtest-engine
pip install numlib-linalg
pip install execution-simulator
pip install incremental-feature-store
pip install var-cvar
pip install abm-market
pip install gamesize
pip install optkit
pip install steam-families-library
```

Varios nombres no coinciden con su repositorio porque los nombres simples estaban ocupados o bloqueados en PyPI: `numlib-linalg`, `incremental-feature-store`, `var-cvar`, `abm-market`, `gamesize`, `optkit` y `steam-families-library`. El paquete que se importa y el comando conservan su nombre original.

Última actualización: 25 de noviembre de 2026.
