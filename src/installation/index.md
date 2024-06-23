---
outline: deep
---

# Installation

## From GitHub releases

1. Go to the [latest release](https://github.com/schooltape/schooltape/releases/latest).
2. Download the `.zip` file for your browser.
3. Extract the `.zip` file.
4. Follow the instructions for your browser:
   - [Chrome](chrome.md)
   - [Firefox](firefox.md)
   - [Edge](edge.md)
   - [Safari](safari.md)
   - [Other](chrome.md)
5. Enjoy Schooltape!

## From web stores

::: info
Schooltape is currently unavailable in the following web stores:

- Chrome Web Store
- Firefox Add-ons
- Edge Add-ons
- Opera Add-ons
- Safari Extensions

Please install Schooltape from GitHub releases or source code.
:::

## From source

::: warning
Installing from source is not recommended for most users.
:::

1. Clone the repository:

   ```sh
   cd path/to/where/you/want/schooltape/to/be
   git clone https://github.com/schooltape/schooltape.git # [!code focus]
   cd schooltape
   ```

2. Install [Bun](https://bun.sh/)

   ::: code-group

   ```bash [Linux]
   curl -fsSL https://bun.sh/install | bash
   ```

   ```bash [MacOS]
   curl -fsSL https://bun.sh/install | bash
   ```

   ```powershell [Windows]
   powershell -c "irm bun.sh/install.ps1 | iex"
   ```

   :::

3. Install dependencies

   ```bash
   bun install
   ```

4. Build the extension

   ::: code-group

   ```bash [Chrome]
   bun build
   ```

   ```bash [Firefox]
   bun build:firefox
   ```

   :::

5. Load the extension:

   - For Chrome / Chromium-based:

     1. Open `chrome://extensions/`.
     2. Enable Developer mode.
     3. Click on `Load unpacked`.
     4. Select the `dist` directory in the `schooltape` directory.

   - For Firefox:
     1. Open `about:debugging#/runtime/this-firefox`.
     2. Click on `Load Temporary Add-on`.
     3. Select the `manifest.json` file in the `dist` directory in the `schooltape` directory.

::: tip
You can also use `bun dev` or `bun dev:firefox` to build the extension in development mode, which will automatically reload the extension when you make changes. More information can be found in the [contributing guide](/contributing).
:::

::: warning
Loading a temporary add-on in Firefox will remove the extension when you close the browser.
:::
