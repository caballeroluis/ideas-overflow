# 1. Reescribimos el archivo completo asegurando todas las URLs reales e inexpugnables

<img width="1500" height="996" alt="Warinerbeijing" src="https://github.com/user-attachments/assets/24914f38-0926-470e-be04-aedb0ff4b94b" />

# Case 005: Flawed Photo-Finish System

The traditional photo-finish layout used in Olympic athletics track races contains a native geometric and optical bias that systematically favors specific runners based on their lane distance to the camera.

## The Rolling Shutter & Line-Scan Anomaly
A photo-finish camera is a **line-scan camera** that continuously captures a single vertical slice of pixels aligned with the finish line, recording changes over time from top to bottom (rolling shutter effect).

In a standard athletics track layout architecture (as shown in the Beijing 2008 asset above):
1. The **furthest lane** from the camera (Lane 1) maps to the **top edge** of the captured image.
2. The **closest lane** to the camera (Lane 9) maps to the **bottom edge** of the image, right next to the lens.

Because the camera sensor reads and extracts pixel data sequentially from the top of the frame moving downwards, **the light coming from Lane 1 (top) is processed microseconds BEFORE the light coming from Lane 9 (bottom)**. At Olympic sprint speeds, this tiny gap in pixel serialization creates a physical, unfair advantage for the far lanes, imposing a silent hardware penalty on the runner closest to the lens layout.

## The Absolute Solution: Parallel Horizontal Slit
The side-angle placement does not fix the sensor lag if the line-scan grid remains vertical. The true structural fix requires matching the physical reading trajectory with the chronological plane:

*   **Horizontal Camera Alignment:** Rotate the line-scan camera 90 degrees, aligning the sensor array perfectly **horizontal and parallel** to the finish line.
*   **Simultaneous Cross-Lane Sweeping:** By sweeping the pixel array horizontally across the lanes instead of slicing from top to bottom, the sequential data readout registers all lanes under the exact same nanosecond time-stamp. Distance-to-lens lag is completely flattened, making the system 100% fair for high-stakes competition.

## Case Study: David Neville's Beijing 2008 Agony
David Neville’s iconic bronze medal dive at the Beijing 2008 400m final showcases this reality. Running in the closest position to the lens axis (Lane 9, bottom edge), his light was serialized last in the sensor line-sweep. He literally had to drag his skin against the track to overcome both the split-second timer and the sensor's sequential readout bias.

<img width="1280" height="960" alt="image" src="https://github.com/user-attachments/assets/f6963b68-d787-4f21-be0f-bd90557f0af8" />

### Empirical Validation Protocol (The Stress Test)
The definitive scientific proof of this hardware bias consists of executing the following field experiment:

1. **The Cube Launch:** Launch a geometrically perfect 3D solid cube at maximum velocity across the finish line.
2. **Camera Position Audit:** Capture the object's transit while swapping the camera setup across different geometric configurations (standard vertical side-angle vs. our horizontal parallel zenith alignment).
3. **Deformity Analysis:** Analyze the image. If the cube edges skew diagonally—indicating distortion not perfectly perpendicular to the finish line—the vertical sensor is introducing a row-readout micro-lag, causing an unfair timing bias across lanes.

## Empirical References and Case Studies
For a deeper audit on standard industrial implementation, reference the official coverage:
*   [Olympic Timing Analysis](https://www.olympics.com/es/noticias/como-se-determina-la-foto-finish) — Official breakdown by Olympics.com detailing Omega's 40,000 Hz vertical line-scan sensors.
*   [Historical Case Review](https://www.dakotaphotos.es/fotografia-de-deportes-las-5-mejores-photo-finish/) — Practical examples by Dakota Photos showcasing elevated overhead camera structures.
*   [Rolling Shutter Technical Overview](https://es.wikipedia.org/wiki/Rolling_shutter) — Detailed breakdown by Wikipedia explaining sequential sensor readout, skew distortion, and spatial-temporal anomalies.
*   [DPReview Rolling Shutter Video Analysis](https://www.dpreview.com/videos/3277074851/rolling-shutter-explained-with-simple-side-by-side-examples) — High-end hardware breakdown by DPReview with side-by-side visual examples of sensor readout lag.

---
*Technical Research Lab. Beijing 2008 asset courtesy of Jmex60 (CC BY-SA 3.0).*

