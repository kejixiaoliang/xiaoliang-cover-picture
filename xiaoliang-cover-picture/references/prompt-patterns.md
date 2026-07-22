# Cover Prompt Patterns

Use these patterns as starting points. Adapt the title, action, and scene to the article.

## AI Tutorial

Concept: Xiaoliang teaching a practical AI workflow through one visible object.

Prompt notes:
- Expression: focused, confident, slightly excited.
- Action options: standing half-body explaining beside a physical workflow map; placing one card into a sequence; pointing at a real object on the desk; turning from the object toward camera.
- Visual subject: one laptop, one book, one device, or one physical workflow object.
- Scene options: clean home-office desk, studio table, wall-mounted paper flow, daylight workbench, compact teaching corner.
- Highlight color: blue or cyan.

## Product Review

Concept: Xiaoliang testing one product in a realistic review setup.

Prompt notes:
- Expression: curious, analytical, mildly surprised.
- Action options: holding the product near camera; opening packaging; measuring with a ruler/caliper; comparing two physical states; looking through a magnifier; lifting the finished result.
- Visual subject: the product only.
- Scene options: simple tabletop review scene, lightbox corner, teardown tray, parts mat, product stage with one directional light.
- Highlight color: cyan or orange-red depending on verdict.

## Tool Experience

Concept: Xiaoliang discovers what a tool really does through a strong visual metaphor, not a UI dashboard.

Prompt notes:
- Expression: engaged, discovery-driven, surprised but controlled.
- Action options: opening, uncovering, lighting up, inspecting, plugging in, pressing a physical button, pulling a cable, placing a key object, turning back in realization.
- Visual subject: one physical metaphor object, such as an open book, archive box, toolbox, microscope, spotlight, mirror, lab table, or illuminated map.
- Scene options: realistic or surreal-realistic desk, archive table, maker bench, studio floor, wall of notes, dark room lit by the object, daylight desk with object shadow.
- Highlight color: cyan or blue.
- Avoid: default hand-held phone, multiple app screenshots, UI cards, code windows.

Example: for a WeRead Skill article, use one huge open book glowing cyan-blue, Xiaoliang leaning forward with both hands open, and the title `微信读书Skill\n把我的书架\n看透了`.

## Opinion Analysis

Concept: Xiaoliang as a calm tech commentator with one symbolic object.

Prompt notes:
- Expression: confident, thoughtful.
- Action options: standing half-body with one symbolic object; side-profile thinking; seated but turned toward camera; holding a paper note; resting one hand on the object.
- Visual subject: one symbol or object, not a collage.
- Scene options: clean studio, office wall, window light, simple shelf, neutral wall with one physical prop.
- Highlight color: white plus blue.

## Failure Review Or Warning

Concept: Xiaoliang points out one concrete issue without making the cover messy.

Prompt notes:
- Expression: surprised but controlled, analytical.
- Action options: uncovering, circling with a marker, isolating the problem object, pulling a loose cable, holding a broken part, comparing wrong vs right object.
- Visual subject: one device, product, warning object, or broken workflow metaphor.
- Scene options: simple desk with hard side light, teardown tray, warning-color tabletop, dark background with one lit problem object.
- Highlight color: orange-red.

## Hardware Maker

Concept: Xiaoliang turns code into a physical device.

Prompt notes:
- Expression: focused debugging, surprised when it lights up, proud after finishing.
- Action options: soldering on a mat; plugging in USB; holding the finished board toward camera; pressing a tiny button; measuring with probes; placing an ESP32 beside the output device; shielding eyes from a bright LED.
- Visual subject: one hardware object only, such as LED matrix, ESP32 board, sensor, motor, status light, or wiring harness.
- Scene options: maker desk, soldering mat, parts tray, tool pegboard, dark desk lit by LEDs, daylight bench with components, close macro hardware foreground.
- Highlight color: cyan, green, or yellow depending on status.
- Avoid: generic laptop coding scene, too many scattered components, fake circuit-board collage, random neon tech background.

## High-Impact Xiaohongshu

Concept: turn the article's main insight into one bold scene.

Prompt notes:
- Title: top 40-50%, huge Chinese type.
- Person: close or medium-close, face recognizable, black clothing, silver glasses.
- Action: choose one specific action from the article type; avoid repeating "hands open, leaning in" unless that is clearly the best action.
- Object: one foreground object with depth.
- Lighting: strong but clean contrast from the object or side light.
- Style: realistic editorial with creative metaphor; not anime, not movie poster, not cyberpunk.

Good structure:

```text
Scene/backdrop: dark clean studio desk with one <core object> in foreground, <accent-color> light bursting from it.
Core visual subject: one <core object> only.
Composition/framing: vertical 3:4, huge title in the top half, Xiaoliang in the lower half close enough to recognize, leaning forward with hands interacting with the object.
Lighting/mood: dramatic but clean light from the object illuminating face and glasses.
Avoid: phone, generic influencer face, flat desk photo, extra captions, floating UI cards.
```

## High-Impact WeChat

Concept: use the wide canvas to create a strong left-right story moment.

