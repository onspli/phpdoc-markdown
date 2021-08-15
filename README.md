# phpdoc markdown template

[phpDocumentor](https://phpdoc.org/) template that generates Markdown documentation of the **public API** only to a **single README.md file**. It will skip all abstract classes and non-public methods. Fork of template [cvuorinen/phpdoc-markdown-public](https://github.com/cvuorinen/phpdoc-markdown-public) by Carl Vuorinen.

The main use-case for this template is to generate simple and nice looking usage documentation, that can then be published on GitHub.

For example, a small library can document it's public API in DocBlock comments, use this template to generate the Markdown documentation and then commit it to GitHub with the library to easily create a nice looking documentation for other developers to see.

Example of documentation generated with this template: https://github.com/onspli/chess/tree/master/docs

## Installation

Install with Composer:

```bash
composer require onspli/phpdoc-markdown-public
```

## Usage

First, you need to install phpDocumentator. There are multiple options how to install it, one of them is using the PHAR:
```bash
$ wget https://phpdoc.org/phpDocumentor.phar
```
Read more about [installation of phpDocumentator](https://phpdoc.org/). Note that phpDocumentator is also available via Composer, however its documentation states
> Ah, you discovered our secret. There is a phpDocumentor composer package that you could use to install phpDocumentor.
>
> However: phpDocumentor is a complex application, and its libraries are used in countless other libraries and applications (2 of our libraries have more than 150 million downloads each); and this means that the chances for a conflict between one of our dependencies and yours is high. And when I say high, it is really high.
> 
> So, because of the above: we do not endorse nor actively support installing phpDocumentor using Composer.

Next, run phpDocumentor and set template as `vendor/onspli/phpdoc-markdown-public/data/templates/markdown-public`.

```bash
$ phpDocumentator.phar --directory=src/ --target=docs/ --template="vendor/onspli/phpdoc-markdown-public/data/templates/markdown-public" --title="My Project Documentation"
```
The documentation will be generated to `docs/README.md` file.

More information about [configuring phpDocumentor](https://docs.phpdoc.org/3.0/guide/references/configuration.html).
