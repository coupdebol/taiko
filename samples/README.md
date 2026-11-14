# Taiko samples

Real taiko recordings with open licences. None of them are isolated *don* / *ka* one-shots.
They are performance recordings, so slice individual hits out of them (see below).

| File | Length | Licence | Source / credit |
|---|---|---|---|
| `opengameart-jobro/taiko-drums-loop.ogg` | 3:39, stereo 44.1 kHz | CC-BY 3.0 | "Taiko drums (seamless loop)" by **jobro**, https://opengameart.org/content/taiko-drums-seamless-loop (cut from https://freesound.org/people/jobro/sounds/112248/). **Attribution required.** |
| `wikimedia-commons/taiko2-singapore-wind-symphony-25s.oga` | 0:25, mono 44.1 kHz | CC0 (per Commons) | "02 Taiko2 (short)", Scott Harding's *Taiko* performed by the Singapore Wind Symphony Percussion Ensemble. https://commons.wikimedia.org/wiki/File:02_Taiko2_(short).oga |
| `wikimedia-commons/sanja-matsuri-drums-and-flute.ogg` | 0:21, stereo 48 kHz | CC BY 3.0 | "Drums and flute at Sanja Matsuri" by **Torsodog**, https://commons.wikimedia.org/wiki/File:Drums_and_flute_at_Sanja_Matsuri.ogg. **Attribution required.** Field recording with flute and crowd, so it is noisy. |

## Using them in a sampler
- Don (centre of the head, low) and ka (rim, high, "clack") are easiest to find in the jobro loop.
  Cut hits at zero crossings with ffmpeg, e.g.
  `ffmpeg -ss 12.30 -t 0.8 -i taiko-drums-loop.ogg -af afade=t=out:st=0.6:d=0.2 don.wav`
- For a crude bass voice, pitch one slice down, e.g. `-af asetrate=44100*0.7,aresample=44100`.

## Looked at but not downloaded
- Free packs that need an email, a Gumroad checkout or a login, or whose licence is unstated:
  Strezov Thunder X3M (Kontakt), SampleScience Taiko Drums (plugin), Wavparty Akemie's/Dinky's Taiko (synthesised, not real taiko), Looperman, Freesound (login needed to download).
- BudgetPixel "Taiko War Drum Hit" is a single hit under CC BY 4.0. It is a good candidate for a clean *don* if you want to fetch it by hand.
