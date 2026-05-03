# Codex Pets: 一二 and 布布

Custom Codex desktop pet spritesheets for two soft chibi companions:

- **一二**: a shy white rounded pet with dark brown ears, pink cheeks, tiny limbs, and no eyebrows.
- **布布**: a sleepy milk-tea-brown bear with yellow cheek patches, a relaxed face, and playful desk-companion actions.

## Contents

```text
pets/
  yier/
    pet.json
    spritesheet.webp
    preview.png
  bubu/
    pet.json
    spritesheet.webp
    preview.png
prompts/
references/
previews/
docs/
```

`duo` is planned but not included yet because no combined duo spritesheet has been generated.

## Install

Copy a pet folder into your Codex pets directory:

```powershell
Copy-Item -Recurse .\pets\yier "$env:USERPROFILE\.codex\pets\yier"
Copy-Item -Recurse .\pets\bubu "$env:USERPROFILE\.codex\pets\bubu"
```

Then restart Codex.

## QA

Both spritesheets were validated as `1536x1872` transparent-capable WebP atlases with `192x208` cells.

- 一二 contact sheet source: `runs/yi-er/qa/contact-sheet.png`
- 布布 contact sheet source: `runs/bu-bu/qa/contact-sheet.png`

MP4 preview videos are not included because `ffmpeg` was unavailable in the generation environment; GIF previews are included instead.
