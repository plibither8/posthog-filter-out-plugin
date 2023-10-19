# 🦔 PostHog Filter Out Plugin

> Injest only those events satisfying the given filter conditions

---

## ⚠️ Moved to [PostHog/posthog-filter-out-plugin](https://github.com/PostHog/posthog-filter-out-plugin)

Development and support for this plugin has been moved to [**PostHog/posthog-filter-out-plugin**](https://github.com/PostHog/posthog-filter-out-plugin). Create issues and PRs in PostHog's repository instead.

---

## Configuration

The plugin configuration requires a JSON file with the following structure:

**Example filters:**

Only keep events where all the following conditions are met:

- **Email** _does not contain_ **yourcompany.com**
- **Host** _is not_ **localhost:8000**
- **Browser version** _greater than_ **100**

```json
[
  {
    "property": "email",
    "type": "string",
    "operator": "not_contains",
    "value": "yourcompany.com"
  },
  {
    "property": "host",
    "type": "string",
    "operator": "is_not",
    "value": "localhost:8000"
  },
  {
    "property": "browser_version",
    "type": "number",
    "operator": "gt",
    "value": 100
  }
]
```

**Allowed types and their operators:**

| Type    | Operators                                            |
| ------- | ---------------------------------------------------- |
| number  | gt, gte, lt, lte, eq, neq                            |
| string  | is, is_not, contains, not_contains, regex, not_regex |
| boolean | is, is_not                                           |

## License

[MIT](LICENSE)
