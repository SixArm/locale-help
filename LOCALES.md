# Locales

Locales help people translate this project into multiple worldwide languages.


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

* <https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes>


## Content subdirectory names

Content subdirectory names should be translated into their corresponding languages.

Examples:

* `locale/en/hello/`

* `locale/zh/你好/`

* `locales/hi/नमस्ते/`

* `locales/es/hola/`

* `locales/ar/مرحبًا/`


## Slug format

Content subdirectory names should use a slug format, which means a format that is user-friendly for copying, pasting, typing, and browsing. 

Our preferred slug format for English is alphanumeric lowercase with separators that are dashes that are hyphen-minus characters.

Right:

* `locale/en/alpha-bravo-charie`

Wrong:

* `locale/en/Alpha-Bravo-Charlie` (because it uses mixed case)

* `locale/en/alpha bravo charlie` (because it uses spaces)

* `locale/en/alpha@bravo@charlie` (because it uses symbols)

* `locale/en/alphabravocharlie` (because it doesn't use separators)


## locale peer id

This project keeps track of corresponding content across multiple locales by using the computer science technique named "locale peer id".

A locale peer id is a secure randomly-generated 32-character lowercase hexadecimal string.

For example:

* abc7c72d426bc75e40b25a44ae37ce73

* 9f8b29ae5b4a937f8865e87e3e0ea9f8

* b82232cff8e5bb785fbc855b65a83653

A locale peer id is NOT a UUID, beacuse a locale peer id is totally random on purpose.

For example one way to generate a locale peer id is this shell command:

```sh
printf "%s\n" $(LC_ALL=C < /dev/urandom tr -dc '0-9a-f' | head -c32 )
```

## .local-peer-id file

Each directory contains a file named `.locale-peer-id` that contains the locale peer id.

When anyone translates any project directory from one language into another, then the locale peer id is identical. 

For example each directory below contains a file named `.locale-peer-id` and each file contains the identical locale peer id:

* `locale/en/hello/.local-peer-id`

* `locale/zh/你好/.local-peer-id`

* `locales/hi/नमस्ते/.locale-peer-id`

* `locales/es/hola/.locale-peer-id`

* `locales/ar/مرحبًا/.locale-peer-id`

If you want to create a translation of a directory and its contents, you must use the same locale peer id and put in a file named `.locale-peer-id`, because this is what's necessary for the project team to track translations across languages.
