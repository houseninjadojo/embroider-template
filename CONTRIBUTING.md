### CONTRIBUTING TO EMBER ABSTRACT DROPDOWN

#### TABLE OF CONTENTS

- [CONTRIBUTING TO EMBER ABSTRACT DROPDOWN](#contributing-to-ember-abstract-dropdown)
	- [TABLE OF CONTENTS](#table-of-contents)
	- [GETTING THE CODE](#getting-the-code)
	- [SETTING UP THE ENVIRONMENT](#setting-up-the-environment)
		- [Generating the GPG Key](#generating-the-gpg-key)
		- [Setting up Git Config Locally](#setting-up-git-config-locally)
	- [BUILDING AND TESTING](#building-and-testing)

#### GETTING THE CODE

```
git clone https://github.com/houseninjadojo/embroider-template
cd embroider-template
npm i
```

#### SETTING UP THE ENVIRONMENT

##### Generating the GPG Key

[Embroider Template](https://github.com/houseninjadojo/embroider-template) requires that every commit be signed before it is accepted for merging into the main branch prior to release.

All contributors are expected to create a GPG Key and use it to sign all their commits during the development process.
At the very minimum, all _Pull Requests_ are expected to be signed by the contributors' GPG Key prior to being accepted.

Please follow the Github guide on [Managing commit signature verification](https://help.github.com/en/github/authenticating-to-github/managing-commit-signature-verification) for instructions on how to get this done.

##### Setting up Git Config Locally

```
git config commit.gpgsign true

git config trailer.sign.key "Signed-off-by: "
git config trailer.sign.ifmissing add
git config trailer.sign.ifexists doNothing
git config trailer.sign.command 'echo "$(git config user.name) <$(git config user.email)>"'

git config user.name "YOUR NAME"
git config user.email "your.name@twyr.com"
git config user.signingKey "GPG Key Id"
```

#### BUILDING AND TESTING

| Operation                 | NPM Script / Command             |
| ------------------------- | -------------------------------- |
| Building Everything       | npm run build --workspaces       |
| Clean Building Everything | npm run build:clean --workspaces |
| Linting                   | npm run lint --workspaces        |
| Linting with fixes        | npm run lint:fix --workspaces    |
| Running the Tests         | npm run test --workspaces        |
|                           |                                  |
