FastSpeech 2 Bilingual TTS 🗣️🌐
Welcome to the official repository showcase for the FastSpeech 2 Bilingual Text-to-Speech (TTS) assignment project (Deadline: 07-11-2026).

🔗 Live Application & Evaluation PortalExperience and test the production interface and audio synthesis evaluation hub instantly here:
👉 Launch FastSpeech 2 TTS Portal (https://ggzi80-8ht3uxwbd-arcadawebapps2.vercel.app)

📝 Project OverviewFastSpeech 2 Bilingual TTS serves as the unified evaluation and synthesis layer for non-autoregressive text-to-speech accessibility. It is designed to bridge the gap between heavy deep-learning acoustic models and rigorous linguistic performance metrics, providing a responsive interface for automated English and Telugu speech generation and variance-adaptor inspection[cite: 1, 3, 7].

Core Features :
Bilingual Translation & Synthesis Hub: Built a seamless, high-performance web dashboard to process test sentences (E1–E4 for English and T1–T4 for Telugu)[cite: 1, 2] and synthesize high-fidelity conversational audio streams via HiFi-GN vocoders.

Responsive Variance-Adaptor Matrix:Designed with strict adherence to clean visual hierarchies, interactive loss curve inspectors, and multi-modal plot tabs displaying predicted duration, pitch ($F_0$), and energy distributions for every test utterance[cite: 2, 3].

Cloud & Repository Architecture Sync:Fully integrated repository pipelines mirroring the strict project/ folder structure to maintain persistent checkpoints, loss curves (training_loss.png, validation_loss.png), and reproducible configuration files (config.yaml)[cite: 2, 3].

🛠️ Technical Stack & Dataset Specifications

Model Architecture: Non-autoregressive FastSpeech 2 Transformer with direct variance predictors (Duration, Pitch $F_0$, Energy)[cite: 3].

Frontend Architecture: React, Vite, Tailwind CSS, Lucide React Icons[cite: 7].

Training Datasets:
English: Svarah dataset (~5 hours training, ~1 hour validation, zero overlap)[cite: 1].
Telugu: IndicTTS Telugu dataset with Akshara-level G2P mapping (~5 hours training, ~1 hour validation, zero overlap)[cite: 1, 11].

Deployment Platform: 
Optimized web cloud infrastructure and GitHub repository storage with Git LFS checkpoint support[cite: 3, 7].



# React + TypeScript + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react) uses [Babel](https://babeljs.io/) (or [oxc](https://oxc.rs) when used in [rolldown-vite](https://vite.dev/guide/rolldown)) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## React Compiler

The React Compiler is not enabled on this template because of its impact on dev & build performances. To add it, see [this documentation](https://react.dev/learn/react-compiler/installation).

## Expanding the ESLint configuration

If you are developing a production application, we recommend updating the configuration to enable type-aware lint rules:

```js
export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...

      // Remove tseslint.configs.recommended and replace with this
      tseslint.configs.recommendedTypeChecked,
      // Alternatively, use this for stricter rules
      tseslint.configs.strictTypeChecked,
      // Optionally, add this for stylistic rules
      tseslint.configs.stylisticTypeChecked,

      // Other configs...
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```

You can also install [eslint-plugin-react-x](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-x) and [eslint-plugin-react-dom](https://github.com/Rel1cx/eslint-react/tree/main/packages/plugins/eslint-plugin-react-dom) for React-specific lint rules:

```js
// eslint.config.js
import reactX from 'eslint-plugin-react-x'
import reactDom from 'eslint-plugin-react-dom'

export default defineConfig([
  globalIgnores(['dist']),
  {
    files: ['**/*.{ts,tsx}'],
    extends: [
      // Other configs...
      // Enable lint rules for React
      reactX.configs['recommended-typescript'],
      // Enable lint rules for React DOM
      reactDom.configs.recommended,
    ],
    languageOptions: {
      parserOptions: {
        project: ['./tsconfig.node.json', './tsconfig.app.json'],
        tsconfigRootDir: import.meta.dirname,
      },
      // other options...
    },
  },
])
```
