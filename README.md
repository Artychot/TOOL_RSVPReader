# TOOL_RSVPReader

      // Français //
Composant de lecture de texte réutilisable basé sur la technique RSVP (Rapid Serial Visual Presentation) pour TouchDesigner

# **Introduction**

TOOL_RSVPReader est un composant autonome et réutilisable développé dans TouchDesigner. Il explore une autre manière de présenter du texte dans un environnement visuel, en utilisant la méthode RSVP (Rapid Serial Visual Presentation).

L'idée est née d'un problème assez concret : intégrer du texte dans une composition visuelle ne garantit pas qu'il sera lu. Entre les images, les animations et les différentes sollicitations visuelles, un message peut facilement passer inaperçu ou devenir difficile à suivre.

Le principe du lecteur est simple : plutôt que d'afficher une phrase entière et de laisser le regard parcourir la ligne, les mots apparaissent successivement au même emplacement, un à la fois. L'attention est ainsi ramenée vers un point fixe, tandis que le texte se déroule à une cadence réglable.Chaque mot est aligné sur un point de référence appelé ORP (Optimal Recognition Point). Une lettre de référence est mise en évidence en rouge afin de maintenir un repère visuel constant d'un mot à l'autre. Cette approche vise à limiter les déplacements du regard et à faciliter le suivi de la lecture.

Au-delà de son aspect fonctionnel, TOOL_RSVPReader est aussi une expérimentation sur la place du langage dans les compositions visuelles. Comment rendre un message lisible dans un environnement où l'image domine ? Comment diriger l'attention sans multiplier les éléments à l'écran ?

# **Visualisations & Capture d’écran**

**Capture d’écran #1 | Projet Touchdesigner | artychot**

Interface nodale de TouchDesigner présentant l’architecture du composant TOOL_RSVPReader : gestion du texte, positionnement des mots et assemblage des éléments visuels par un réseau de TOPs et de scripts Python.

￼<img width="788" height="512" alt="Capture d’écran, le 2026-11-22 à 18 10 50" src="https://github.com/user-attachments/assets/f7a1d584-1f0a-439a-9c2b-d38faaaa85e1" />

** Capture d’écran #2 | Visualisation du Rendu dans Touchdesigner | artychot **

Interface RSVP minimaliste affichant un mot à la fois, avec un repère central rouge pour guider la lecture rapide et un encadrement horizontal.

￼<img width="472" height="194" alt="Capture d’écran, le 2026-11-22 à 18 13 33" src="https://github.com/user-attachments/assets/1479e293-5361-4663-8309-8b3220c6018d" />

** Extrait #1 | Visualisation du Rendu dans Touchdesigner | artychot**

Démonstration du composant TOOL_RSVPReader : une phrase défile mot par mot selon la méthode de lecture RSVP, jusqu’à révéler : « Tu ne détestes pas les lundis, tu détestes le capitalisme. »   [ insérer vidéo ici ]

https://github.com/user-attachments/assets/cbdd0360-8e54-4194-b87f-94f862b93d5f

# **Caractéristiques techniques**

| Environnement | - TouchDesigner

| Architecture | - Composant autonome et réutilisable (TOOL_RSVPReader)

| Texte Source | - Modifiable directement dans les paramètres du composant

| Typographie | - Courier New, police monospace assurant une largeur constante des caractères

| Taille de police | - 30 px par défaut, ajustable

| Méthode de lecture | - RSVP (Rapid Serial Visual Presentation)

| Repère visuel | - ORP (Optimal Recognition Point), avec mise en évidence rouge de la lettre de référence

| Traitement du texte | - Découpage automatique en mots et gestion de leur succession par indexation

| Vitesse | - Cadence de défilement réglable

| Positionnement | - Calcul dynamique pour maintenir le point de reconnaissance à une position fixe,indépendamment de la longueur des mots.


# **Principe de fonctionnement**

Le texte source est automatiquement découpé en une séquence de mots. Ceux-ci sont ensuite affichés successivement au même emplacement. Pour chaque mot, le système détermine le point de reconnaissance optimal (ORP), puis ajuste sa position horizontale afin que la lettre de référence reste alignée avec un repère fixe à l'écran.

