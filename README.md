# Universal representation of a coding style

This document defines a universal representation of a coding style in JSON format.

```json
{
  csn: integer,
  version: integer,
  name: {
    <language iso code>: string
  },
  rationale: {
    <language iso code>: string
  },
  languages: [string],
  sources: [
    {
      name: string,
      url: string
    }
  ],
  tags: [string],
  related: [integer],
  conflicts: [integer]
}
```

## Status

Work in progress.
Comments are welcome!
