# Contributing

First off, thanks for taking the time to contribute :tada:!

Before you do anything, you need to setup a development environment.
If you haven't used Git before, I'd highly recommend reading [Pro Git](https://git-scm.com/book/en/v2) (it's 100% free and open source)

1. Fork this repository

   - [What is a fork?](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/working-with-forks/fork-a-repo)
   - [Fork Schooltape](https://github.com/schooltape/schooltape/fork)

2. Clone your fork

   - Make sure you have [Git](https://git-scm.com/) installed
   - [What is cloning?](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository)
   - Clone Schooltape

   ```bash
   cd /path/to/your/working/directory
   git clone https://github.com/your_username/schooltape # [!code focus]
   cd schooltape
   ```

3. Install [Bun](https://bun.sh/)

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

4. Install dependencies

   ```bash
   bun install
   ```

5. Build the extension

   ::: code-group

   ```bash [Chrome]
   bun dev
   ```

   ```bash [Firefox]
   bun dev:firefox
   ```

   :::

## Code

::: warning
This section is outdated for the upcoming `v3.0.0` release of Schooltape. Please wait for the release before contributing.
:::

In this next section, we'll look into how you can make your own plugins, themes, or snippets and then, submit a [Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests).

### Plugins

1. [Open an issue](https://github.com/schooltape/schooltape/issues/new/choose) describing your plugin to get your idea approved
2. Add your plugin to the [`plugins.json`](https://github.com/schooltape/schooltape/blob/main/src/plugins/plugins.json) file
3. Create your plugin, a good example is [`timetable-labels`](https://github.com/schooltape/schooltape/blob/main/src/plugins/timetable-labels/timetable-labels.js)
4. Submit a PR

### Themes

This project uses [Catppuccin](https://github.com/catppuccin/catppuccin)

1. [Open an issue](https://github.com/schooltape/schooltape/issues/new/choose) describing your change to the theme to get your idea approved
2. [Create](https://github.com/schooltape/schooltape/fork) a fork of the repository
3. Make your changes to [`catppuccin.css`](https://github.com/schooltape/schooltape/blob/main/src/themes/catppuccin.css)
4. Submit a PR

### Snippets

#### Public Snippets

1. [Open an issue](https://github.com/schooltape/schooltape/issues/new/choose) describing your snippet to get your idea approved
2. Add your plugin to the [`snippets.json`](https://github.com/schooltape/schooltape/blob/main/src/snippets/snippets.json) file
3. Create your snippet
4. Submit a PR

#### Private Snippets

Snippets can also be added manually by the user, allowing users to add them on a per-Schoolbox basis. Create a snippet, following [this format](https://gist.github.com/42Willow/4555f0d8fdf8e59b479fd44539740937) and then share it with your friends! These snippets are able to be removed by the user after installation.

Make sure to include the `css` comments

- Do not use quotation marks
- Make sure it is spelt correctly
- Leave a trailing newline character

```css
/* name: Hide PFP */
/* description: Hide your profile picture across Schoolbox */
```

## Pull Request

To merge your changes into this repository you can create a pull request (PR).

Here is a handy guide on [what a pull request](https://docs.github.com/articles/about-pull-requests) is and [how to make one](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request).

---

## Contributing Guidelines

Please follow the styling and contributing guidelines outlined [here](https://github.com/schooltape/schooltape/blob/main/CONTRIBUTING.md).
