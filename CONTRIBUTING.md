# Contributing
To make this project extensible as far into the future as possible we are following certain rules which will also make it possible to programmatically generate new language pairs from existing translations.

Pull requests, corrections, translations & fixes are welcome. Any contributions must be submitted under the same license that the original piece of work (see below). Take a look at any open issues or submit new ones if there is something that needs to be fixed or added.

## Translating for other languages
Translations in all languages are welcome. Send a pull request or open an issue any time of day or night.

**Please prepend the tag `[lang-code-lang-code]` to your issues and pull requests.** For example, `[fr-en]` for French-English. This will help everyone pick out things they care about.

We're happy for any contribution in any form, but if you're making more than one major change (i.e. translations for two different languages) it would be super cool of you to make a separate pull request for each one so that someone can review them more effectively and/or individually.

## Folder and Filename conventions
Every language pair should be saved in a folder called `lang-code-lang-code` for example `[fr-en]` for French-English. In each folder you save 
- .txt source files for each chapter
- and a folder called `APKG` 

The latter is for the output .apkg files after having imported and exported the .txt files via Anki.

**Each chapter name .txt file has five parts to it:**
1. UFLF
2. fr-en
3. Vocabulary Chapter X
4. Chapter title
5. .txt

**Explanation**
1. is an acronym for "Universal Foreign Language Flashcards", 
2. is the language code pair for the given languages where separated by a hyphen which corresponds to the order that the translations are shown on each side of the .txt files, 
3. is "Vocabulary Chapter X" is "Vocabulary Chapter" translated into the latter language (here English) followed by the chapter number (1, 2, 3 etc),
4. is the chapter title translated into the former language (here French),
5. is the extension file to make it readable by the correct text editors (here it is a text file)

**Each chapter name .apkg file has eight parts to it:**
1. UFLF
2. fr-en
3. Français-English
4. Vocabulary 
5. (Darigov Decks)
6. Chapter X
7. Chapter title
8. .apkg

**Explanation**
1. is an acronym for "Universal Foreign Language Flashcards", 
2. is the language code pair for the given languages where separated by a hyphen which corresponds to the order that the translations are shown on each side of the Anki Flashcard, 
3. the full language names separated by a hyphen translated in the original language
4. is the word "Vocabulary" translated into the latter language (here English),
5. a way to designate that the Anki Flashcards comes from a larger body of work (Darigov Decks, see our other works),
6. is "Chapter X" where the word "Chapter" is translated into the latter language (here English) followed by the Chapter number (1, 2, 3 etc),
7. is the Chapter title translated into the former language (here French),
8. is the extension file to make it readable by Anki-based software (here it is an Anki Package file)

## Requesting a new language
You can request a language via an issue request with the following title `[lang-code-lang-code]: Language Request` and body text:

```
*New language-existing language* has been requested, having the following title names in *New language* to build out the folder structure would be helpful to begin the translation of each chapter
0. Bienvenue!
1. Bonjour!
2. Me voici !
3. Les vacances en France
4. Les gens
5. Bon appétit!
6. La ville
7. Les fêtes
8. La maison
9. Médias et communications
10. Mode, Forme et santé
11. Les études
12. La vie professionnelle
13. L'amour et l'argent
```

Supplying the new language translation of all the chapter titles means that we can create the corresponding folder structure & to make it easier for you to just translate the content. In the future we hope to have code to auto generate the file structure for you but this is currently work in progress.

## Requesting a new language combination from existing translations
If you wish to pair two languages together that already exist you can do so manually. We are unsure of how best to integrate these as it means that if there are any corrections to be made someone will need to update each place where it is used which makes it hard to keep track of updates (do let us know if you have any suggestions).

## File structure
Each file has one row for each word or phrase separated by a `|` where the text on each side corresponds to the translation for the language given in the language code pair. 

The first card of Chapter 0 contains an introductory card which is in the latter language of the language pair. It must have the language pair for that deck appended in brackets on the front of the card because if a user has more than one UFLF introductory card in their Anki collection it will not be imported and the user will not know where they can find updates, corrections and improvements to the flashcards. For example `Introduction (UFLF fr-en)` for the French-English flashcards. 

Please work from Chapter 0 to Chapter 13 for consistency when translating into a new language as it also means that some can learn using your translation before having all the chapters available.

## Steps for submitting a new translation
The general process for porting existing translations to make a new language pair is the following:
1. Make a fork of the latest version of the repository
2. Download it to your local computer
3. Copy the source files which contains one side of the language pair you would like to make into a new folder with that language pair 
4. Rename the filenames translating the correct words if required
5. To the start of each row separated by a `|` the translation of the word or phrase into the new language. This allows you to ensure that you are making the correct translation and to ensure cross-language compatibility
6. Check your work (it is much easier to make corrections before many people have downloaded your translated flashcards than after)
7. On each line remove the previous translation that you used to help make your word
8. Generate the .apkg files with the correct filename in the app so that the chapter number and title are subdecks
    - Do so in a fresh desktop Anki profile to ensure that as many new words are imported as possible
    - Export each subdeck and the deck as a whole and add it to the APKG folder of your language pair
9. Make a pull request

Do not feel that you need to wait until all the chapters have been translated before making a pull request as it means that people can start learning.

Please ensure that there are exactly as many words and phrases in your new translation as in the original file that you copied over. This is important when it comes to being able to make new language combinations from existing translations, we will have a clear one-to-one mapping of words between languages. Anki will remove any duplicates so having duplicates will not be an issue when learning using the output .apkg files.

## Style Guidelines
- Do make sure punctuation is consistent across translations
    - This includes but is not limited to spaces, brackets, quotation marks, question marks, asterisks, exclamation points, ellipses etc.
- Do follow the naming conventions for file and folder names above
- Do ensure that you are using the correct delimiter on each row
- Do not delete or combine multiple translations into one line
- Refrain from adding additional context to a translation as it may not be relevant if your language gets paired with a different language in the future
- Do not use any online translation tools or dictionaries to help with the translation
    - We want this project to be a human-led endeavour as people tend to understand the context of translation better than computer generated tools