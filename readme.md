# Retail theft Detection System

An AI-powered tool that uses computer vision to detect suspicious customer behavior in retail stores. Uses YOLOv8 for person detection, centroid-based tracking, and zone-based dwell time analysis.

## Features
- **Real-time person detection** via YOLOv8
- **Multi-person tracking** with unique IDs
- **Zone monitoring** — define regions of interest (e.g., high-value merchandise areas)
- **Dwell time alerts** — flags when someone lingers unusually long in a zone
- **Movement pattern tracking** — logs paths for behavioral analysis
- **Visual dashboard overlay** — real-time bounding boxes, zones, timers, and alerts

## Setup

```bash
# 1. Create virtual environment
python3 -m venv venv
source venv/bin/activate

# 2. Install dependencies
pip install -r requirements.txt

# 3. Run with webcam
python src/main.py

# 4. Run with a video file
python src/main.py --source path/to/video.mp4
```

## Configuration
Edit `config/settings.json` to customize:
- Detection confidence threshold
- Dwell time alert threshold (seconds)
- Zone definitions (coordinates)
- Tracking parameters


## Ethical Note
This system uses **anomaly detection** (statistical outliers from normal behavior). It tracks behavior patterns (dwell time, movement).
