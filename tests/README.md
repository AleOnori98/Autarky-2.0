# Test Suite for Autarky Models

This folder contains test scripts to verify that each optimization model in the repository:
- Runs without errors
- Produces expected result files (e.g., CSV, JSON)

## Default Case Studies
Each model (Deterministic, Expected, ICC, JCC) is tested using the pre-loaded inputs inside their `/inputs` folder.

The inputs are minimal test cases intended to:
- Validate functionality
- Keep runtime under 10–30 seconds per model

## Running Tests

From the project root:

```bash
julia --project=. tests/runtests.jl
