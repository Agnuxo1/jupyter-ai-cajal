# CAJAL Integration for Jupyter AI

Use CAJAL as a **Custom Persona** in Jupyter AI to generate scientific papers directly from Jupyter notebooks.

## Quick Setup

### 1. Install Jupyter AI
```bash
pip install jupyter_ai
```

### 2. Configure Ollama with CAJAL
```bash
# Download CAJAL-9B
huggingface-cli download Agnuxo/CAJAL-9B-P2PCLAW --local-dir ./cajal

# Create Ollama model
ollama create cajal -f ./cajal/Modelfile
```

### 3. Add CAJAL Persona

Copy `cajal_persona.json` to your Jupyter AI personas directory:
- **Linux/Mac**: `~/.jupyter_ai/personas/`
- **Windows**: `%USERPROFILE%\.jupyter_ai\personas\`

### 4. Start Jupyter Lab
```bash
jupyter lab
```

### 5. Use CAJAL
- In Jupyter AI chat, select persona: **"CAJAL Scientific Writer"**
- Type: "Generate a paper about neural networks in climate modeling"
- CAJAL will output a structured paper with [ABSTRACT], [INTRO], etc.

## Example Session

```
User: Generate a paper about quantum computing applications in drug discovery

CAJAL:
[ABSTRACT]
Quantum computing offers unprecedented computational advantages...

[INTRO]
The pharmaceutical industry faces a critical bottleneck...

[METHODS]
We employed variational quantum eigensolver (VQE) algorithms...

[RESULTS]
Our simulations on 50 molecular structures demonstrated...

[CONCLUSIONS]
Quantum computing presents a viable pathway for accelerating...

--- TRIBUNAL REVIEW ---
Originality: 8.5/10
Methodology: 7.2/10
Clarity: 8.0/10
Impact: 9.1/10
Average: 8.2/10
```

## Links
- CAJAL GitHub: https://github.com/Agnuxo1/CAJAL
- HuggingFace: https://huggingface.co/Agnuxo/CAJAL-9B-P2PCLAW
- Paper: https://arxiv.org/pdf/2604.19792
