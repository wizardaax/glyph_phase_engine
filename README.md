# Glyph Phase Engine

Python engine that processes symbolic input and adjusts operational phase based on dynamic delta values. Used for phase-state tracking in recursive models.

## Installation

```bash
pip install glyph-phase-engine
```

## Usage

```python
from glyph_phase_engine import GlyphPhaseEngine, PhaseState

# Create engine instance
engine = GlyphPhaseEngine()

# Process symbolic input
result = engine.process_symbolic_input("some_symbolic_data")
print(f"Phase state: {result}")

# Adjust phase with delta values
new_state = engine.adjust_phase_delta(0.5)

# Get current phase information
info = engine.get_phase_info()
print(info)
```

## Development

### Setup
```bash
pip install -e ".[dev]"
```

### Running Tests
```bash
pytest tests/ -v
```

### Building
```bash
python -m build
```

## CI/CD

This project uses GitHub Actions for automated testing and publishing:

- **Tests**: Run on every push and PR
- **TestPyPI Publishing**: Automatically publishes to TestPyPI on pushes to main
- **PyPI Publishing**: Publishes to PyPI on tagged releases using Trusted Publishing
- **SLSA Attestations**: Generates build provenance for security

### Publishing Workflow Features

- ✅ Trusted Publishing setup for PyPI/TestPyPI
- ✅ SLSA attestation generation 
- ✅ Build → twine check → provenance → publish → smoke install pipeline
- ✅ Version/tag consistency checks
- ✅ Comprehensive sanity checks and validation
- ✅ Dry-run capability for testing

## License

MIT License - see [LICENSE](LICENSE) file for details.
