# Surge RULE-SET collection

These files are converted from the `yuumimi/rules` release branch's Surge DOMAIN-SET files into Surge-compatible RULE-SET lists.

| File | Original source | Rules |
| --- | --- | ---: |
| [OpenAI.list](./OpenAI.list) | [openai.txt](https://raw.githubusercontent.com/yuumimi/rules/release/surge/openai.txt) | 24 |
| [Gemini.list](./Gemini.list) | [google-gemini.txt](https://raw.githubusercontent.com/yuumimi/rules/release/surge/google-gemini.txt) | 49 |
| [Google.list](./Google.list) | [google.txt](https://raw.githubusercontent.com/yuumimi/rules/release/surge/google.txt) | 847 |
| [YouTube.list](./YouTube.list) | [youtube.txt](https://raw.githubusercontent.com/yuumimi/rules/release/surge/youtube.txt) | 177 |
| [NTPService.list](./NTPService.list) | [NTPService.lsr](https://rule.kelee.one/Loon/NTPService.lsr) (verified via GitHub mirrors) | 82 |

Snapshot: 2026-11-22. NTPService rules were already in Surge-compatible DOMAIN-SUFFIX format, so only whitespace and file extension were normalized; source verification used two matching GitHub mirrors because the original host was unavailable. Conversion was structural only: `.example.com` becomes `DOMAIN-SUFFIX,example.com` and `example.com` becomes `DOMAIN,example.com`. Original domain coverage was retained, including potentially historical services. This collection is not automatically updated yet.

## Surge example

Use the Raw URLs of this repository in [Rule]. Select a pre-existing policy group. Put more specific service rules before generic Google and Proxy rules:

```ini
RULE-SET,https://raw.githubusercontent.com/Jay-make8/my-icons/main/rules/OpenAI.list,"Open ai"
RULE-SET,https://raw.githubusercontent.com/Jay-make8/my-icons/main/rules/Gemini.list,Gemini
RULE-SET,https://raw.githubusercontent.com/Jay-make8/my-icons/main/rules/YouTube.list,YouTube
RULE-SET,https://raw.githubusercontent.com/Jay-make8/my-icons/main/rules/Google.list,Google
RULE-SET,https://raw.githubusercontent.com/Jay-make8/my-icons/main/rules/NTPService.list,"ISP Exit"
```

Note: This repository contains both icon assets and rules. Changes to this folder do not modify the `icons/` or `icons.json` files.