Prompt notes:
- Title: 2-3 huge Chinese lines on the left or center-left.
- Person: recognizable Xiaoliang on the opposite side, close enough to read the face.
- Action: choose one specific action from the article type: plugging in, soldering, lifting, opening, measuring, dismantling, revealing, comparing, turning back, or reacting.
- Object: one large object in the foreground or center, never a collage.
- Lighting: directional light, diagonal glow, or object-led illumination for depth.
- Style: clean editorial with a bold metaphor; not a calm office portrait.

Good structure:

```text
Scene/backdrop: wide clean studio desk with one <core object> in foreground, <accent-color> light or action creating diagonal depth.
Core visual subject: one <core object> only.
Composition/framing: 2.35:1 wide cover, huge title on the left/center-left, Xiaoliang on the right/center-right interacting with the object, strong foreground depth, sparse background.
Lighting/mood: punchy but clean editorial light, clear and trustworthy, more dynamic than a stable desk photo.
Avoid: flat left-text-right-portrait layout, holding a phone without reason, generic business portrait, floating UI cards.
```

## Variation Checklist

Before writing each prompt, state these choices inside the prompt:

- Pose: <one concrete body posture>
- Hand action: <one concrete hand action>
- Camera angle: <low / top-down / side / over-shoulder / close-up / wide>
- Scene family: <maker / reading / product / studio / archive / teardown / teaching>
- Lighting source: <object glow / window / desk lamp / side light / daylight>

If the previous generated cover used "dark desk + glowing object + leaning forward with hands open", pick a different hand action or camera angle for the next cover.

## Title Rewrite Patterns

Transform article titles into cover titles:

- `<工具名>\n真能提效吗？`
- `我试了<时间>\n发现一个坑`
- `普通人也能用\nAI 做<结果>`
- `<产品名>测评\n值不值得买？`
- `别急着用\n先看这个`
- `<关键词>\n可能变天了`
- `这次升级\n有点不一样`
- `<工具名>\n把<对象>\n看透了`
- `AI 打开了\n我的<数据/书架/笔记>`

Keep the final image title short. If the article title is long, choose the strongest promise, doubt, result, discovery, or warning.

## WeChat Prompt Skeleton

```text
Use case: ads-marketing
Asset type: WeChat official account article cover, 2.35:1 wide horizontal image
Reference image: use Xiaoliang's IP reference for identity consistency
Primary request: high-impact clean Chinese tech creator cover for an article about <topic>
Main subject: Xiaoliang, slightly beautified but recognizable, round face, short black hair, silver-framed glasses, black clean tech-creator outfit
Scene/backdrop: <one realistic or surreal-realistic wide scene with a bold metaphor>
Core visual subject: <one foreground object only>
Composition/framing: wide 2.35:1 high-impact composition, huge Chinese title on <left/center-left>, Xiaoliang on <right/center-right> interacting with the core object, strong foreground depth or diagonal light, sparse background, no floating panels
Lighting/mood: punchy but clean editorial lighting, clear and trustworthy, discovery-driven
Color palette: clean black, white, gray, one accent color <blue/cyan/orange-red>
Text (verbatim): "<line 1>\n<line 2>\n<line 3 optional>"
Typography: very large bold Chinese title, white text with one highlighted keyword in accent color, readable thumbnail text
Constraints: preserve Xiaoliang's round face shape, short hair, silver glasses, age range, black clothing, professional AI/tech review temperament; subtly beautify skin and posture
Avoid: flat left-text-right-portrait layout, holding a phone unless requested, generic influencer face, generic business portrait, plain stable desk photo, floating UI cards, code boxes, icon collage, dense background, small text, excessive glow, cinematic poster look, cheap ad style, clutter
```

## Xiaohongshu Prompt Skeleton

```text
Use case: ads-marketing
Asset type: Xiaohongshu article cover, 3:4 vertical image
Reference image: use Xiaoliang's IP reference for strict identity consistency
Primary request: high-impact clean Chinese creator cover for an article about <topic>
Main subject: Xiaoliang, slightly beautified but recognizable, round face, short slightly fluffy black hair, silver-framed glasses, black clean tech-creator outfit
Scene/backdrop: <one realistic or surreal-realistic scene with a bold metaphor>
Core visual subject: <one foreground object only>
Composition/framing: vertical mobile-first composition, huge Chinese title in the top 40-50%, Xiaoliang in middle/lower area close enough to recognize, clear energetic action, strong depth, sparse background
Lighting/mood: punchy but clean editorial lighting, strong contrast, discovery-driven
Color palette: clean black, white, gray, one accent color <blue/cyan/orange-red>
Text (verbatim): "<line 1>\n<line 2>\n<line 3 optional>"
Typography: extra-large bold Chinese title, white text with one highlighted keyword in accent color, readable thumbnail text, no extra small text
Constraints: preserve Xiaoliang's round face shape, short hair, silver glasses, age range, black clothing, grounded tech creator temperament; subtly beautify only
Avoid: holding a phone unless requested, generic influencer face, older businessman, flat desk photo, floating UI cards, code boxes, icon collage, dense background, small text, excessive glow, cyberpunk city, cheap ad style, clutter
```
