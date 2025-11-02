# Deeptics — Partner Preview (v0.3, Legged Series)

**What’s new**
- Added **Legged Series**: Compact/Micro humanoids, Power-class humanoid, Agile/Pet/Edu/Ghost quadrupeds, **Hexapod‑Mantis**, **Salamander**
- All assets ship with deterministic configs, default sensors, controller presets, and PoSml manifests.

**Why partners care**
- **Reproducible**: fixed seeds & calibrated noise profiles
- **Auditable**: signed artifacts (`run.log`, `metrics.json`) with traceable configs
- **Composable**: swap sensors/controllers via SDK without breaking determinism

**Integration**
- SDK/API: load asset → select env → choose planner → execute PoSml run
- Telemetry: task success, stability, latency, energy proxy
- Safety: workspace guards, joint limits, fail-safe halts

**Example validations**
- Humanoids: push‑recovery + whole‑body control stress tests
- Quadrupeds/Hexapod: gait stability on gravel/grass/incline; disturbance injections
- Salamander: CPG tuning for crawling/swimming transitions

**Mid-term roadmap (6–10 wks)**
- Environment Packs: FactoryCell, WarehouseAisle, LabBench, OutdoorTerrain
- Evaluation Suites: SLAM robustness, grasp success, gait/push‑recovery metrics
- SDK Preview: asset loader, sensor swap, planner orchestration, signed export
- Invite‑only Partner Preview: mirrored runs, dashboarded KPIs

**Contact**
partners@deeptics.ai
