# prettier-config-nahid

##### My sharable and pluggable Prettier configuration.

## Contents

-   [`wp-prettier`](https://www.npmjs.com/package/wp-prettier) (as [`prettier`](https://www.npmjs.com/package/prettier))
-   [`@wordpress/prettier-config`](https://www.npmjs.com/package/@wordpress/prettier-config)

## Features

-   Formats code using [Prettier](https://www.npmjs.com/package/prettier).

## Requirements

-   [NodeJS](https://nodejs.org/en/) ( >=12.0.0 )
-   [NPM](https://www.npmjs.com/) ( >=6.14.5 )

## Installation

1. If your project doesn't have a `package.json` file already, create one using the [`npm init` command](https://docs.npmjs.com/cli-commands/init.html).
2. Run the command: `npx install-peerdeps --dev prettier-config-nahid`
3. In your `package.json` file, reference the config using the `prettier` property, in the following way;

```json
"prettier": "prettier-config-nahid"
```

Learn more about using shareable Prettier config [here](https://prettier.io/docs/en/configuration.html#sharing-configurations).

## Usage

1. You can try running the following command `prettier --check .` to run Prettier. Look at Prettier's command-line interface guide [here](https://prettier.io/docs/en/cli.html).
2. I prefer adding two scripts to the `package.json` file:

```json
"scripts": {
	"format": "prettier --check \"**/*.{html,json,md}\"",
	"format:fix": "prettier --write \"**/*.{html,json,md}\""
}
```

That way, I can run `npm run format` and `npm run format:fix` to check formatting and check/format all the HTML, JSON, and MD files in the codebase.

The documentation for Prettier as a whole can be found [here](https://prettier.io/docs/en/install.html).

## FAQ

#### Why [`wp-prettier`](https://www.npmjs.com/package/wp-prettier)?

I started my career in software development with WordPress, and I'm really fond of the coding standards WordPress has been enforcing recently. I've been using them for quite a very long time now and I'm very used to them, which is why I like to carry them onto my other (non-WordPress) projects as well. You should also see that this config includes [`@wordpress/prettier-config`](https://www.npmjs.com/package/@wordpress/prettier-config) carrying over coding standards from the WordPress ecosystem.

My Prettier config uses [`wp-prettier`](https://www.npmjs.com/package/wp-prettier) as `prettier`. [`wp-prettier`](https://www.npmjs.com/package/wp-prettier) is a fork of `prettier` created by my folks at WordPress. It adds a new command line option `--paren-spacing` which inserts extra spaces inside parentheses, the way how projects in the WordPress ecosystem, and I like to format their code.
