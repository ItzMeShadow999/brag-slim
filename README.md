# brag-slim

> Turn a project directory or a website URL into a 20-second launch video with music, motion, and share copy. One file, no bundled assets.

`brag-slim` is a single-file agent skill. Point it at a codebase or a live site and the model builds the whole video itself: story, visuals, soundtrack, render. It uses only tools already on the machine (ffmpeg, a headless browser, the project's own build tool).

## What you get

Written to `brag-output/`:

- `brag.mp4`: the launch video (about 20s, 30fps, poster baked in as frame 0)
- `brag.jpg`: poster frame
- `share-copy.txt`: a postable caption
- `brag-plan.md`: the storyboard
- `work/`: every intermediate file

## Usage

```
/brag-slim [input] [--tone <preset|freeform>] [--format landscape|vertical|square] [--duration <s>]
```

| Option | Default |
|---|---|
| `--tone` | inferred (`default`, `polished`, `yc-parody`, `chaotic`, `deadpan`, `cinematic`, `app-store`, or freeform) |
| `--format` | `landscape` (1920x1080); `vertical` 1080x1920; `square` 1080x1080 |
| `--duration` | about 20s |

Input is either a project directory (the current one if omitted) or an `http(s)://` URL / bare domain.

## Install

Copy `SKILL.md` into a skills folder as `brag-slim/SKILL.md`, for example `~/.claude/skills/brag-slim/SKILL.md`. Requires ffmpeg and a headless browser (the skill asks before fetching anything).

## Credit

This is the `brag-slim` skill from **[latent-spaces/brag](https://github.com/latent-spaces/brag)**. All credit goes to the latent-spaces team; this repo is just a copy of that one file. The upstream project is MIT licensed, see its [LICENSE](https://github.com/latent-spaces/brag/blob/main/LICENSE) for the full terms and copyright notice, which apply here too.

Upstream credits for the full `/brag` skill: music by ende.app ("Happy Beats / Business Moves", CC BY 4.0), sound effects by Kenney, video generation via Hyperframes.
