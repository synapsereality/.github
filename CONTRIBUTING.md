# Contributing

Thanks for looking. Bug reports, fixes and small features are welcome in every
repo here. For anything bigger, open an issue first so we can agree the shape
before you write it.

## Reporting a bug

Open an issue with the bug form. Include the command you ran, the version
(`aeb --version`, `one-hop --version` or `npx answer-crawler-check --version`) and
the output. If a public URL shows the problem, include it.

## Making a change

1. Fork the repo and branch from `main`.
2. Run the checks before you push. They are the same ones CI runs.

   Python repos (answer-engine-benchmark, one-hop):

   ```bash
   pip install -e ".[test]" ruff
   ruff check .
   pytest -q
   ```

   answer-crawler-check:

   ```bash
   npm test
   ```

3. Add a test for the behaviour you changed. The tests never call a real API or
   a real site, so they need no keys and no network.
4. Open a pull request against `main`. Say what changed and how you checked it.

`main` only takes pull requests, and CI has to pass before one can merge. We
squash-merge, so the pull request title becomes the commit message.

## Licence

Everything here is MIT licensed. By opening a pull request you agree that your
change is released under the same licence.

## Conduct

Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).
Report problems to ben@synapsereality.io.
