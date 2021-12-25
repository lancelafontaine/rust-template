# Rust Github Template

A template for [cargo generate](https://github.com/cargo-generate/cargo-generate) that is the starting point for all of [@lancelafontaine](https://github.com/lancelafontaine)'s Rust projects on GitHub.

This template was originally forked from [`rust-github`'s template](https://github.com/rust-github/template) and customized for my projects.

See the [`rust-github`'s website](https://rust-github.github.io) for details on setting up a new project.

## Getting Started

- Install or update `cargo-generate`.

```
cargo install cargo-generate
```

- Generate a new project from this template. This command will prompt you for a project name, project description, and GitHub username.

```
cargo generate --git https://github.com/lancelafontaine/rust-template.git
```

- Create a new empty GitHub repository and follow the instructions to push the newly-created local repository to Github.

- Protect the main branch, require a pull request to the repository before merging, and rrequire status checks to pass before merging.

- Set up your [crates.io token](https://doc.rust-lang.org/cargo/reference/publishing.html) in a [GitHub secret](https://docs.github.com/en/actions/security-guides/encrypted-secrets) called `CARGO_API_KEY`.


## Publishing

When you are ready to publish a version of your application (eg. `0.1.0`), run:

```
git tag -a 0.1.0
git push --follow-tags
```

This tag should trigger the continuous deployment which will publish your application on crates.io and publish the binaries on GitHub Releases.

