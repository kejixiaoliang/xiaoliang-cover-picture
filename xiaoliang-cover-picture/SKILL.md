---
name: xiaoliang-cover-picture
description: Use when the user asks for a WeChat official account cover, Xiaohongshu cover, article cover, title image, creator thumbnail, or cover image for the 科技小亮 personal IP based on an article title, summary, draft, Markdown, or topic.
---

# Xiaoliang Cover Picture

Create finished raster cover images inside Codex, not just prompts. Default to the built-in `image_gen` tool; do not require `OPENAI_API_KEY` unless the user explicitly requests CLI/API fallback.

Core taste: clean, readable, creator-led covers with a strong visual hook. Both WeChat and Xiaohongshu covers should avoid safe desk-review sameness; favor one bold metaphor, recognizable Xiaoliang identity, and thumbnail impact. WeChat is wider and more composed, but it still needs tension, depth, and a clear creative idea.

## Default Assets

- Default IP reference: `assets/ip-reference/xiaoliang-ip-reference.png`
- Optional positive example: `examples/weread-skill-xiaohongshu-impact-clean.png`
- These assets are local private working files. They are intentionally not part of the public GitHub repository.
- If `assets/ip-reference/xiaoliang-ip-reference.png` does not exist, tell the user to place their IP reference image there before generating identity-sensitive covers.
- If the user provides a different local reference path, use that path for the current task and mention that `assets/ip-reference/xiaoliang-ip-reference.png` remains the default reusable location.
- If the optional example image does not exist, continue without it and rely on `references/cover-style.md`, `references/prompt-patterns.md`, and `references/style-matrix.md`.
- Treat the reference image as strict identity guidance for round face shape, short slightly fluffy black hair, silver-framed glasses, young tech creator temperament, natural skin texture, and clean black clothing style.
- Before using a local reference image with built-in generation, inspect it with `view_image` so it is visible in the conversation context.

If the user provides another reference image in the conversation, use that as the primary identity reference and keep the bundled asset as fallback.

## Core Workflow

1. Read the user's article title, topic, summary, Markdown, or draft.
2. Decide the article type: AI tutorial, product review, tool experience, opinion analysis, trend explainer, failure review, or creator announcement.
3. Create a short cover concept:
   - final big title text, split into 2-4 Chinese lines;
   - one highlighted keyword or phrase;
   - Xiaoliang's expression, body posture, and hand action;
   - one realistic or surreal-realistic scene selected for the article, not reused by habit;
   - one core visual subject only;
   - one bold visual metaphor that turns the article's insight into an image.
4. Generate both required formats unless the user asks for only one:
   - WeChat official account cover: aspect ratio 2.35:1, wide horizontal composition.
   - Xiaohongshu cover: aspect ratio 3:4, vertical composition.
5. Use built-in `image_gen` once per format. Each format needs its own prompt, because composition must change with aspect ratio.
6. Inspect the generated image(s). Check identity, title readability, clean composition, visual hook, and avoid-list compliance.
7. If a result is cluttered, text-heavy, generic, too ad-like, too plain, too stable, or the person looks unlike the reference, retry once with a targeted correction.
8. For project-bound outputs, move or copy final images from Codex's generated image location into `outputs/covers/` with descriptive filenames, and report the saved paths.

## Prompt Requirements

Read `references/cover-style.md` before writing image prompts. Read `references/prompt-patterns.md` when choosing a scene/action/title pattern. Read `references/style-matrix.md` when selecting article type, platform layout, pose variation, and title pattern. Use `references/quality-gate.md` before accepting or reporting final covers.

Every prompt must include:

```text
Use case: ads-marketing
Asset type: Chinese creator article cover
Reference image: use the bundled Xiaoliang IP reference as strict identity guidance
Aspect ratio: <2.35:1 or 3:4>
Main subject: "科技小亮" as a slightly beautified but still recognizable young Chinese tech creator
Text (verbatim): "<final title text with line breaks>"
Composition: big title + Xiaoliang + one core visual subject + minimal environment
Style: clean realistic editorial cover; high-impact creative realistic or surreal-realistic when the topic has discovery, transformation, memory, product insight, or "AI saw through X" energy
Constraints: preserve round face shape, short slightly fluffy black hair, silver glasses, black clothing, young grounded tech creator temperament
Avoid: floating UI cards, code boxes, icon collage, dense background, small text, cheap ad look, generic business portrait, influencer face
```

## Identity And Beauty Rules

- Beautify subtly: cleaner skin, brighter eyes, tidy hair, better posture, softer professional lighting.
- Preserve identity: round face shape, silver round glasses, short black hair, young age range, natural expression, and grounded tech-creator temperament must remain recognizable.
- Do not turn the person into a fashion model, anime character, corporate stock-photo actor, older businessman, or generic influencer.
- Use natural expressions: focused, curious, confident, mildly excited, surprised by a finding, or analytical.
- Vary poses by article topic. Avoid repeating stiff thumbs-up or pointing poses.
- If the user says the person is unlike Xiaoliang, strengthen identity wording before retrying: "closer to the reference photo than a generic handsome influencer; keep rounder face, natural skin texture, short slightly fluffy hair, silver glasses, black zip jacket."

## Pose And Scene Variety

Never reuse the same pose formula by default. Before prompting, choose one option from each group and make it specific:

- Body posture: seated close-up, standing half-body, side-profile at a workbench, top-down hands-only plus partial face, over-shoulder view, low-angle hero view, crouched near hardware, leaning back in realization, turning from desk to camera.
- Hand action: holding the core object, plugging in a cable, soldering, measuring with a probe, opening a lid/book/box, pulling a cable, placing a chip, comparing two objects, drawing a connection line, lifting a finished build, shielding eyes from light, pressing one physical button.
- Expression: discovery, "wait this works?", controlled surprise, proud after finishing, focused debugging, skeptical testing, amused by a clever hack, calm explainer.
- Camera angle: low-angle foreground object, top-down desk, three-quarter side view, close face plus object, wide maker-room view, macro hardware foreground with Xiaoliang behind it, mirror/reflection shot, doorway/studio reveal.

