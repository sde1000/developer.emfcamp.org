# developer.emfcamp.org

These are the source files for <https://developer.emfcamp.org>.

The site is statically generated using [Hugo](https://gohugo.io) and the [Docsy theme](https://www.docsy.dev).

If you're just here to edit page content, what you need is in the [`content/docs/` subdirectory](content/docs/).

## How to preview and build the site locally

Although the site is built with Hugo, the required versions of Hugo and
associated tooling are intended to be obtained as npm packages.  This ensures
the correct version of Hugo is being used for the Docsy theme (which is quite
picky about Hugo versions).

There are various ways to install Hugo, but Docsy does require the 'extended'
build of Hugo, and all the other npm packages are required to build the site
anyway, e.g. to process JavaScript and styles for publication.  Therefore it's
recommended to just get all your dependencies through npm to match how it's
done with success in the live site deployment.

### Required software

Install these however you like.

* Node.js 24
* npm 11 (check with `npm --version` once you have Node 24 installed)
* Go 1.14+ (this is used by Hugo internally)

### Commands you can run

After the required software are installed, install all the dependencies with `npm clean-install` (shorthand: `npm ci`).

Start the auto-reloading Hugo dev server with `npm run dev`.

If you want to supply extra arguments to `hugo server`, do so like `npm run dev -- --extra-args --go-here`.

You can build the site for production as it's done in GitHub Actions with `npm run build`.
