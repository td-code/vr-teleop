# Status und nächste Schritte

Hier tracken wir aktuellen Status und anstehende Aufgaben. Bitte vor jedem Treffen updaten.

## 26-03-17

Status:
- x

Nächste Schritte:
- [x] Regelmäßige Treffen aufsetzen: Vorschlag Montags, 14:00 Uhr 
- [x] Literaturrecherche https://www.reddit.com/r/robotics/comments/1nha7rc/we_developed_an_opensource_endtoend_teleoperation/
- [x] Literaturrecherche https://arclab-mit.github.io/beavr-landing/

BEAVR stellt ein modulares Teleoperations-Framework dar, das die Echtzeitsteuerung von Robotern über VR-Systeme ermöglicht. Der Fokus liegt auf einer niedrig-latenten Datenpipeline (≤35 ms), einer modularen Roboterabstraktion sowie der Aufzeichnung von Demonstrationsdaten im standardisierten LeRobot-Format.

Das System ist so aufgebaut, dass es:
- verschiedene Robotertypen unterstützt
- sowohl Simulation (z. B. MuJoCo, Isaac) als auch reale Hardware ansteuern kann
- mit modernen Visuomotor-Policies (z. B. DiffusionPolicy, ACT) kompatibel ist

- [x] Literaturrecherche https://github.com/ARCLab-MIT/BeaVR-app

Die BeaVR-App ist eine auf Unity & OpenXR basierende Anwendung für Meta Quest Geräte, die zur Erfassung von Hand- bzw. Controllerbewegungen sowie zur Visualisierung des Roboters in VR dient.

Die App:
- nutzt XR Hands / Controller Tracking
- überträgt Bewegungsdaten in Echtzeit an ein Backend
- empfängt visuelles Feedback
- ermöglicht intuitive Steuerung durch Gesten
-> Interface zwischen Mensch und Roboter


- [x] Zusammenfassung erstellen: Wie sieht BeaVR-Gesamtsystem aus? Auf welcher Plattform lauffähig und HW-Anforderungen? Welche Roboter werden unterstützt? Welche Datenformate (Huggingface)?

Meta Quest (BeaVR-App)
    ↓ Hand-/Controllertracking
Streaming / Netzwerk
    ↓
Backend (beavr-bot)
    ↓
Mapping + Inverse Kinematics
    ↓
Robot / Simulation

VR-Seite
- Meta Quest 2 / 3 / 3S
- WLAN-Verbindung
- Unity & OpenXR

Backend (offiziell):
- Linux/Docer
- NVIDIA GPU (CUDA)

Roboter:
    Explizit genannt:
    - RX-1 Humanoid
    - xArm + LeapHand
    Generell aber auch:
    - UR-Roboterarme
    - 7-DoF Manipulatoren
    - Quadrupeds

- [x] Literaturrecherche: welche ähnlichen Projekte gibt es?
- https://arxiv.org/pdf/2303.04137
- https://arxiv.org/pdf/2603.00020 (Meta Quest Pro)
- https://arxiv.org/pdf/2305.19352 (KI-Training)

- [x] evtl: Inbetriebnahme Meta Quest 3S beginnen.

## Backlog

- Anbindung an Simulation https://huggingface.co/docs/lerobot/so101 (Ros2, Mujoco, Isaac Sim?) oder Simulation Leap Hand V1?
 



 