L'utilisation de Courier New permet de conserver une largeur constante entre les caractères et de simplifier les calculs de positionnement. Deux Text TOP indépendants assurent l'affichage du mot complet et la mise en évidence de sa lettre de référence.

La cadence de lecture est réglable en secondes, ce qui permet d'adapter le comportement du composant au contexte de présentation et au type de contenu.

# **Installation**

Glissez le composant dans votre projet TouchDesigner, modifiez le texte source directement dans ses paramètres et ajustez les réglages selon vos besoins.

Cliquez, glissez et profitez !


# **Démarche de développement**

Le développement de TOOL_RSVPReader a donné lieu à une forme de collaboration assez particulière entre un humain et une intelligence artificielle.

Je prenais en charge la direction du projet, les intentions fonctionnelles et les choix visuels. ChatGPT intervenait comme assistant technique : il proposait des solutions, écrivait des portions de code Python et me guidait dans les manipulations à effectuer dans TouchDesigner.

Progressivement, les rôles ont pris une tournure assez particulière. Je devenais en quelque sorte l'exécutant d'une machine : je copiais ses instructions dans le Textport, lançais les commandes, observais les résultats et lui rapportais les erreurs. De son côté, ChatGPT me posait des questions de plus en plus précises sur mon environnement de travail, les paramètres et les comportements observés, afin d'adapter ses instructions à la situation réelle.

Une succession de commandes, de tests, de corrections et de validations s'est ainsi installée. ChatGPT ne pouvait ni voir mon interface ni intervenir directement dans le logiciel. Il dépendait entièrement de mes observations pour comprendre ce qui se passait. Je devenais ses yeux et ses mains, tandis qu'il organisait et orientait une partie du développement.

Il y avait quelque chose d'assez absurde dans cette situation : un humain qui exécute les instructions d'une machine pour construire un outil destiné à automatiser la lecture. Une sorte de mise en abyme où l'humain devient lui-même un intermédiaire d'exécution, au service d'une autre machine.

Cette expérience m'a intéressé autant pour son résultat technique que pour la dynamique qu'elle a fait émerger. Elle ouvre une réflexion sur les nouvelles formes de collaboration entre humains et intelligences artificielles, mais aussi sur les déplacements de rôles, de compétences et de responsabilités qu'elles peuvent entraîner.


# **TOOL_RSVPREADER_v∞[?] **

TOOL_RSVPReader est fonctionnel et prêt à être utilisé comme composant autonome dans des projets TouchDesigner.
Il constitue une base réutilisable, mais n'a pas la prétention de répondre à tous les contextes de lecture. La méthode RSVP, le positionnement ORP et la cadence d'affichage peuvent nécessiter des ajustements selon la typographie, la langue, le type de contenu ou les conditions de présentation.

Le composant est partagé comme un outil ouvert à l'expérimentation et à l'amélioration. Les adaptations, propositions et contributions permettant de l'ajuster à des besoins spécifiques sont les bienvenues.

·
·
·
·
·

        // English //
        
Reusable RSVP (Rapid Serial Visual Presentation) text reader component for TouchDesigner



# **Introduction**

TOOL_RSVPReader is a standalone, reusable component developed in TouchDesigner. It explores an alternative way of presenting text within visual environments using the RSVP (Rapid Serial Visual Presentation) method.

The idea came from a fairly simple observation: incorporating text into a visual composition doesn't necessarily mean it will actually be read. Between images, animations, and competing visual stimuli, textual messages can easily go unnoticed or become difficult to follow.

The reader takes a different approach. Instead of displaying an entire sentence and asking the viewer's eyes to scan across a line, words appear one at a time, successively occupying the same fixed position on screen. This brings attention to a single focal point while the text unfolds at an adjustable pace. Each word is aligned around a reference point known as the ORP (Optimal Recognition Point). A reference letter is highlighted in red to maintain a consistent visual anchor from one word to the next. This approach aims to reduce eye movement and make the reading process easier to follow.

Beyond its functional purpose, TOOL_RSVPReader is also an experiment in the role of language within visual compositions. How can a message remain readable in an environment dominated by images? How can attention be directed without adding more visual elements to the screen?

# **Visualizations & Screenshots**

