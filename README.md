# Sharan's Road to French 🇫🇷

A 3D voice game for practising French vowels on the way to Paris.

A ball wearing a beret rolls down a Paris street toward wooden walls. Each wall has a hole at the height of one French sound. Say that sound out loud and hold it, and your voice lifts the ball into the hole. Say the wrong vowel, or go quiet, and it bounces off the wood.

**Play:** https://thimith.github.io/FrenchGame/ (open it on a phone and allow the microphone)

## Sounds
- **Easy:** A · E · I · O · U
- **Hard:** adds É and OU
- **Expert:** adds È and EU
- **Words mode:** walls show real words (tu, café, vous, mère…) with the target vowel highlighted

## How it hears you
The game listens to the *shape* of each vowel (its formants, the resonances of the mouth), not the pitch, so any note works. Everything runs in the browser and no audio leaves the phone.

For best results, tap **Calibrate** once (say A, I and OU) so the game learns your voice.

## Tech
- A single `index.html` with no build step. three.js r128 (MIT) is inlined so the game works offline once loaded.
- Vowel detection uses LPC with polynomial root-finding at about 60 analyses per second, then nearest-prototype classification in log-formant space.
- It needs https for microphone access. GitHub Pages provides that.
