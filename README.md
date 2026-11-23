# Prophetly

Prophetly is a privacy-first time series forecasting app. It runs Facebook Prophet directly in your browser using WebAssembly. Your CSV data stays on your machine, and no calculations rely on a remote backend server.

## Features

- **100% Local & Private**: All data parsing and model fitting happen inside background Web Workers using WebAssembly.
- **Interactive Visualizations**: View forecast predictions, uncertainty bounds, decomposed trends, seasonalities, and changepoints.
- **Smart Cross-Validation**: Evaluate model performance with rolling historical cutoffs, metrics (RMSE, MAE, MAPE, MDAPE, Coverage), and cancellation controls.
- **Presets & Custom Settings**: Choose starting presets or fine-tune growth models, prior scales, and interval widths.
- **Local History & Exports**: Store past runs locally in your browser and export results to CSV, JSON, or PNG chart images.

## Getting started

### Prerequisites

- [Bun](https://bun.sh) (v1.3.0 or newer)

### Development

1. Install dependencies:

   ```bash
   bun install
   ```

2. Start the local development server:

   ```bash
   bun run dev
   ```

3. Open `http://localhost:5173` in your browser.

## Available scripts

- `bun run dev` starts the Vite dev server with HMR.
- `bun run build` compiles TypeScript and bundles the production assets, including the WASM binaries.
- `bun run preview` serves the production build locally.
- `bun run lint` runs Biome checks.
- `bun run test` runs the Vitest suite.
