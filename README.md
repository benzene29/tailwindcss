<p align="center">
  <a href="https://tailwindcss.com" target="_blank">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/tailwindlabs/tailwindcss/HEAD/.github/logo-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/tailwindlabs/tailwindcss/HEAD/.github/logo-light.svg">
      <img alt="Tailwind CSS" src="https://raw.githubusercontent.com/tailwindlabs/tailwindcss/HEAD/.github/logo-light.svg" width="350" height="70" style="max-width: 100%;">
    </picture>
  </a>
</p>

<p align="center">
  A utility-first CSS framework for rapidly building custom user interfaces.
</p>

<p align="center">
    <a href="https://github.com/tailwindlabs/tailwindcss/actions"><img src="https://img.shields.io/github/actions/workflow/status/tailwindlabs/tailwindcss/ci.yml?branch=next" alt="Build Status"></a>
    <a href="https://www.npmjs.com/package/tailwindcss"><img src="https://img.shields.io/npm/dt/tailwindcss.svg" alt="Total Downloads"></a>
    <a href="https://github.com/tailwindcss/tailwindcss/releases"><img src="https://img.shields.io/npm/v/tailwindcss.svg" alt="Latest Release"></a>
    <a href="https://github.com/tailwindcss/tailwindcss/blob/master/LICENSE"><img src="https://img.shields.io/npm/l/tailwindcss.svg" alt="License"></a>
</p>

---

## Documentation

For full documentation, visit [tailwindcss.com](https://tailwindcss.com).

## Community

For help, discussion about best practices, or any other conversation that would benefit from being searchable:

[Discuss Tailwind CSS on GitHub](https://github.com/tailwindcss/tailwindcss/discussions)

For chatting with others using the framework:

[Join the Tailwind CSS Discord Server](https://discord.gg/7NF8GNe)

## Contributing

If you're interested in contributing to Tailwind CSS, please read our [contributing docs](https://github.com/tailwindcss/tailwindcss/blob/next/.github/CONTRIBUTING.md) **before submitting a pull request**.

## Running Tests with Coverage and SonarQube

To generate code coverage and report it to SonarQube:

1. **Install the correct coverage provider:**
   - Make sure `vitest` and `@vitest/coverage-v8` are on the same major version. For example:
     ```sh
     pnpm add -w -D vitest@latest @vitest/coverage-v8@latest
     ```

2. **Run tests with coverage:**
   ```sh
   pnpm vitest run --coverage
   ```
   This will generate a coverage report at `coverage/lcov.info`.

3. **Run SonarQube analysis:**
   ```sh
   sonar-scanner \
     -Dsonar.projectKey=tailwind \
     -Dsonar.sources=. \
     -Dsonar.host.url=http://localhost:9000 \
     -Dsonar.token=sqp_2b706011529f6dcc3ef8207723c3f86ff1c793eb \
     -Dsonar.javascript.lcov.reportPaths=packages/tailwindcss/coverage/lcov.info
   ```
   Replace `YOUR_TOKEN` with your actual SonarQube token.

---

**Troubleshooting:**
- If you see errors about version mismatches, upgrade both `vitest` and `@vitest/coverage-v8` to the latest version.
- If you use a monorepo, always install devDependencies at the workspace root with `-w`.

