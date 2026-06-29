# Case 005: Flawed Photo-Finish System

The traditional photo-finish layout used in Olympic track races contains a native geometric and optical bias that systematically favors specific runners based on their lane distance to the camera.

## 🌀 The Rolling Shutter & Line-Scan Anomaly
This is the exact same optical phenomenon that deforms moving airplane propellers in digital photos (**rolling shutter effect**). A photo-finish camera does not take a full picture; it is a **line-scan camera** that continuously captures a single vertical slice of pixels aligned with the finish line, recording changes over time from top to bottom.

In a standard track setup:
1. The runner in the **furthest lane** from the camera appears at the **top edge** of the captured image.
2. The runner in the **closest lane** appears at the **bottom edge** of the image.

Because the camera sensor reads and extracts pixel data sequentially from the top of the frame moving downwards, **the light coming from the furthest runner is processed microseconds before the light coming from the closest runner**. At Olympic sprint speeds, this tiny gap in pixel serialization creates a physical, unfair time-hiding advantage on the final composite image.
# Actualizamos la sección de la solución con tu corrección exacta de hardware
cat << 'EOF' >> ~/ideas-overflow/posts/case-005-flawed-photo-finish-system.md

## 🛠️ The Absolute Solution: Parallel Horizontal Slit
The side-angle or simple elevated placement does not fix the sensor lag if the line-scan grid remains vertical. The true structural fix requires matching the physical reading trajectory with the chronological plane:

*   **Horizontal Camera Alignment:** Rotate the line-scan camera 90 degrees, aligning the sensor array perfectly **horizontal and parallel** to the finish line.
*   **Simultaneous Cross-Lane Sweeping:** By sweeping the pixel array horizontally across the lanes instead of slicing from top to bottom, the sequential data readout registers all lanes under the exact same nanosecond time-stamp. Distance-to-lens lag is completely flattened, making the system 100% fair for high-stakes competition.

## 🌐 Empirical References and Case Studies
For a deeper audit on standard industrial implementation, reference the official coverage:
*   [Olympic Timing Analysis](https://www.olympics.com/es/noticias/como-se-determina-la-foto-finish) — Official breakdown by Olympics.com detailing Omega's 40,000 Hz vertical line-scan sensors.
*   [Historical Case Review](https://www.dakotaphotos.es/fotografia-de-deportes-las-5-mejores-photo-finish/) — Practical examples by Dakota Photos showcasing elevated overhead camera structures in cycling and winter sports.
*   [Rolling Shutter Technical Overview](https://es.wikipedia.org/wiki/Rolling_shutter) — Detailed breakdown by Wikipedia explaining sequential sensor readout, skew distortion, and spatial-temporal anomalies.
*   [Rolling Shutter Technical Overview](https://wikipedia.org) — Detailed breakdown by Wikipedia explaining sequential sensor readout, skew distortion, and spatial-temporal anomalies.