# Contributing

Welcome, and thank you for your interest in contributing to the FSR website! Whether you're fixing a typo, adding content, or implementing new features, your help is appreciated. Before getting started, please read through this guide to ensure a smooth contribution process.

## Build the website yourself

First, clone the website locally. You can do this by installing [Git](https://git-scm.com/downloads) and then running:

```sh
git clone https://git.fsinf.informatik.uni-leipzig.de/fsinf/website-25.git
```

To build the website, you need to have [Node.js](https://nodejs.org/en/download) installed.

If you have Nix installed, you can alternatively install all required packages in your development shell by running:

```sh
nix-shell
```

Finally run:

```sh
npm install
```

to install all packages. That's it!

## Commit Messages

Write your commit messages **in English only**! Please use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/).
Your commit messages should follow this structure:

- feat: add your cool new feature
- fix: fix a bug
- docs: add or improve documentation
- style: reformat code (no logic changes)

## Testing changes

You should **ALWAYS** test your changes before pushing them!
To test them locally, run the following command in your terminal:

```sh
npm run dev
```

You can now see your changes at port `4321`. When you make changes locally, they will automatically be rebuilt. The command output should look like this:

```md
> apparent-azimuth@0.0.1 dev
> astro dev

12:47:09 [types] Generated 1ms
12:47:09 [content] Syncing content
12:47:10 [content] Synced content

astro v5.13.5 ready in 1828 ms

┃ Local http://localhost:4321/
┃ Network use --host to expose

12:47:10 watching for file changes...
```

## Format your files

Before pushing your files, run:

```sh
treefmt
```

to format all files properly.
If you don't have treefmt installed, you can do so via Nix (in nix-shell) or manually by following the [installation guide](https://numtide.github.io/treefmt/).

### Pre-Push checklist

- [ ] I tested the website locally with `npm run dev`
- [ ] I followed the commit message conventions
- [ ] I formatted my code using `treefmt`

If you've completed this checklist, you can push your changes to GitLab by running:

```sh
git push origin main
```

This will trigger the workflow and rebuild the website.
Your changes should be live shortly!
