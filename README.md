# Locale help

Locale explains how people can translate this project into worldwide languages.

## Locale subdirectory names

Each locale subdirectory must be named using a standard locale code.

Examples:

```txt
- `locales/en-us/` is for English - United States regional dialect

- `locales/en-gb/` is for English - Great Britain regional dialect

- `locales/zh-cn/` is for Chinese - China mainland dialect with simplified Mandarin

- `locales/zh-tw/` is for Chinese - Taiwan island dialect with traditional Mandarin
```

## Where to find locale codes?

List of BCP-47 language tags:

- [https://developer.mozilla.org/en-US/docs/Glossary/BCP_47_language_tag](https://developer.mozilla.org/en-US/docs/Glossary/BCP_47_language_tag)

List of ISO 639-1 codes:

- [https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

## Content subdirectory names

Content subdirectory names must be translated into their corresponding languages.

Examples:

- `locales/en-us/hello/`

- `locales/zh-cn/你好/`

## Slug format

Content subdirectory names must use a slug format, which means a format that is user-friendly for reading, copying, pasting, typing, browsing, and searching:

Example:

- `locales/en-us/hello-world`

- `locales/zh-cn/你好-世界`

You have options for the slug format:

- Our projects use a slug format for English that uses alphanumeric lowercase characters, with words separated by a hyphen-minus character, and no other characters.

- Your projects may use whatever you prefer; for example Wikipedia uses alphanumeric mixed-case characters, with words separated by an underscore character, and other characters such as parentheses.

## locale peer id

This project keeps track of corresponding content across multiple locales by using the computer science technique named "locale peer id".

A locale peer id is a secure randomly-generated 32-character lowercase hexadecimal string.

For example, `b82232cff8e5bb785fbc855b65a83653`.

## .locale-peer-id file

Each directory contains a file named `.locale-peer-id` that contains the locale peer id then a newline.

When anyone translates any project directory from one language into another, then the locale peer id is identical.

For example each directory below contains a file named `.locale-peer-id` and each file contains the identical locale peer id:

```txt
locales/
  en-us/
    hello-world/
      .locale-peer-id - b82232cff8e5bb785fbc855b65a83653 then newline
      index.html - translation with English United States dialect
  zh-cn/
    你好-世界/
      .locale-peer-id - contains b82232cff8e5bb785fbc855b65a83653 then newline
      index.html - translation with Chinese China mainland dialect
```

## To create a translation

To create a translation of a directory and its contents, you must use the same
locale peer id and file name `.locale-peer-id`, because this consistency is what
enables the project team to track directory translations among languages.

### For programmers

If you are a programmer, then see these tools which may help you:

- [bin/locale-peer-id](bin/locale-peer-id): generate a locale peer id

- [bin/grep-locale-peer-id](bin/grep-locale-peer-id): find files that contain a given locale peer id

- [bin/markdown-read-to-headline](bin/markdown-read-to-headline): markdown tool to read a file or stdin, then print the first headline

- [bin/slug-case](bin/slug-case): input a line of text; output the text converted to slug case

## Extras

### Locale without region

A locale can have a region, such as:

- `locales/es/` is for Spanish - officially doesn't have a region

- `locales/hi/` is for Hindi - officially doesn't have a region

### Locale with unspecified region

A locale can have an unspecified region such as:

- `locales/en/` is for English (unspecified region) - better to be specific `en-us` or `en-gb`.

- `locales/zh/` is for Chinese (unspecified region) - better to be specific `zh-cn` or `zh-tw`.

### Oxford locale

For worldwide standards, international organizations, cross-border communications, and the like, we prefer
we currently prefer using the Oxford locale:

- `locales/en-gb-oxendict/` is for English - Great Britain - Oxford English dictionary

For example, the World Health Organization (WHO) and United Nations (UN) use this locale.

### Locale en-001 English (World)

en-001 replaces en-US as the generic fallback.

Historically, many applications used American English as the default global
fallback, which forced everyone to use MM/DD/YYYY dates and imperial
measurements. en-001 solves this.

Defined in CLDR as equivalent to “English (United States)” except:

Almost equivalent to “English (United States)”, except for some locale and
formatting differences including these:

- Date format DD/MM/YYYY instead of MM/DD/YYYY.
- First day of the week is Monday instead of Sunday.
- Currency symbol is US$ instead of $.
- Use metric measurements.

### Locale en-150 English (Europe)

en-150 replaces en-US as the Europe fallback.

Historically, millions of Europeans used American English as a professional
lingua franca but are deeply accustomed to European standards like the 24-hour
clock and comma-separated numbers.

Defined in CLDR as equivalent to “English (World)” except:

- For decimal separator, use comma instead of period.
- For time format, use 24-hour instead of 12-hour
- For currency symbol, use `¤` of `US$`.

### Our preferences

For our major worldwide projects, we consider these locales.

The United Nations languages:

- ar-001: Arabic (World)
- en-001: English (World)
- es-001: Spanish (World)
- fr-001: French (World)
- ru-001: Russian (World)
- zh-001: Chinese (World)

The locales where we receive funding:

- en-us English (United States)
- en-gb English (Great Britain)
- cy-gb Cymraeg (Great Britain)

The top 10 most-spoken languages in order:

- en-001: English: ~1.49 billion total speakers (372M native + 1.12B non-native)
- zh-001: Mandarin Chinese: ~1.18 billion total speakers (988M native + 194M non-native)
- hi-001: Hindi: ~611 million total speakers (347M native + 264M non-native)
- es-001: Spanish: ~561 million total speakers (487M native + 75M non-native)
- ar-001: Modern Standard Arabic: ~335 million total speakers (mostly second-language or formal use)
- fr-001: French: ~334 million total speakers (75M native + 258M non-native)
- bn-001: Bengali: ~274 million total speakers (234M native + 43M non-native)
- pt-001: Portuguese: ~269 million total speakers (252M native + 18M non-native)
- id-001: Indonesian: ~255 million total speakers (78M native + 177M non-native)
- ur-001: Urdu: ~246 million total speakers (78M native + 168M non-native)
