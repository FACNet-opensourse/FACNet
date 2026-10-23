# FACNet (Fixed Anti-Cheat Network)

![FACNet Logo](bannerfacnet.png)

An open-source CS2 demo analyzer that uses machine learning to detect aimbot kinematics and reduce false positives in anti-cheat systems.

##  What is FACNet?

FACNet is a post-match demo analysis tool for Counter-Strike 2. Instead of relying on statistical anomalies (like headshot percentage), it analyzes **mouse kinematics** to distinguish between legitimate aim and aimbot behavior.

## 💡 Why I Built This

I received a 20-hour VAC Live cooldown after a Wingman match where I won 4-2 with 3 Deagle headshots across different rounds. The system flagged my gameplay as suspicious based on stats alone, without analyzing *how* I aimed. This motivated me to build a better approach.

## 🔍 What FACNet Analyzes

1. **Mouse Kinematics**
   - Micro-corrections and jitter
   - Path curvature and straightness
   - Acceleration patterns

2. **Contextual Reaction Time**
   - FOV-based reaction analysis
   - Pre-aim positioning
   - Human biological limits

3. **Weapon-Specific Behavior**
   - Deagle 1-tap mechanics vs continuous tracking
   - AWP flick patterns
   - Spray control signatures

## 🛠️ Tech Stack

- **Language:** Python 3.13
- **Demo Parsing:** `demoparser2`
- **Data Processing:** `pandas`, `numpy`
- **Machine Learning:** `scikit-learn`, `XGBoost` (planned)
- **Visualization:** `matplotlib`, `plotly` (planned)

##  Installation

```bash
# Clone the repository
git clone https://github.com/FACNet-opensourse/FACNet.git
cd FACNet

# Install dependencies
pip install demoparser2 pandas numpy
