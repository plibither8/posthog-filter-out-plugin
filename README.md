# 🦔 PostHog Value Filter Plugin

> Filter out events where property values satisfy the given condition

## Configuration

The plugin configuration requires a JSON file with the following structure:

```json
{
  "filters": [
    {
      "key": "event_property",
      "type": "number",
      "operator": "gt",
      "value": 10
    },
    {
      "key": "event_property",
      "type": "string",
      "operator": "includes",
      "value": "foo"
    }
  ]
}
```

**Allowed types and their operators:**

| Type    | Operators                                            |
| ------- | ---------------------------------------------------- |
| number  | gt, gte, lt, lte, eq, neq                            |
| string  | is, is_not, contains, not_contains, regex, not_regex |
| boolean | is, is_not                                           |

## License

[MIT](LICENSE)