Scene library:

- Hardware/maker: soldering mat, oscilloscope-style bench, USB cables and ESP32, pegboard tools, dark desk with object light, daylight desk with parts tray, hands assembling a board.
- AI/tool: clean studio desk, glowing paper notebook, physical workflow map, archive box, microscope/lens over a tool, spotlight on one device.
- Reading/knowledge: open book, bookshelf shadow, desk lamp, annotation cards, paper stack, library-like corner.
- Product/review: tabletop product stage, teardown tray, comparison ruler, packaging opened, small lightbox.
- Opinion/trend: clean wall, standing presenter pose, large symbolic object, window light, simple studio corner.

For repeated outputs in one session, intentionally vary at least two of these: body posture, hand action, camera angle, scene family, and lighting source.

## Composition Rules

- The cover must feel clean at first glance.
- Use one main visual idea only.
- Prefer realistic environments: desk, laptop, phone, product on table, studio corner, home office, simple review setup.
- Avoid floating windows, UI cards, code snippets, dashboards, chart panels, and icon clusters unless the user explicitly asks for them.
- Use large Chinese title text as a primary visual object. Keep it short, bold, and readable.
- Use white title text with one accent color: bright blue, cyan, or orange-red.
- Keep supporting text out of the image unless the user explicitly requests it.
- Do not default to "creator holding a phone" for tool articles. Use it only when the phone itself is the reviewed product or the user asks for it.
- When an article has a strong transformation, discovery, memory, or "AI saw through X" angle, use a physical metaphor: open book, portal, microscope, spotlight, exploded object, lab table, mirror, archive box, or illuminated map.

## Impact Defaults

Start impact-first for both formats. A clean cover can still be bold.

Shared defaults:

- Use one metaphor or physical object that explains the article at a glance.
- Make Xiaoliang interact with the object using a specific action from the pose library, not generic open hands every time.
- Use stronger contrast than a plain desk photo while keeping the scene readable.
- Avoid passive sitting, stiff pointing, and "person holding phone" unless the phone itself is the point.

For WeChat:

- Use the wide canvas for left-right tension: huge title on one side, Xiaoliang and the core object on the other side, or a diagonal object crossing the frame.
- Keep title readable after official-account cropping; use 2-3 large lines, not many small words.
- Put the core object in the foreground or center-right/center-left so the scene has depth, not a flat portrait.
- Prefer a decisive story moment: opening, revealing, lighting up, dismantling, plugging in, soldering, measuring, comparing, lifting the finished result, or discovering.
- Do not settle for a calm office-wall portrait unless the article is purely opinion commentary.

For Xiaohongshu, start impact-first:

- Use close or medium-close framing so the face is recognizable.
- Put the title in the top 40-50% with oversized bold Chinese text.
- Add one dramatic diagonal or foreground object for depth.
- Use stronger contrast than WeChat covers, while keeping the scene readable.
- Let Xiaoliang interact with the core object using a varied, article-specific action. Avoid making every cover "leaning forward with both hands open."

Successful pattern from the WeRead Skill cover:

- See `examples/weread-skill-xiaohongshu-impact-clean.png` as the current taste reference.
- Topic: AI reads a personal reading history.
- Title: `微信读书Skill\n把我的书架\n看透了`
- Visual metaphor: one huge open book glowing cyan-blue as if it contains the user's reading data.
- Action: Xiaoliang leans toward the book with both hands open, surprised and focused.
- WeChat adaptation: use the same metaphor in a wide layout, with the huge title on the left, Xiaoliang and the glowing open book on the right/center, strong diagonal light, and no phone.
- Why it works: strong title, one metaphor, no phone, recognizable face, high contrast, clear thumbnail impact.

## Format Guidance

WeChat 2.35:1:
- Use a wide, high-impact layout, not a plain stable desk portrait.
- Place the large title on one side or across the left/center; keep it huge and readable.
- Place Xiaoliang and the core visual subject on the opposite side or center-right/center-left, with a clear action.
- Use foreground depth, diagonal light, or a single bold object to create tension.
- Keep the background sparse; the impact should come from the title, Xiaoliang, and one metaphor object.

Xiaohongshu 3:4:
- Use a tighter, more forceful portrait composition than WeChat.
- Let the title occupy the upper 40-50%; make the strongest phrase huge.
- Place Xiaoliang in the middle/lower area with a clear, energetic action.
- Make the core visual subject large in the foreground.
- Default to creative realistic or surreal-realistic scenes, not plain desk screenshots.

## Quality Gate

Use `references/quality-gate.md` as the authoritative acceptance checklist.

Reject and retry when any of these appear:

- cluttered collage or too many objects;
- floating cards, UI panels, code frames, or icon piles;
- title text too small, too dense, or unreadable;
- person looks unlike the reference image;
- Xiaoliang looks like a generic influencer, corporate stock model, or older businessman;
- the pose is just holding a phone without a strong reason;
- the pose repeats the last successful cover too closely;
- Xiaoliang is only leaning forward with both hands open when another action would better fit the article;
- the scene repeats the same dark desk / glowing object setup without a topic reason;
- the cover feels too stable, plain, ordinary, or like a generic desk review;
- excessive glow, cyberpunk effects, movie-poster drama, or cheap sales-ad styling;
- stiff body language or repeated stock gesture;
- background competes with the title or person.

When retrying, change only the failing point. Keep the article concept and title stable.
