# github-demo
sample test with WSL
```
ddd
```


CakePHP Documentation
=====================

This is the official documentation for the CakePHP project. It is available online in HTML, PDF and EPUB formats at http://book.cakephp.org.

Requirements
------------

You can read all of the documentation within as its just in plain text files, marked up with ReST text formatting.  To build the documentation you'll need the following:

* Make
* Python
* Sphinx
* PhpDomain for sphinx

You can install sphinx using:

	easy_install sphinx

You can install the phpdomain using:

	easy_install sphinxcontrib-phpdomain

*To run the easy_install command, the setuptools package must be previously installed.*

Building the documentation
--------------------------

After installing the required packages, you can build the documentation using `Make`.

	# Create all the HTML docs. Including all the languages.
	make html
	
	# Create just the english HTML docs.
	make html-en
	
	# Create all the EPUB (e-book) docs.
	make epub
	
	# Create just the engish EPUB docs.
	make epub-en

	# Populate the search index
	make populate-index

This will generate all the documentation in an html form.  Other output such as 'pdf' and 'htmlhelp' are not fully complete at this time.

After making changes to the documentation, you can build the html version of the docs by using `make html` again.  This will build only the html files that have had changes made to them.


Contributing
------------

Contributing to the documentation is pretty simple. Please read the documentation on contributing to the documentation over on [the cookbook](http://book.cakephp.org/2.0/en/contributing/documentation.html) for help.

There are currently a number of outstanding issues that need to be addressed.  We've tried to flag these with `.. todo::` where possible.  To see all the outstanding todo's add the following to your `config/all.py`

	todo_include_todos = True

After rebuilding the html content, you should see a list of existing todo items at the bottom of the table of contents.

You are also welcome to make and suggestions for new content as commits in a github fork.  Please make any totally new sections in a separate branch.  This makes changes far easier to integrate later on.

Translations
------------

Contributing translations requires that you make a new directory using the two letter name for your language.  As content is translated, directories mirroring the english content should be created with localized content.


Generating Meta tags
--------------------

If you are providing translations and want to automatically generate meta tags for the resulting html files, a MetatagShell is provided in
the `scripts` folder of this repo. In order to use it, copy it into any CakePHP 2.0 empty application inside `app/Console/Command`, execute
`Console/cake metatag` and follow the instructions.

The script will process all the files under one of the translation folders and generate the possible description terms using an external API, 
it is a good idea to go over the generated terms and clean-up whatever noise it might have generated.

Making search work locally
--------------------------

* Install elasticsearch.  This varies based on your platform, but most
  package managers have a package for it.
* Clone the [docs_search](https://github.com/cakephp/docs_search) into a
  web accessible directory.
* Modify `searchUrl` in `themes/cakephp/static/app.js` to point at the
  baseurl for your docs_search clone.
* Start elasticsearch with the default configuration.
* Populate the search index using `make populate-index`.
* You should now be able to search the docs using elasticsearch.



# [React](https://react.dev/) &middot; [![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/facebook/react/blob/main/LICENSE) [![npm version](https://img.shields.io/npm/v/react.svg?style=flat)](https://www.npmjs.com/package/react) [![(Runtime) Build and Test](https://github.com/facebook/react/actions/workflows/runtime_build_and_test.yml/badge.svg)](https://github.com/facebook/react/actions/workflows/runtime_build_and_test.yml) [![(Compiler) TypeScript](https://github.com/facebook/react/actions/workflows/compiler_typescript.yml/badge.svg?branch=main)](https://github.com/facebook/react/actions/workflows/compiler_typescript.yml) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://legacy.reactjs.org/docs/how-to-contribute.html#your-first-pull-request)

React is a JavaScript library for building user interfaces.

* **Declarative:** React makes it painless to create interactive UIs. Design simple views for each state in your application, and React will efficiently update and render just the right components when your data changes. Declarative views make your code more predictable, simpler to understand, and easier to debug.
* **Component-Based:** Build encapsulated components that manage their own state, then compose them to make complex UIs. Since component logic is written in JavaScript instead of templates, you can easily pass rich data through your app and keep the state out of the DOM.
* **Learn Once, Write Anywhere:** We don't make assumptions about the rest of your technology stack, so you can develop new features in React without rewriting existing code. React can also render on the server using [Node](https://nodejs.org/en) and power mobile apps using [React Native](https://reactnative.dev/).

[Learn how to use React in your project](https://react.dev/learn).

## Installation

React has been designed for gradual adoption from the start, and **you can use as little or as much React as you need**:

* Use [Quick Start](https://react.dev/learn) to get a taste of React.
* [Add React to an Existing Project](https://react.dev/learn/add-react-to-an-existing-project) to use as little or as much React as you need.
* [Create a New React App](https://react.dev/learn/start-a-new-react-project) if you're looking for a powerful JavaScript toolchain.

## Documentation

You can find the React documentation [on the website](https://react.dev/).

Check out the [Getting Started](https://react.dev/learn) page for a quick overview.

The documentation is divided into several sections:

* [Quick Start](https://react.dev/learn)
* [Tutorial](https://react.dev/learn/tutorial-tic-tac-toe)
* [Thinking in React](https://react.dev/learn/thinking-in-react)
* [Installation](https://react.dev/learn/installation)
* [Describing the UI](https://react.dev/learn/describing-the-ui)
* [Adding Interactivity](https://react.dev/learn/adding-interactivity)
* [Managing State](https://react.dev/learn/managing-state)
* [Advanced Guides](https://react.dev/learn/escape-hatches)
* [API Reference](https://react.dev/reference/react)
* [Where to Get Support](https://react.dev/community)
* [Contributing Guide](https://legacy.reactjs.org/docs/how-to-contribute.html)

You can improve it by sending pull requests to [this repository](https://github.com/reactjs/react.dev).

## Examples

We have several examples [on the website](https://react.dev/). Here is the first one to get you started:

```jsx
import { createRoot } from 'react-dom/client';

function HelloMessage({ name }) {
  return <div>Hello {name}</div>;
}

const root = createRoot(document.getElementById('container'));
root.render(<HelloMessage name="Taylor" />);
```

This example will render "Hello Taylor" into a container on the page.

You'll notice that we used an HTML-like syntax; [we call it JSX](https://react.dev/learn#writing-markup-with-jsx). JSX is not required to use React, but it makes code more readable, and writing it feels like writing HTML.

## Contributing

The main purpose of this repository is to continue evolving React core, making it faster and easier to use. Development of React happens in the open on GitHub, and we are grateful to the community for contributing bugfixes and improvements. Read below to learn how you can take part in improving React.

### [Code of Conduct](https://code.fb.com/codeofconduct)

Facebook has adopted a Code of Conduct that we expect project participants to adhere to. Please read [the full text](https://code.fb.com/codeofconduct) so that you can understand what actions will and will not be tolerated.

### [Contributing Guide](https://legacy.reactjs.org/docs/how-to-contribute.html)

Read our [contributing guide](https://legacy.reactjs.org/docs/how-to-contribute.html) to learn about our development process, how to propose bugfixes and improvements, and how to build and test your changes to React.

### [Good First Issues](https://github.com/facebook/react/labels/good%20first%20issue)

To help you get your feet wet and get you familiar with our contribution process, we have a list of [good first issues](https://github.com/facebook/react/labels/good%20first%20issue) that contain bugs that have a relatively limited scope. This is a great place to get started.

### License

React is [MIT licensed](./LICENSE).
