# Notes diverses

Notes, remarques, rappels, etc.


## VS Codium

### Activer le marketplace complet (VSCode)

source : https://github.com/VSCodium/vscodium/blob/master/DOCS.md#how-to-use-the-vs-code-marketplace

Sur Linux, créer/modifier le fichier `product.json` dans le dossier `~/.config/VSCodium` et y ajouter

    {
        "extensionsGallery": {
            "serviceUrl": "https://marketplace.visualstudio.com/_apis/public/gallery",
            "cacheUrl": "https://vscode.blob.core.windows.net/gallery/index",
            "itemUrl": "https://marketplace.visualstudio.com/items",
            "controlUrl": "",
            "recommendationsUrl": ""
        }
    }
    

## Vim

### Rechercher un motif et le remplacer partout dans le document

* Chercher *text1* et remplacer partour par *TEXT2* :<br/>
`:%s/text1/TEXT2/g`
* Remplacer les tabulations par des retours chariots :<br/>
`:%s/\t/\r/g`
* Avec des motifs cherchés et réécrits modifiés. Pour cela, on groupe le(s) motif(s) puis on y fait référence dans la partie remplacement. Exemple pour les fichiers `.srt` avec par exemple un `01:57:35.667` à remplacer par `01:57:35,667`. On utilise un motif de type \d\d : \d\d\d (où \d signifie un chiffre). On groupe un motif avec `\( ... \)`. Ce qui donne : <br/>
`:%s/\(\d\d\)\.\(\d\d\d\)/\1,\2/g`

source : [http://vimregex.com/#backreferences](http://vimregex.com/#backreferences)