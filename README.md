# 一二与布布 Codex Pets

这是一个基于“一二”和“布布”形象制作的 Codex 自定义桌宠项目。项目将两个软萌风格的角色转化为适用于 Codex 的桌面宠物，使其能够在 Codex 环境中以轻量、可爱、陪伴式的方式出现。

## 项目简介

本仓库目前包含两个已经生成并验证过的 Codex 宠物包：

- **一二**：白色圆润身体、深棕色圆耳朵、粉色腮红、小圆眼睛和 tiny `w` 嘴。新版一二没有眉毛，整体性格柔软、温柔、害羞、可爱。
- **布布**：奶茶棕色小熊，深棕色描边，黄色腮红，困困的小表情，整体气质慵懒、治愈、呆萌，适合作为轻松陪伴型桌宠。

两个角色都采用 Codex desktop pet 风格：简洁轮廓、有限配色、扁平化表现、pixel-art-adjacent 质感，并优先保证小尺寸下的可读性。

## 仓库结构

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
  duo/
    README.md
prompts/
references/
previews/
docs/
```

`duo` 是计划中的一二 + 布布组合宠物，目前还没有生成真实 spritesheet，所以没有放置可安装的 `pet.json` 或 `spritesheet.webp`。

## 安装

把对应宠物目录复制到本机 Codex pets 目录，然后重启 Codex。

```powershell
Copy-Item -Recurse .\pets\yier "$env:USERPROFILE\.codex\pets\yier"
Copy-Item -Recurse .\pets\bubu "$env:USERPROFILE\.codex\pets\bubu"
```

## 预览

- `previews/yier_preview.gif`
- `previews/bubu_preview.gif`

每个 `pets/<name>/preview.png` 是从 spritesheet 的 idle 第一帧导出的静态预览。

## QA

两个 spritesheet 都已通过 `hatch-pet` 的 deterministic QA：

- WebP atlas 尺寸：`1536x1872`
- cell 尺寸：`192x208`
- `review.json`：无 errors/warnings
- `validation.json`：无 errors/warnings

MP4 预览视频未包含，因为生成环境没有 `ffmpeg`；仓库中提供 GIF 预览作为替代。

## Notes

`references/` 中保存的是本次生成后的 canonical base reference，不是原始上传参考图。若要公开分发原始参考图，请先确认你拥有相应使用权。

## License

MIT License. See `LICENSE`.