Screenshot #1 | Touchdesigner Project | artychot

A TouchDesigner node-based interface showing the architecture of the TOOL_RSVPReader component: text management, word positioning, and visual element compositing through a network of TOPs and Python scripts.

<img width="788" height="512" alt="Capture d’écran, le 2026-11-22 à 18 10 50" src="https://github.com/user-attachments/assets/f7a1d584-1f0a-439a-9c2b-d38faaaa85e1" />
￼
 Screenshot #2 | Touchdesigner Rendered Visualisation | artychot 
A minimalist RSVP interface displaying one word at a time, with a central red fixation point to guide rapid reading and horizontal framing lines.

<img width="472" height="194" alt="Capture d’écran, le 2026-11-22 à 18 13 33" src="https://github.com/user-attachments/assets/1479e293-5361-4663-8309-8b3220c6018d" />

 Example #1 | Touchdesigner Rendered Visualisation | artychot 
An example of the TOOL_RSVPReader component, displaying the sentence “You do not hate Mondays, you hate capitalism” one word at a time using the RSVP reading method.

https://github.com/user-attachments/assets/cbdd0360-8e54-4194-b87f-94f862b93d5f


# **Technical Specifications**

Environment			  TouchDesigner
Architecture			Standalone, reusable component (TOOL_RSVPReader)
Source Text			  Editable directly through the component's parameters
Typeface			    Courier New (monospaced font)
Font Size			    30 px by default, adjustable
Reading Method		RSVP (Rapid Serial Visual Presentation)
Visual Reference	ORP (Optimal Recognition Point), with the reference letter highlighted in red
Text Processing		Automatic word splitting and sequential indexing
Speed				      Adjustable display interval, in seconds
Positioning			  Dynamic positioning calculation keeps the recognition point fixed, regardless of word length

# **How It Works**

The source text is automatically split into a sequence of individual words, which are then displayed successively at the same screen position.

For each word, the system identifies the optimal recognition point (ORP) and dynamically adjusts its horizontal position so that the reference letter remains aligned with a fixed point on screen.

Using Courier New ensures consistent character widths, making the positioning calculations more predictable. Two independent Text TOPs handle the display: one for the complete word and another for highlighting its reference letter.
The reading speed can be adjusted in seconds, allowing the component to adapt to different presentation contexts and types of content.

**How to set it up**

Drag the component into your TouchDesigner project, edit the source text directly in its parameters, and adjust the settings to suit your needs.
Drag, drop and enjoy!

# **Development Process**

The development of TOOL_RSVPReader led to a rather unusual form of collaboration between a human and an artificial intelligence.

I was responsible for the overall direction of the project, its functional intentions, and its visual decisions. ChatGPT acted as a technical assistant: suggesting solutions, writing portions of Python code, and guiding me through the operations required in TouchDesigner.

As the process evolved, the roles took on an unexpected dynamic. I gradually became the executor of a machine's instructions: copying commands into the Textport, running them, observing the results, and reporting back any errors. In turn, ChatGPT asked increasingly precise questions about my working environment, parameters, and observed behaviours in order to adapt its instructions to the actual state of the project.

A continuous sequence of commands, tests, corrections, and validations gradually took shape. ChatGPT couldn't see my interface or interact directly with the software. It relied entirely on my observations to understand what was happening. I became its eyes and hands, while it helped structure and guide part of the development process.
There was something rather absurd about this arrangement: a human executing a machine's instructions to build a tool designed to automate reading. A kind of recursive loop in which the human becomes an intermediary, carrying out operations on behalf of another machine.

I found this experience just as interesting for the technical result as for the working dynamic it produced. It raises questions about emerging forms

# **TOOL_RSVPREADER_v∞ [?]**

TOOL_RSVPReader is functional and ready for use as a standalone component within TouchDesigner projects.
While it serves as a reusable foundation, it is not intended to cover every possible reading scenario. The RSVP method, ORP (Optimal Recognition Point) positioning, and display cadence may require adjustments depending on the typeface, language, content type, or presentation conditions.

This component is shared as a tool open to experimentation and improvement. Adaptations, proposals, and contributions aimed at tailoring it to specific needs are welcome.
