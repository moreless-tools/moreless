# Sample files

These files contain fictional project data. Download a file, open the matching MORELESS editor and follow the steps below.

| File | Contents | Expected result |
| --- | --- | --- |
| [project-brief.pdf](project-brief.pdf) | A three-page brief, review checklist and approval form. | The PDF editor opens three pages. The last page has reviewer, date and reference fields, plus an approval checkbox. |
| [project-data.json](project-data.json) | Three document records and two milestones, written as compact JSON. | Formatting produces readable JSON. The review query below returns two document names. |
| [project-data.csv](project-data.csv) | The same three document records with a header row. | CSV to JSON produces an array of three records. |
| [project-data.xml](project-data.xml) | The three document records as XML. | Use the XML Field Extractor to inspect the document fields. |
| [text-before.txt](text-before.txt) and [text-after.txt](text-after.txt) | Two versions of a short project note. | Text Diff shows a review date changing from 5 November to 6 November and a new instruction to confirm the links. |

## Query the JSON

Open [JSON Formatter](https://moreless.tools/en/tools/json-formatter/), import `project-data.json` and select **JSONPath**.

This query selects the names of documents waiting for review:

```text
$.documents[?(@.status == "review")].name
```

Expected output:

```json
[
  "Project brief",
  "Release notes"
]
```

The query was checked in the public MORELESS web product on 1 November 2026.

[PDF walkthrough](../guides/pdf-workflow.md) · [JSON walkthrough](../guides/json-workflow.md) · [Open MORELESS](https://moreless.tools/en/)
