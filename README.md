# Triple Tuned – 3D-Logo-Animation

Blender-Projekt für das „Triple Tuned“-Logo, erstellt mit Blender 5.3 und dem offiziellen Blender-Lab-MCP.

## Finale Dateien

| Datei | Inhalt |
|---|---|
| `triple_tuned_drop_4K.mp4` | **Finale Animation**, 3840×2160, 30 fps, 9 s, mit Ton (Mix v21) |
| `triple_tuned_drop.blend` | Blender-Projekt der Drop-Animation (rendert standardmäßig in Full HD) |
| `triple_tuned_drop_audio_v21.wav` | Finaler Soundtrack, -14 LUFS |
| `triple_tuned_spin.mp4` / `triple_tuned.blend` | Erste Version: einfache 360°-Drehung |
| `logo_clean.svg` / `logo_clean.png` | Sauber nachgezeichnetes Vektor-Logo (Vorlage: `logo_low_res.png`) |

## Ablauf der Drop-Animation (30 fps)

| Zeit | Bild | Ton (v21) |
|---|---|---|
| 0,8–2,9 s | Platten L, T, E, R, P, I fallen und schlagen ein | eigene Sounds aus `samples/self2.wav` (G3, A#3, F3, G3, E3, D3) + Metall-Layer, Whooshes, Swell (`anything.wav`) |
| 3,3–4,9 s | Laser schneidet TUNED aus | `laser.wav` + synthetischer Laser |
| 5,0 / 5,7 / 6,38 s | Balken I, II, III erscheinen | Plucks aus `SH_Pluck_Cut_D#.wav` (G2, D3, G3) |
| ab 5,6 s | III löst sich (Spitze bei 6,38 s) | `KSHMR_fx_impact_clean_bottom.wav`, Peak auf III |
| 7,96 s | Funkelstern am E, Lichtschweif | „Bling“ (synthetisch) |

Tonart der ganzen Sounddesigns: G-Moll.

## Hinweise

- Die Roh-Samples (`samples/`) sind aus Lizenzgründen nicht im Repo, sondern nur lokal vorhanden. Die fertigen Mixe und Videos enthalten den finalen Ton.
- Die Python-Skripte, mit denen die Mixe v1–v21 erzeugt wurden, lagen in einem temporären Ordner und sind nicht mehr vorhanden. Die gerenderten Mixe (`triple_tuned_drop_audio_v*.wav`) und Vorschauen sind vollständig erhalten.
- 4K-Render: `Blender -b triple_tuned_drop.blend --python-expr "import bpy; bpy.context.scene.render.resolution_percentage=200" -a` (ca. 1 Stunde).
- Große Binärdateien (`.blend`, `.wav`, `.mp4`, `.png`) werden mit Git LFS verwaltet.
