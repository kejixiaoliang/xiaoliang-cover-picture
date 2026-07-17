# Cover Quality Gate

Use this checklist before accepting a generated cover. Reject and retry when a critical item fails.

## 1. Setup Check

| Check | Pass Standard |
| --- | --- |
| IP reference exists | `assets/ip-reference/xiaoliang-ip-reference.png` exists, or the user provided another reference path. |
| Private assets stay local | Reference images, generated covers, article screenshots, and drafts are not prepared for public upload. |
| Output path is local | Final covers are saved under `outputs/covers/` or another user-approved local path. |

If the default IP reference is missing, stop before image generation and ask the user to place a clear reference image at:

```text
assets/ip-reference/xiaoliang-ip-reference.png
```

## 2. Prompt Check

| Check | Pass Standard |
| --- | --- |
| Article type is named | AI tutorial, product review, tool experience, opinion analysis, trend explainer, failure review, hardware maker, or creator announcement. |
| Title is short | 2-4 Chinese lines, no long sentence, no small subtitle unless the user explicitly asks. |
| One core subject | The prompt names exactly one main object, product, metaphor, or scene anchor. |
| One clear action | Xiaoliang is opening, testing, connecting, comparing, revealing, measuring, explaining, or reacting to the core subject. |
| Platform is explicit | WeChat prompt says `2.35:1`; Xiaohongshu prompt says `3:4`. |
| Avoid list is present | Prompt explicitly bans floating UI cards, code boxes, icon collage, dense background, tiny text, generic influencer face, and unnecessary phone-holding. |

## 3. Image Review

| Area | Reject When |
| --- | --- |
| Title | Text is too small, too dense, misspelled, cluttered, or unreadable as a thumbnail. |
| Identity | The person looks like a generic influencer, older businessman, fashion model, anime character, or unrelated stock portrait. |
| Composition | The image has no focal point, too many props, too many UI elements, or a flat left-text-right-person layout. |
| Scene | The scene repeats dark desk + blue glow + open hands without a topic reason. |
| Platform fit | The WeChat cover lacks wide-frame tension, or the Xiaohongshu cover is not close/mobile-first enough. |
| Privacy | The image includes unintended private screenshots, personal information, file paths, or user data. |

## 4. Retry Rules

Retry only the failing part. Keep the article concept and title stable unless the title itself failed.

| Failure | Retry Instruction |
| --- | --- |
| Person looks unlike the reference | Strengthen identity wording: closer to the reference photo, rounder face, natural skin texture, short slightly fluffy black hair, silver glasses, grounded tech creator temperament. |
| Title is unreadable | Reduce title length, increase title size, remove subtitle, and keep only one highlighted phrase. |
| Image is cluttered | Remove extra screens, icons, panels, props, and secondary captions. Keep one object. |
| Composition feels passive | Add one physical action: opening, plugging in, measuring, dismantling, pressing, comparing, lifting, or revealing. |
| Platform mismatch | Recompose instead of cropping. WeChat needs wide tension; Xiaohongshu needs closer title/person/object framing. |

## 5. Final Delivery

Report only the useful final paths and any caveats:

```text
WeChat cover: outputs/covers/<name>-wechat-cover.png
Xiaohongshu cover: outputs/covers/<name>-xiaohongshu-cover.png
```

Do not report private reference image details unless the user asks.
