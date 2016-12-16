# Changes

Generate a changelog as part of the [npm version command][1].

## Usage

- Use `npm version [patch|minor|major]` to create a release
- Your editor will open with a generated `CHANGES.md` file
- When you're done writing the release notes, save and close the editor to
  continue
- To abort the release, remove the heading with the new version number

## Install

```bash
$ npm install @studio/changes --save-dev
```

## Configure

Add this to your `package.json`:

```json
{
  "scripts": {
    "preversion": "npm test",
    "version": "changes",
    "postversion": "git push --follow-tags && npm publish"
  },
  "devDependencies": {
    "@studio/changes": "^1.0.0"
  }
}
```

Configure your preferred editor with the `$EDITOR` environment variable.

![](https://javascript.studio/assets/changes-1.0.gif)

## License

MIT

<div align="center">Made with ❤️ on 🌍</div>

[1]: https://docs.npmjs.com/cli/version
