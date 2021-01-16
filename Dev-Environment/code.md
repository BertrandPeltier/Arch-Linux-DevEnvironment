## Installation de VS Code + extension

* Installation de VSC
```bash
pacman -S code
```
NB : il existe d'autres version : [https://wiki.archlinux.org/index.php/Visual_Studio_Code](https://wiki.archlinux.org/index.php/Visual_Studio_Code)

* Installation des extensions
NB : certaines extensions ne s'installe pas en lignes de commande, il faut les installer manuellement depuis le gestion de VSC (installer depuis un .VSIX).

BASE
```bash
code --install-extension MS-CEINTL.vscode-language-pack-fr # language pack en FR
code --install-extension ms-vsliveshare.vsliveshare # Live-share
code --install-extension github.vscode-pull-request-github # Gestion GitHub directement dans VSC
```
[Language pack FR](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-fr)
[Live-share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)
[GitHub](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)

MARKDOWN
```bash
code --install-extension bierner.markdown-preview-github-styles #Preview comme GitHub
code --install-extension DavidAnson.vscode-markdownlint # Linter md
```
[Preview GitHub](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
[Linter md](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

To be continued...