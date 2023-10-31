# CodeVA Standards Index

This repository contains data about all the standards CodeVA uses for alignment in its curricular products.

## Schema

Standards are expressed in `.yaml` format. Each `.yaml` file contains all the standards associated with a given grade level and subject area. The file should be located in a folder corresponding to the grade level.

Each standard should be written in the correct format. See below for the K.1 and K.2 computer science standards expressed in the correct format:

```
-   id: K.CS.AP.1
    title: K.1
    text: The student will construct sets of step-by-step instructions (algorithms) either independently or collaboratively including sequencing that emphasize the beginning, middle, and end.
    subs: []

-   id: K.CS.AP.2
    title: K.2
    text: The student will construct programs to accomplish tasks as a means of creative expression using a block based programming language or unplugged activities, either independently or collaboratively, including sequencing, emphasizing the beginning, middle, and end.
    subs: []
```

Pay close attention to the dash before `id`--this symbol separates standards from one another. Also pay close attention to indentation--YAML is a whitespace-sensitive format.

The four fields are required--all standards must define an `id` (in the correct format), a `title`, `text`, and `subs`. The chart below explains the information each field should contain:

| Field | Description | Example |
| ----- | ----------- | ------- |
| `id`  | The unique identifier for the standard. The format is `[grade].[subject].[strand].[number]`. See `id_key.yaml` for permitted subject and standard abbreviations and their definitions. | `- id: 3.MT.NS.1` |
| `title` | The title for the standard that will be displayed on the website. This title should match the name of the standard in the official VDOE document. | `title: K.1` |
| `text` | The text of the standard as written in the official VDOE document | `text: The student will...` |
| `subs` | A list of sub-standards as defined in the official VDOE document. The list must be enclosed in `[` and `]`, and each sub-standard should be enclosed in `"` and `"` and followed by a comma. | See `kindergarten/science.yaml` |


## Contributing

To contribute to the standards library, follow the steps below:

1. Create a new branch, and give it a descriptive name based on what work you will accomplish on that branch (e.g., `grade-2-CS` for working on compiling the 2nd grade computer science standards).
2. Add `.yaml` files to the appropriate folder in your branch.
3. When finished, make a pull request to trigger review and to prompt the project manager to merge your work in to the main branch.