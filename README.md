This is an example repo to go along with this ['how to' article](https://codeburst.io/testing-mocking-http-requests-with-nock-480e3f164851).

It uses [Nock](https://github.com/nock/nock) alongside a [Random User API](https://randomuser.me/documentation).

#### Linting:

For linting [eslint-config-skyscanner](https://github.com/Skyscanner/eslint-config-skyscanner ) has been used, along with [prettier](https://github.com/prettier/prettier). This is not included in each directory, if you wish to add it duplicate the [.eslintrc](.eslintrc) and [.prettierrc](.prettierrc) and run:

```sh
(
    export PKG=eslint-config-skyscanner;
    npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev
    "$PKG@latest"
)
```
to setup eslint, and then the following to integrate prettier:
```sh
npm install -D eslint-config-prettier eslint-plugin-prettier prettier
```
