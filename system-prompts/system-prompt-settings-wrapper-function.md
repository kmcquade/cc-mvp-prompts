# System Prompt: settings-wrapper-function

- Source: inline

## Summary

Function template names wrapper via EXPR_1 and references user, project, local settings.

## Placeholder Hints (source-backed)

| Expression | Hint | Reference |
| --- | --- | --- |
| `EXPR_1` | None | None |

# Raw Prompt Text
function ${EXPR_1}(${URL}){
  ${URL}
  ${URL}
  userSettings
  projectSettings
  localSettings
}
