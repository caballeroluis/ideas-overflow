# Case 002: The Mirror Firewall — Catching Deepfakes with Everyday Physics

<img width="1185" height="893" alt="espejito" src="https://github.com/user-attachments/assets/61c4088a-f9d6-4826-a191-9790393a4aae" />

This system checks if the person on the other side of the webcam is real or using a fake video (deepfake). Instead of spending money on expensive AI detection software, we use a physical mirror to break the hacker's setup.

## Where the Impostor's AI Fails

Deepfake programs work great when you look straight into the webcam because they only need to paste a "digital mask" over your original face. The trick breaks completely when you force the AI to draw two different angles at the same time (your front view and your side reflection in the mirror).

To trick this system, a hacker faces three math problems that are impossible to solve at home:

1. **Synchronization:** Their program must draw your front face and your reflection at 45 degrees perfectly in sync. If you turn your head, the reflection must move at the exact same millisecond.
2. **Lighting:** Room lights and reflections must bounce exactly the same way off real skin as they do off the fake pixels in the mirror.
3. **Image Cutting:** If you pass your hand in front of your face or the mirror, the AI has to calculate the edges in real-time, which adds complexity and exposes the whole act to more failures.

---

## How to Set Up the System

We require the candidate to place a normal, everyday mirror behind them at their desk.
