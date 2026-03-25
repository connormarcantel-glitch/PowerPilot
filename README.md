=============================================
  PowerPilot v2.0
  Intelligent Power Manager
=============================================

WHAT IT DOES
------------
PowerPilot runs silently in your system tray and automatically
adjusts your laptop's power profile based on:

  - Power source (AC vs battery)
  - CPU/GPU temperature and load
  - Running applications (games, editors, renderers, VR)
  - Machine learning that learns YOUR usage patterns over time

PROFILES
--------
  Efficiency      Battery saver - capped CPU, passive cooling, power saving
  Balanced        Normal desktop use on AC
  Performance     Detected heavy workload - editing, moderate gaming
  Max Performance Full power - gaming, VR, rendering, manual override

The ML engine continuously logs system state and learns when you
prefer which profile. After ~80 samples, it starts making predictions
and gets smarter the longer you use it.

DETECTED APPLICATIONS
---------------------
  Games:     Steam, Epic, GOG, Battle.net, EA, Ubisoft, + engine detection
  Editing:   DaVinci Resolve, Premiere Pro, After Effects, OBS, HandBrake
  Rendering: Blender, Cinema 4D, 3ds Max, Maya, Houdini, KeyShot
  VR:        SteamVR, Oculus/Meta Quest Link

HOW TO USE
----------
  - Right-click PowerPilot.exe -> Run as administrator
  - It appears as a lightning bolt icon in your hidden icons tray
  - Left-click the tray icon to open the dashboard
  - Right-click for quick profile switching and status

AUTO-START AT LOGIN
-------------------
  1. Press Win+R, type: shell:startup
  2. Create a shortcut to PowerPilot.exe in that folder
  3. Right-click the shortcut -> Properties -> Advanced
  4. Check "Run as administrator" -> OK

For best temperature monitoring, optionally install
LibreHardwareMonitor (free, open source) and run it alongside
PowerPilot. This gives accurate per-sensor CPU and GPU temps.

DATA STORAGE
------------
All data is stored in: %APPDATA%\PowerPilot\
  - powerpilot.log     Activity log
  - training_data.json ML training samples
  - model.pkl          Trained ML model
  - settings.json      User preferences

To reset ML learning, delete training_data.json and model.pkl.
