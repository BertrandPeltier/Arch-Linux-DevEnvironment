## Installation de VS Code + extension

* Installation de VS Codium (Open-source release)
```bash
pacman -S code
```

* VS Code (Microsoft-branded release) depuis les dépôts AUR
```bash
git clone https://aur.archlinux.org/visual-studio-code-bin.git
```
cf. Tips [Dépots AUR](./Tips/aur.md)


* Extensions de base
    * [Language pack FR](https://marketplace.visualstudio.com/items?itemName=MS-CEINTL.vscode-language-pack-fr)
    * [Live-share](https://marketplace.visualstudio.com/items?itemName=MS-vsliveshare.vsliveshare)
    * [Gestion GitHub directement dans VSC](https://marketplace.visualstudio.com/items?itemName=GitHub.vscode-pull-request-github)
```bash
code --install-extension MS-CEINTL.vscode-language-pack-fr
code --install-extension ms-vsliveshare.vsliveshare
code --install-extension github.vscode-pull-request-github
```

* Markdown
    * [Preview GitHub](https://marketplace.visualstudio.com/items?itemName=bierner.markdown-preview-github-styles)
    * [Linter md](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)
```bash
code --install-extension bierner.markdown-preview-github-styles
code --install-extension DavidAnson.vscode-markdownlint
```
* HTML
    * [Linter HTML](https://marketplace.visualstudio.com/items?itemName=mkaufman.HTMLHint)
```bash
pacman -S htmlhint # A installer avant l'extension linter
code --install-extension mkaufman.HTMLHint
```
* CSS
    * [Linter stylehint CSS](https://marketplace.visualstudio.com/items?itemName=stylelint.vscode-stylelint)
    * [Si stylehint ne marche pas](https://marketplace.visualstudio.com/items?itemName=calvinhong.stylelint-fix)
    * [Auto-complexion class-name](https://marketplace.visualstudio.com/items?itemName=Zignd.html-css-class-completion)
    * [Color colorising](https://marketplace.visualstudio.com/items?itemName=kamikillerto.vscode-colorize)
```bash
pacman -S stylelint # A installer avant l'extension linter
code --install-extension vscode-stylelint
code --install-extension Zignd.html-css-class-completion
code --install-extension kamikillerto.vscode-colorize
```

* JS
    * [Linter JS](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
    * [Syntax highlighting](https://marketplace.visualstudio.com/items?itemName=mgmcdermott.vscode-language-babel)
    * [Bracket pair colorizer](https://marketplace.visualstudio.com/items?itemName=CoenraadS.bracket-pair-colorizer)
```bash
pacman -S eslint # a installer avant l'extension linter
code --install-extension dbaeumer.vscode-eslint
code --install-extension dzannotti.vscode-babel-coloring
code --install-extension CoenraadS.bracket-pair-colorizer
```

* PHP
    * [PHP](https://marketplace.visualstudio.com/items?itemName=bmewburn.vscode-intelephense-client)
```bash
code --install-extension bmewburn.vscode-intelephense-client
```

