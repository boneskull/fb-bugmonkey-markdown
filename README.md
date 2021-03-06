# BugMonkey Markdown

[BugMonkey](https://help.fogcreek.com/7585/customizing-your-fogbugz-site-with-bugmonkey) customization for FogBugz which allows for [Markdown](https://daringfireball.net/projects/markdown/) in case editor.

Observe:

![bugmonkey-markdown-example](http://goo.gl/Lpcajy)

## Prerequisites

1.  You **need** [FogBugz](http://www.fogcreek.com/fogbugz/).
2.  You **must** be using the desktop version of the FogBugz site.
3.  You need IE9+, FF14+, Chrome 18+, Safari 6+, Opera 15+, or...
4.  for mobile browser compatibility, see [here](http://caniuse.com/mutationobserver).

## Installation

1.  Create a new Customization in FogBugz.
2.  Paste the contents of `dist/bugmonkey-markdown.min.txt` into the customizations editor.
3.  Enable the Customization for yourself.
4.  Save, refresh a case page, and you should be ready to go.

## Usage

Here's an example of altering the CodeMirror CSS:

```js
localStorage['BugMonkey.Markdown.THEME_URL'] = '//cdnjs.cloudflare.com/ajax/libs/codemirror/3.21.0/theme/solarized.min.css';
localStorage['BugMonkey.Markdown.THEME_NAME'] = 'solarized';
```

Now, next time you refresh, you will use this custom theme.

*This behavior is slated to change in `v1.2.0`*

## Debugging

Paste `dist/bugmonkey-markdown.txt` into the editor instead.

## Development

You might want to do this if you hate the CSS I picked, or want some other fancy CodeMirror feature.

1.  Execute `npm install`
2.  Make edits to any/all of the following:
  1.  `./bugmonkey-markdown.js`
  2.  `./bugmonkey-markdown.css`
  3.  `./header.txt`
3.  Execute `grunt` to output `bugmonkey-markdown.txt` and `bugmonkey-markdown.min.txt` into the `dist/` directory.
4.  Alternatively, execute `grunt watch` before you start fiddling with files and the `dist/*.txt` files will be created automatically.
5.  Paste the contents of one of the files in the `dist/` directory back into FogBugz.  Save, refresh, rinse, repeat.

### Dependencies

BugMonkey Markdown leverages:

* [Showdown](https://github.com/coreyti/showdown)
* [CodeMirror](http://codemirror.net/)
* [jquery.preempt](http://boneskull.github.io/jquery.preempt)
* [Showdown FogBugz extension](https://github.com/boneskull/showdown-fogbugz)

IE9 and IE10 support courtesy [Mutation Observers Polyfill](http://goo.gl/yRyxCK) from the [Dart](http://dart-lang.org) project.

## License

MIT

## Author
[Christopher Hiller](http://boneskull.github.io)
