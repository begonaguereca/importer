# Travis CI to Actions migrations powered by GitHub Actions Importer

The instructions below will guide you through configuring a GitHub Codespace environment that will be used in subsequent labs that demonstrate how to use GitHub Actions Importer to migrate Travis CI pipelines to GitHub Actions.

These steps **must** be completed prior to starting other labs.

## Create your own repository for these labs

1. Ensure that you have created a repository using the [actions/importer-labs](https://github.com/actions/importer-labs) as a template.

## Configure your Codespace

1. Start a new Codespace.

    - Click the `Code` with button down arrow above repository on the repository's landing page.
    - Click the `Codespaces` tab.
    - Click `Create codespaces on main` to create the codespace.
    - After the Codespace has initialized there will be a terminal present.

2. Verify the GitHub Actions Importer CLI is installed and working. More information on the GitHub Actions Importer extension for the official GitHub CLI can be found [here](https://github.com/github/gh-actions-importer).

    - Run the following command in the codespace's terminal:

      ```bash
      gh actions-importer version
      ```

    - Verify the output is similar to below.

      ```console
      $ gh actions-importer version
      gh version 2.14.3 (2022-07-26)
      gh actions-importer        github/gh-actions-importer v0.1.12
      actions-importer/cli       unknown
      ```

    - If `gh actions-importer version` did not produce similar output then please follow the troubleshooting [guide](#troubleshoot-the-actions-importer/cli).

## Labs for Travis CI

Perform the following labs to learn more about GitHub Actions migrations with GitHub Actions Importer:

1. [Configure credentials for GitHub Actions Importer](1-configure.md)
2. [Perform an audit of Travis CI](2-audit.md)
3. [Forecast potential build runner usage](3-forecast.md)
4. [Perform a dry-run of a Travis CI pipeline](4-dry-run.md)
5. [Use custom transformers to customize GitHub Actions Importer's behavior](5-custom-transformers.md)
6. [Perform a production migration of a Travis CI pipeline](6-migrate.md)

## Troubleshoot the GitHub Actions Importer CLI

The CLI extension for GitHub Actions Importer can be manually installed by following these steps:

- Verify you are in the codespace terminal
- Run this command from within the codespace's terminal:

  ```bash
  gh extension install github/gh-actions-importer
  ```

- Verify the result of the install contains:

  ```console
  $ gh extension install github/gh-actions-importer
  ✓ Installed extension github/gh-actions-importer
  ```

- If you get an error similar to the image below, then click the link in the terminal output to authorize the token.
  - Restart the codespace after clicking the link.
  ![img](https://user-images.githubusercontent.com/26442605/169588015-9414404f-82b6-4d0f-89d4-5f0e6941b029.png)
- Verify GitHub Actions Importer CLI extension is installed and working by running the following command from the codespace's terminal:

  ```bash
  gh actions-importer version
  ```
