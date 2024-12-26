# Locale help

Locales help that explains how people can translate this project into worldwide languages.


## Locale subdirectory names

Each locale subdirectory should be named using a standard locale code.

If possible, use the ISO 639-1 two-letter language codes.

Examples:

* `locales/en/` is for English

* `locales/zh/` is for Chinese

* `locales/hi/` is for Hindi

* `locales/es/` is for Spanish

* `locales/ar/` is for Arabic

For a list of ISO 639-1 codes:

* [https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)


## Content subdirectory names

Content subdirectory names should be translated into their corresponding languages.

Examples:

* `locales/en/hello/`

* `locales/zh/你好/`

* `locales/hi/नमस्ते/`

* `locales/es/hola/`

* `locales/ar/مرحبًا/`


## Slug format

Content subdirectory names should use a slug format, which means a format that is user-friendly for copying, pasting, typing, and browsing. 

Example:

* `locales/en/hello-world`


### Slug format for English

Our slug format for English is alphanumeric lowercase characters plus a separator which is the hyphen-minus character.

Right:

* `locales/en/hello-world`

Wrong:

* `locales/en/Hello-World` (because it uses uppercase letters)

* `locales/en/hello world` (because it uses a space)

* `locales/en/hello+world` (because it uses a symbol)


## locale peer id

This project keeps track of corresponding content across multiple locales by using the computer science technique named "locale peer id".

A locale peer id is a secure randomly-generated 32-character lowercase hexadecimal string.

For example:

* abc7c72d426bc75e40b25a44ae37ce73

* 9f8b29ae5b4a937f8865e87e3e0ea9f8

* b82232cff8e5bb785fbc855b65a83653


## .local-peer-id file

Each directory contains a file named `.locale-peer-id` that contains the locale peer id.

When anyone translates any project directory from one language into another, then the locale peer id is identical. 

For example each directory below contains a file named `.locale-peer-id` and each file contains the identical locale peer id:

* `locales/en/hello/.local-peer-id`

* `locales/zh/你好/.local-peer-id`

* `locales/hi/नमस्ते/.locale-peer-id`

* `locales/es/hola/.locale-peer-id`

* `locales/ar/مرحبًا/.locale-peer-id`

If you want to create a translation of a directory and its contents, you must use the same locale peer id and put in a file named `.locale-peer-id`, because this is what's necessary for the project team to track translations across languages.


###  For programmers

If you are a programmer, then see these tools which may help you:

* [bin/locale-peer-id](bin/locale-peer-id): generate a locale peer id

* [bin/grep-locale-peer-id](bin/grep-locale-peer-id): find files that contain a given locale peer id

* [bin/markdown-read-to-headline](bin/markdown-read-to-headline): markdown tool to read a file or stdin, then print the first headline

* [bin/slug-case](bin/slug-case): input a line of text; output the text converted to slug case
