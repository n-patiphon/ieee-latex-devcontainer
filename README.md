# IEEE LaTex Dev Container

A boilerplate project for creating an IEEE paper in VS code using Development Container (devcontainer).

## Requirements
1. [Docker](https://docs.docker.com/desktop/linux/install/ubuntu/)
2. [Docker Compose](https://docs.docker.com/compose/install/compose-plugin/l)
3. [VS code](https://code.visualstudio.com/download)
3. [VS code remote containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

## Usage
1. Clone the repo
2. Run `id` in a terminal to get `UID`, `GUID`, and `UNAME`.
3. Change `UID`, `GUID`, `UNAME`, and `TZ` in the `.devcontainer/.env` file.
4. Press F1 and choose `Remote-Containers: Reopen in Container` in VS code.
5. Start writing (the output PDF file will be automatically built on save).
6. Preview the document by pressing F1 and choosing `LaTex Workshop: View LaTex PDF file`

## Tips
1. The Grammarly plugin will continuously check for grammar errors in the background.
2. Trailing spaces are removed on save.
3. To efficiently control the source files using Git, it is best to add a line break after a complete sentence, i.e., after a full stop. This can be done by selecting the target text, pressing F1, choosing `Replace Rules: Run Rule...`, and choosing `Replace Rules: Add a new line after every sentence`.

## Acknowledgment
- [latexdevcontainer](https://github.com/qdm12/latexdevcontainer)