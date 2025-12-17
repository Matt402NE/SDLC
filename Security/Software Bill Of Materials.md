# # (Draft) Software Bill Of Materials (SBOM)




## Integrating with GitHub Actions

To automate SBOM generation as part of your CI/CD workflow, you can use a GitHub Action. This ensures the SBOM is always up-to-date with your builds. 

- **GitHub's built-in action**: You can use the [official sbom-generator action](https://github.com/jhutchings1/sbom-generator) which leverages the Dependency Graph API.
