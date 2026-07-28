# De l'article à la pratique — Injection de prompt indirecte

Un échantillon pédagogique complet qui transforme un article de recherche en sécurité de l'IA en une expérience d'apprentissage pratique, bilingue-ready, pour des publics non spécialistes.

**Article source :** Greshake et al. (2023), *Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection* — [arXiv:2302.12173](https://arxiv.org/abs/2302.12173)

## Ce que contient ce dépôt

| Fichier | Rôle | Durée |
|---|---|---|
| `resume_injection_fr.md` | Résumé vulgarisé d'une page — « l'article en 5 minutes » pour un public professionnel non technique | 5 min de lecture |
| `lab_injection_indirecte.ipynb` | Mini-laboratoire Jupyter: réaliser une injection inoffensive, tester 3 mitigations, **mesurer** leur efficacité | 45-60 min |
| `guide_animateur.md` | Guide de l'animateur : minutage, réponses attendues, pièges fréquents, adaptation débutant/avancé | — |

## Pourquoi cet exemple

Ce triptyque (résumé accessible → exercice pratique → guide d'animation) illustre le mouvement « paper-to-practice » : rendre un concept d'IA complexe concret, mesurable et actionnable. Il couvre trois axes à la fois — **schémas d'invite**, **évaluation empirique de modèles** et **IA responsable** — sur un sujet classé dans le OWASP Top 10 for LLM Applications.

## Prérequis techniques

Volontairement minimaux : un notebook Jupyter et **n'importe quel endpoint compatible OpenAI**.
- **Local (recommandé, gratuit, privé)** : Lemonade Server, Ollama ou LM Studio
- **Infonuagique** : OpenAI ou autre — il suffit de changer l'URL de base et la clé

```bash
pip install openai
jupyter lab lab_injection_indirecte.ipynb
```

## Cadre éthique

Le laboratoire utilise exclusivement des charges **inoffensives** (le mot « BANANE ») dans un environnement contrôlé par l'apprenant, et rappelle explicitement les normes de divulgation responsable. Aucun système tiers n'est visé.

## Licence

MIT — réutilisation, adaptation et diffusion encouragées, y compris en contexte de formation.

---
*Préparé par Yannick Lepage. Retours bienvenus.*
