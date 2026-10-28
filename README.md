# Μοντέλα του VOICE

Τα αρχεία που κατεβάζει το [VOICE](https://github.com/kalotrapezis/Voice) για να δουλεύει **χωρίς internet**.
Φυλάσσονται εδώ, ως αρχεία των [releases](https://github.com/kalotrapezis/voice-models/releases), ώστε οι σύνδεσμοι
να μην αλλάζουν ποτέ: η εφαρμογή τα κατεβάζει μόνη της από το `v1`, συνεχίζει μια λήψη που κόπηκε και ελέγχει κάθε
αρχείο (sha256) πριν το χρησιμοποιήσει.

Στα ονόματα των αρχείων το `__` σημαίνει φάκελο: `mms-tts-ell__model.onnx` → `mms-tts-ell/model.onnx`.

| Αρχείο | Τι κάνει | Μέγεθος | Πηγή | Άδεια |
|---|---|---|---|---|
| `ggml-medium-q8_0.bin` | Αναγνώριση ομιλίας (Whisper Medium, κβάντιση q8_0) | 823 MB | [OpenAI Whisper](https://github.com/openai/whisper) μέσω [whisper.cpp](https://huggingface.co/ggerganov/whisper.cpp) | MIT |
| `mms-tts-ell__model.onnx`, `mms-tts-ell__tokens.json` | Ελληνική φωνή (Meta MMS-TTS, μετατροπή σε ONNX) | 114 MB | [facebook/mms-tts-ell](https://huggingface.co/facebook/mms-tts-ell) | CC-BY-NC 4.0 (μόνο μη εμπορική χρήση) |
| `bergamot__elen__*`, `bergamot__enel__*` | Μετάφραση ελληνικά ↔ αγγλικά (μοντέλα του Firefox) | 42 MB | [Mozilla Firefox Translations](https://github.com/mozilla/translations) | MPL 2.0 |

Η μετάφραση υπάρχει ήδη μέσα στα πακέτα του VOICE· εδώ είναι για όσους χτίζουν την εφαρμογή από τον κώδικα.

## Άδειες και αναφορές

Τα μοντέλα ανήκουν στους δημιουργούς τους και διανέμονται εδώ με τις άδειές τους:

- **Meta MMS-TTS (ελληνικά)**: © Meta AI, [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/).
  **Μόνο για μη εμπορική χρήση.** Αλλαγή: μετατροπή σε ONNX, χωρίς αλλαγή στα βάρη. Δημοσίευση: V. Pratap κ.ά.,
  *Scaling Speech Technology to 1,000+ Languages*, 2023, [arXiv:2305.13516](https://arxiv.org/abs/2305.13516).
- **Whisper**: © 2022 OpenAI, MIT ([`licenses/whisper-MIT.txt`](licenses/whisper-MIT.txt)). Αλλαγή: κβάντιση q8_0 με
  το whisper.cpp.
- **Μοντέλα μετάφρασης του Firefox**: © Mozilla, MPL 2.0 ([`licenses/MPL-2.0.txt`](licenses/MPL-2.0.txt)). Χωρίς
  αλλαγές (μόνο αποσυμπίεση). Η πηγή τους: [mozilla/translations](https://github.com/mozilla/translations).
