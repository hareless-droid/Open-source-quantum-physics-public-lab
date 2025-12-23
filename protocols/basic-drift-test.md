# Basic Drift Test - $100 Proof of Concept

## Objective
Test if particles drift toward low-entropy regions, and if golden ratio (φ = 1.618) frequency enhances this effect.

## Theory
- Entropy gradient creates thermodynamic force: F = -T∇S
- Particles should drift from high-entropy (chaotic) to low-entropy (ordered) regions
- Hypothesis: φ-frequency optimizes this process

## Equipment Needed (~$100)

### Essential:
- **Speaker:** 20Hz-20kHz range, 10W+ (Amazon: search "Dayton Audio DAEX25")
- **Ferrofluid:** 30-50mL (Amazon: search "ferrofluid educational")
- **Container:** Glass petri dish, 100mm diameter
- **Test particle:** Polystyrene beads, 1-2mm diameter
- **Camera:** Webcam (720p minimum) or smartphone
- **Signal source:** Function generator app on phone (FREE)

### Optional:
- Neodymium magnets
- LED lighting
- Tripod/mount for camera

## Setup Instructions

### Step 1: Assemble Test Cell

1. Place speaker face-up on stable surface
2. Pour ferrofluid into petri dish (~5mm deep)
3. Place petri dish centered on speaker cone
4. Drop ONE test bead into ferrofluid (center)
5. Mount camera directly above, pointing down
6. Set up side lighting (reduces glare)

### Step 2: Camera Setup

- Position: 20-30cm above dish
- Angle: Perpendicular (straight down)
- Focus: On ferrofluid surface
- Frame: Entire dish visible
- Lighting: Bright but avoid direct reflection

### Step 3: Function Generator

Download free app:
- iOS: "Function Generator" 
- Android: "Signal Generator"

Settings:
- Waveform: Sine wave
- Amplitude: 50% (adjust if needed)
- Frequency: Will vary per test

## Experimental Protocol

### Test 1: Baseline (1.0 kHz)

1. Start video recording
2. Note starting position of bead
3. Start tone at **1000 Hz**
4. Record for **5 minutes**
5. Stop tone and recording
6. Note final position

### Test 2: Golden Ratio (1.618 kHz)

1. Reset bead to center (or use fresh bead)
2. Start video recording
3. Start tone at **1618 Hz**
4. Record for **5 minutes**
5. Stop tone and recording
6. Note final position

### Test 3: Control (Optional)

Try other frequencies:
- 1414 Hz (√2 × 1000)
- 2000 Hz (octave)
- 2718 Hz (e × 1000)

Same 5-minute protocol for each.

## Data Collection

### Extract bead position using:
- **Tracker** software (free from physlets.org/tracker)
- **Python + OpenCV** (see software/ folder if available)
- **Manual:** Screenshot every 30 seconds and measure

### Data Format:
```csv
time_sec, x_mm, y_mm, notes
0, 50.0, 50.0, starting position
30, 48.2, 50.1, 
60, 46.5, 49.8, 
...
300, 35.1, 50.3, final position
```

## Analysis

### Key Metric: Total Drift Distance
```
d = sqrt((x_final - x_start)² + (y_final - y_start)²)
```

### Comparison:
- Does φ-frequency (1618 Hz) produce MORE drift than baseline (1000 Hz)?
- Expected: 25-33% increase based on simulations
- Any drift > 5mm is significant (vs Brownian motion ~1mm)

## Expected Results

**If hypothesis is correct:**
- Bead drifts toward edge of dish (low vibration zone)
- φ-frequency shows 25-33% greater drift than baseline
- Direction is consistent across runs

**If hypothesis is wrong:**
- Bead shows random walk only
- No frequency dependence
- **This is also a valid result!**

## Troubleshooting

**Bead doesn't move:**
- Increase amplitude
- Check speaker is working
- Try different bead density

**Bead moves too much:**
- Decrease amplitude
- Use smaller beads
- Try higher viscosity ferrofluid

**Can't track bead:**
- Improve lighting
- Use contrasting bead color
- Slow down video playback

## Submitting Results

1. Upload video to YouTube/Vimeo (can be unlisted)
2. Export data to CSV or Google Sheets
3. Open GitHub Issue with "Experiment Run" template
4. Include setup photo, video link, data file

**Don't worry if results are messy - that's science!**

## Safety Notes

- Ferrofluid stains: Wear gloves, use drop cloths
- Speaker: Don't exceed rated power
- Magnets: Keep away from electronics

## Questions?

Open an Issue with "question" label.

**Good luck! Let's see what entropy does. 🔬**
