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

Τα μοντέλα ανήκουν στους δημιουργούς τους και διανέμονται με τις άδειές τους, χωρίς αλλαγές πέρα από την κβάντιση
(Whisper) και τη μετατροπή σε ONNX (MMS).
