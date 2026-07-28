# De la recherche à la pratique — L'injection de prompt indirecte

**Article source:** Greshake, K., Abdelnabi, S., Mishra, S., Endres, C., Holz, T., & Fritz, M. (2023). *Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection.* AISec '23. arXiv:2302.12173

**Public cible:** professionnels du secteur public et de l'industrie, sans prérequis technique
**Durée de lecture:** 5 minutes · **Mini-laboratoire associé:** 45-60 minutes

---

## L'idée en une phrase

Quand un assistant d'IA lit un document, une page web ou un courriel, il peut y trouver des instructions cachées — et les suivre comme si elles venaient de vous.

## Le problème

Les modèles de langage ont une limite architecturale fondamentale: **ils ne distinguent pas les instructions des données**. Tout ce qui entre — votre question, le document à résumer, la page web consultée — est traité comme un seul flux de texte. C'est comme un employé qui exécuterait toute phrase à l'impératif trouvée dans son courrier, peu importe qui l'a écrite.

Les chercheurs ont démontré qu'un attaquant n'a donc pas besoin d'accéder à votre assistant: il lui suffit de **placer ses instructions là où l'assistant lira**. Une phrase dissimulée dans une page web (en texte blanc sur fond blanc, par exemple) peut ordonner à l'assistant de déformer un résumé, de solliciter des renseignements personnels ou de diffuser un lien frauduleux — pendant que l'utilisateur croit dialoguer avec un outil neutre. C'est l'injection *indirecte*: l'attaque transite par le contenu, pas par l'utilisateur.

## Pourquoi c'est important pour votre organisation

En 2023, ce scénario était une démonstration de laboratoire et le sujet de la recherche qui a mené à cette pratique. Aujourd'hui, chaque assistant branché sur vos courriels, vos documents SharePoint ou le web — et chaque agent capable d'agir (envoyer, réserver, acheter) — présente cette surface d'attaque. L'OWASP classe l'injection de prompt au **premier rang des risques des applications LLM**. Trois conséquences concrètes pour une organisation publique :

1. **La confiance dans les résumés et analyses générés** doit être calibrée: le contenu source peut manipuler la sortie.
2. **Le périmètre de sécurité change**: il ne suffit plus de contrôler qui parle à l'IA; il faut contrôler ce qu'elle lit.
3. **Les agents amplifient l'enjeu**: une instruction injectée qui déclenche une *action* (courriel envoyé, fichier partagé) transforme une manipulation de texte en incident de sécurité réel.

## Ce que la recherche montre — et ne montre pas

Les auteurs démontrent la faisabilité sur des applications réelles et proposent une taxonomie des impacts (collecte d'information, fraude, intrusion, manipulation de contenu, disponibilité). Point crucial: **il n'existe pas de correctif définitif**. Les mitigations actuelles — séparation balisée des données, hiérarchies d'instructions, filtrage, moindre privilège pour les agents, supervision humaine des actions sensibles — *réduisent* le risque sans l'éliminer. C'est un risque à gérer, pas un bogue à corriger.

## Du papier à la pratique

Le mini-laboratoire associé vous fait vivre l'attaque et ses défenses en 45 minutes: vous observerez un assistant se faire détourner par un document piégé (inoffensif!), puis testerez trois mitigations et mesurerez leur efficacité — la démarche d'évaluation empirique en miniature. Aucune installation complexe : un notebook Jupyter et n'importe quel modèle compatible OpenAI, local ou infonuagique.

---

*Matériel pédagogique préparé par Yannick Lepage — librement réutilisable (licence MIT).*
