# Tool Description: read-local-file-lines

- Name: View

## Summary

Read a local file by absolute path with optional line offset and limits.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | 2000 | None |
| `EXPR_2` | 2000 | None |
| `EXPR_3` | ReadNotebook | None |

# Raw Prompt Text
Reads a file from the local filesystem. The file_path parameter must be an absolute path, not a relative path. By default, it reads up to ${EXPR_1: 2000} lines starting from the beginning of the file. You can optionally specify a line offset and limit (especially handy for long files), but it's recommended to read the whole file by not providing these parameters. Any lines longer than ${EXPR_2: 2000} characters will be truncated. For image files, the tool will display the image for you. For Jupyter notebooks (.ipynb files), use the ${EXPR_3: 'ReadNotebook'} instead.
