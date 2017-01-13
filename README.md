# erc-spec

Executable Research Compendium (ERC) specification and guides

Project description: [http://o2r.info](http://o2r.info)

**Read online: [http://o2r.info/erc-spec](http://o2r.info/erc-spec)**

## Guidelines

See [CONTRIBUTING.md](CONTRIBUTING.md)

## Build

This specification is written in [Markdown](https://daringfireball.net/projects/markdown/), rendered with [MkDocs](http://www.mkdocs.org/) and deployed automatically using Travis CI.

[![Build Status](https://travis-ci.org/o2r-project/o2r-web-api.svg?branch=master)](https://travis-ci.org/o2r-project/o2r-web-api)

Use `mkdocs` to render it locally.

```bash
# pip install mkdocs mkdocs-cinder
mkdocs serve
```

### Automated Builds

Our combination of the `.travis.yml` and `.deploy.sh` will run the `mkdocs` command on every direct commit or merge on the master branch and deploy the rendered HTML documents to the `gh-pages` branch in this repository.

Travis authenticates its push to the `gh-pages` branch using a [personal access token](https://github.com/settings/tokens) of the user [@o2r-user](https://github.com/o2r-user), who has write access to this repository.
The access token is encrypted in the `.travis.yml` [using Travis CLI](https://docs.travis-ci.com/user/encryption-keys/):

```bash
travis encrypt GH_TOKEN=<token here>
```

The variable `GH_TOKEN` is used in the deploy script.
The token generated on the GitHub website should not be stored anywhere, simply generate a new one if needed.

This has some security risks, as described [here](https://gist.github.com/domenic/ec8b0fc8ab45f39403dd#sign-up-for-travis-and-add-your-project).
To mitigate these risks, the option "Build pull requests" on the [Travis configuration page for this repo](https://travis-ci.org/o2r-project/erc-spec/settings) must be disabled so that malicious changes to the Travis configuration file will not be build before maintainer inspection.

## License

The o2r Executable Research Compendium specification is licensed under [Creative Commons CC0 1.0 Universal License](https://creativecommons.org/publicdomain/zero/1.0/), see file `LICENSE`.
To the extent possible under law, the people who associated CC0 with this work have waived all copyright and related or neighboring rights to this work.
This work is published from: Germany.
