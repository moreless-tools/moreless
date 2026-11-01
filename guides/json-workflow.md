# Format and query a JSON file

Use [project-data.json](../examples/project-data.json) to try JSON formatting and JSONPath in MORELESS. The file contains three document records and two project milestones.

1. Download the sample and open [JSON Formatter](https://moreless.tools/en/tools/json-formatter/).
2. Choose **Select file** or **Upload JSON file**, then select the sample. You can also paste its contents into **JSON Input**.
3. Select **Format**. With auto-format enabled, the formatted output updates as the input changes. Set the output indentation to two spaces, four spaces or tabs.
4. Select **JSONPath** and enter `$.documents[?(@.status == "review")].name`.
5. Choose **Execute**. The result should contain `Project brief` and `Release notes`.
6. Copy the result or download it as a file.

To inspect the full structure, switch to **Tree view**. **TypeScript** can generate starter interfaces from the example, and **Validate** can check an optional JSON Schema.

Formatting parses and writes the data again. Keep identifiers with more digits than JavaScript can represent exactly as strings. Review repaired JSON and inferred types before using them in an application.

[Full JSON guide](https://moreless.tools/en/docs/tools/json-formatter/) · [Sample files](../examples/)
