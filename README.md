# FIO Developer Hub

This repository houses documentation for the [FIO Protocol](https://fioprotocol.io).

The [docs are written in markdown](docs), processed by [Docusaurus](https://docusaurus.io/), and hosted at the FIO
[Developer Hub](https://ericbutz.github.io/fio-developer-hub/).

## Contributing

Thank you for your interest in contributing to the Developer Hub. Please review our contributor guidelines prior to any contribution. 
If you have any further questions, don't hesitate to reach out on our community channels. 

### Directory Structure

This repository is structured as a Docusaurus project with the markdown files organized in the `/docs` directory. Images
and other assets are in the `/docs/assets/` directory. The `/website` directory is a Yarn Docusaurus project with many
helpful scripts (e.g. `yarn build`, `yarn start`) for working with this codebase.  In the `/website` directory you will
find [`sidebars.json`](https://docusaurus.io/docs/en/navigation) and
[`siteConfig.js`](https://docusaurus.io/docs/en/site-config), which are important Docusaurus files. You will find the
source code for some top-level pages in `/website/pages/en`. Follow our [contribution guidelines](CONTRIBUTING.md).

### Adding a new document

To add a new markdown document:

* Create your markdown document in a suitable directory inside `/docs`.
* If you have images in your document, put them in the `/docs/assets/` directory.
* Documentation should follow our [contribution guidelines](CONTRIBUTING.md).
* If you want your document to appear in the sidebar, add its reference in the `/website/sidebar.json` file under the
  corresponding section.

### Local Testing

* `cd` into the `/website` directory.
* Execute `yarn install` and then `yarn start`.

The FIO Developer Hub website should open in a browser window.

#### Link Checker

Once the website is running, you should use the included Yarn script (`yarn check-links`) to ensure that your changes
do not introduce any broken links and to check for any links that have broken since the last time the check was
executed. Please ensure all links are fixed before submitting any changes.

Once you are done with your changes, feel free to submit a PR.
