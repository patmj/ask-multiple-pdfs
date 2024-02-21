# MultiPDF Chat App

> You can find the tutorial for this project on [YouTube](https://youtu.be/dXxQ0LR-3Hg).

## Introduction
------------

L'application de MultiPDF Chat est une application Python qui vous permet de discuter avec plusieurs documents PDF. Vous pouvez poser des questions sur les PDF en langage naturel, et l'application fournira des réponses pertinentes en s'appuyant sur le contenu des documents. Cette application utilise un modèle de langage pour générer des réponses précises à vos questions. Veuillez noter que l'application ne répondra qu'aux questions relatives aux PDF chargés.

## Comment cela fonctionne
------------

![MultiPDF Chat App Diagram](./docs/PDF-LangChain.jpg)

L'application suit ces étapes pour répondre à vos questions:

1. Chargement du PDF : L'application charge plusieurs documents PDF et extrait leur contenu textuel.

2. Découpage du texte: Le texte extrait est divisé en petits morceaux qui peuvent être traités efficacement.
   
4. Modèle de langage: L'application utilise un modèle de langage pour générer des représentations vectorielles (embeddings/plongement) des fragments de texte.
   
6. Correspondance par similitude: Lorsque vous posez une question, l'application la compare avec les fragments de texte et identifie les extraits les plus proches du point de vue sémantique.

7. Génération de réponse: Les fragments sélectionnés sont transmis au modèle de langage, qui génère une réponse basée sur le contenu pertinent des PDF.

## Dépendances et installation
----------------------------
Pour installer l'application MultiPDF Chat, veuillez suivre les étapes suivantes:

1. Clonez le dépôt de votre machine locale.
   
2. Installez les dépendances requises en exécutant la commande suivante:
   
   ```
   pip install -r requirements.txt
   ```
3. (Facultatif) Obtenez une clé d'API à partir d'OpenAI et l'ajouter au fichier `.env` dans le répertoire du projet.

```commandline
OPENAI_API_KEY=your_secrit_api_key
```

## Utilisation

Pour utiliser l'application MultiPDF Chat, suivez les étapes suivantes:

1. Assurez-vous d'avoir installé les dépendances requises (facultatif: et ajouter la clé d'API OpenAI au fichier `.env`).

2. Exécutez le main.pyfichier utilisant le Streamlit CLI. Exécutzr la commande suivante:

   ```
   streamlit run app.py
   ```

3. L'application sera lancée dans votre navigateur web par défaut, affichant l'interface utilisateur.

4. Chargez plusieurs documents PDF dans l'application en suivant les instructions fournies.

5. Posez des questions en langage naturel sur les PDF chargés à l'aide de l'interface de chat.

## Contribution

Ce répertoire est destiné à des fins éducatives et n'accepte pas d'autres contributions. Il sert de support pour un tutoriel YouTube qui montre comment construire ce projet. N'hésitez pas à utiliser et à améliorer l'application en fonction de vos propres besoins.

## Licence

L'application de Chat MultiPDF est publiée sous [MIT License](https://opensource.org/licenses/MIT).
