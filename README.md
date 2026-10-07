# nlp-video-multimodal-extraction
# Paskaitų asistentas: multimodalinis duomenų išgavimas iš video

Šiame projekte iš paskaitų video išgaunami keli duomenų tipai, kurie vėliau naudojami generatyvaus DI užduotims.

| Įvestis (X) | Išvestis (y) | Įrankis |
|---|---|---|
| Audio (.mp3) | Transkripcija (.txt) | Whisper |
| Vidurinis kadras (.jpg) | Paveikslėlio aprašymas (.txt) | Gemini API |

## Procesas
1. `01_data_preparation.ipynb`: video fragmentai → audio (mp3) → transkripcija (Whisper) ir vidurinis kadras (jpg).
2. `02_image_description.ipynb`: kadrai → aprašymai (Gemini API).

## Duomenų šaltinis
- **Kursas:** MIT OpenCourseWare, 6.0001 Introduction to Computer Science and Programming in Python (Fall 2016)
- **Paskaitos:** Lecture 1, 2, 3, 5, 6 (naudota po 1 min. fragmentą)
- **Autoriai:** Dr. Ana Bell, Prof. Eric Grimson, Prof. John Guttag
- **Šaltinis:** https://ocw.mit.edu/courses/6-0001-introduction-to-computer-science-and-programming-in-python-fall-2016/
- **Licencija:** Creative Commons BY-NC-SA 4.0 (https://creativecommons.org/licenses/by-nc-sa/4.0/)

Šiame repozitorijuje esantys video fragmentai, audio, kadrai, transkripcijos ir aprašymai yra išvestinė medžiaga, naudojama tik mokymosi tikslais ir platinama ta pačia licencija.

## Repozitorijos struktūra
- `data/video/`: 5 video fragmentai (.mp4)
- `data/audio/`: iš video išgauti garso failai (.mp3)
- `data/text/`: Whisper transkripcijos (.txt)
- `data/frames/`: vidurinių kadrų paveikslėliai (.jpg)
- `data/image-descriptions/`: Gemini sugeneruoti aprašymai (.txt)
- `01_data_preparation.ipynb`: duomenų paruošimas
- `02_image_description.ipynb`: paveikslėlių aprašymas

## Kaip paleisti
1. Atidaryk notebook'ą per Google Colab.
2. Antram notebook'ui Colab Secrets pridėk `GOOGLE_API_KEY` (Gemini API raktas iš AI Studio).
3. Paleisk langelius iš eilės.
