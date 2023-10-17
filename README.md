# Description

This repository contains a slightly modified copy of ([**the released version**](https://github.com/samclarke/SCEditor/releases/download/v3.2.0/sceditor-3.2.0.zip)) of [SCEditor 3.2.0](https://github.com/samclarke/SCEditor/releases/tag/v3.2.0) with enabled **[`alternative-lists` plugin](https://github.com/samclarke/SCEditor/pull/691)**

# Usage

1. Download this repository:

   1. Click on the green “<> Code” button
   2. Click on “Download ZIP”

2. Extract the zip file
3. Either:

   - Click on `Online.html` to open a text editor that uses the **current online version of SCEditor**
   - Click on `Local.html` to open a text editor that uses the **local version of SCEditor** (`3.2.0`)

**Alternatively** you can just download `Online.html`:

1. Click [here](https://raw.githubusercontent.com/MyTooliT/SCEditor/main/Online.html)
2. Save the file somewhere
3. Open the downloaded file in your favorite browser

# Notes

- Please **do not do what I did here** 😅
- This is just a quick and dirty way to provide an editor that supports the [alternative BB code syntax for lists](https://helpdesk.bitrix24.com/open/8948499/) (that Bitrix24 uses) for a coworker
- I am **not** a web developer
- I know my (mostly) copy and pasted code is most probably absolutely horrible 😇

---

# [SCEditor](http://www.sceditor.com/)

[![Build Status](https://github.com/samclarke/SCEditor/workflows/Node.js%20CI/badge.svg)](https://travis-ci.org/samclarke/SCEditor)
[![SemVer](http://img.shields.io/:semver-✓-brightgreen.svg)](http://semver.org)
[![License](http://img.shields.io/npm/l/sceditor.svg)](https://github.com/samclarke/SCEditor/blob/master/LICENSE.md)

A lightweight WYSIWYG BBCode and XHTML editor.

[![SCEditor preview](https://cdn.rawgit.com/samclarke/SCEditor/49c696b8/preview.svg)](https://www.sceditor.com/)

For more information visit [sceditor.com](http://www.sceditor.com/)

## Usage

Include the SCEditor JavaScript:

```html
<link rel="stylesheet" href="minified/themes/default.min.css" />
<script src="minified/sceditor.min.js"></script>
<script src="minified/formats/bbcode.js"></script>
<script src="minified/formats/xhtml.js"></script>
```

Then to convert a textarea into SCEditor, simply do:

```js
var textarea = document.getElementById("id-of-textarea");

sceditor.create(textarea, {
  format: "xhtml",
  style: "minified/themes/content/default.min.css",
});
```

or for a BBCode WYSIWYG editor do:

```js
var textarea = document.getElementById("id-of-textarea");

sceditor.create(textarea, {
  format: "bbcode",
  style: "minified/themes/content/default.min.css",
});
```

Finally, to get the contents of the editor:

```js
var textarea = document.getElementById("id-of-textarea");

sceditor.instance(textarea).val();
```

## Options

For a full list of options, see the [options documentation](http://www.sceditor.com/documentation/options/).

## Building and testing

You will need [Grunt](http://gruntjs.com/) installed to run the build/tests. To install Grunt run:

```bash
npm install -g grunt-cli
```

Next, to install the SCEditor dev dependencies run:

```bash
npm install
```

That's it! You can now build and test SCEditor with the following commands:

```bash
# Minify the JS and convert the LESS to CSS
grunt build

# Run the linter, unit tests and coverage
grunt test

# Creates the final distributable ZIP file
grunt release
```

You can also run the dev server to test changes without having to do a full
build by running:

```bash
npm run dev
```

and then going to http://localhost:9000/tests/

## Contribute

Any contributions and/or pull requests would be welcome.

Themes, translations, bug reports, bug fixes and donations are greatly appreciated.

## Donate

If you would like to make a donation you can via
[PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=AVJSF5NEETYYG)
or via [Flattr](http://flattr.com/thing/400345/SCEditor)

## License

SCEditor is licensed under the [MIT](/LICENSE.md) license:

Copyright (C) 2011 - 2017 Sam Clarke and contributors – sceditor.com

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Credits

**Nomicons: The Full Monty Emoticons by:**
Oscar Gruno, aka Nominell v. 2.0 -> oscargruno@mac.com
Andy Fedosjeenko, aka Nightwolf -> bobo@animevanguard.com

**Icons by:**
Mark James (http://www.famfamfam.com/lab/icons/silk/)
Licensed under the [Creative Commons CC-BY license](http://creativecommons.org/licenses/by/3.0/).
