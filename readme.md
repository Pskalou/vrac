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
    