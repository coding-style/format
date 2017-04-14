# Universal representation of a coding style

This document defines a universal representation of a coding style in JSON format.

```json
{
  "csn": integer,
  "version": integer,
  "name": {
    <language iso code>: string
  },
  "rationale": {
    <language iso code>: string
  },
  "languages": [string],
  "sources": [
    {
      "name": string,
      "url": string
    }
  ],
  "tags": [string],
  "related": [integer],
  "conflicts": [integer]
}
```

## Fields

### csn

A coding style number (CSN) is a non-negative integer which uniquely refers to a coding style.

### version

The version of a coding style.
Defaults to 1 if obmitted.
A specific version of a CSN is refered to by appending a `@` and the version.
For example `1@2` would refer to version 2 of CSN 1.

### name

A short description of the coding style, mapped by language code.

### rationale

A description of the rationale of the coding style, mapped by language code

### languages

An array of programming languages this coding style is restricted to.
If this field is omitted or empty, the coding style can be applied to all languages.

### sources

An array of sources or origins of this coding style.
Each source consists of a name of the source and, if available, an URL.
If no URL is available, this field is an empty string.

### tags

An array of tags.
Tags SHOULD be American English, lowercase keywords.

### related

An array of CSNs which are related to this coding style.

### conflicts

An array of CSNs which conflict to this coding style.

## Status

Work in progress.
Comments are welcome!
