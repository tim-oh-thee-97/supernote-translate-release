# Supernote Translate

Release APKs for my Translate app for Supernote Nomad.

> Please keep in mind that translation quality varies from language to language! I did not create the underlying data model that this app uses for translation, and I don't really have a way to improve it.

## Features

* Fully offline translation between any pairing of 49 supported languages.
* Uses Meta No Language Left Behind (NLLB) model under the hood. See [this link](https://huggingface.co/facebook/nllb-200-distilled-600M) for more details.
  * The license for this model is Creative Commons, NonCommercial -- meaning I can't sell this app but I can freely use the model as long as I give credit. So here it is!
* Allows input from keyboard or handwriting (as with any text input on Supernote devices).
* Maintains a translation history that is independent per-language pair (for example, EN->DE has a separate history from ES->IT).
* Shows you a short list of possible alternate translations for your input, and allows you to select one to bring it to the forefront as the "accurate" translation output.
* *For some languages that do not use the latin alphabet*, displays transliteration for the translated output (For example, 안녕하세요 also shows _annyeonghaseyo_ underneath).
  * I only implemented this for the languages that are "easy" to transliterate -- Greek, Russian, Korean, to name a few -- where the alphabet has a pretty straightforward letter-by-letter or character-by-character transliteration.

## How to Use

If you haven't already, you need to enable sideloading on your Supernote within `Settings->Security & Privacy`.

1. Navigate to the [Releases](https://github.com/tim-oh-thee-97/supernote-translate-release/releases) page.
2. Download the most recent APK.
3. Use your favorite sideloading application (I recommend [this one](https://github.com/nerdunit/androidsideloader/releases) on Windows) to install the app.
4. Upon first opening the app, you'll see a button prompting you to select a Model folder. Choose any empty folder where you have 650MB free.
> This next step requires an internet connection on your Supernote device, then forever after you can run translations offline.
5. After selecting the folder, tap the button marked "Download Model". It will download the NLLB model and associated config files.
6. Happy translating!
