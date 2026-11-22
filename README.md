# Silicon Oasis Launcher

> Official launcher for **Silicon Oasis** 《硅基绿洲》 — a cozy post-apocalyptic base-building game about grafting e-waste into plants.

**Status: early development.** No builds yet. Watch this repo to get notified.

---

## Why a separate launcher?

Unity games cannot self-update. This launcher handles what the game itself can't:

- **Update check & download**
- **Version rollback** — if a new build breaks, go back
- **File integrity verification** — repair corrupted or missing files
- **Graphics / resolution / language settings** before launch

Deliberately minimal: no login, no news feed, no community tab. Those live on the website. A launcher is something users wait for — keep it fast.

## Tech stack

- **Avalonia UI** + **.NET 8** — Windows / Linux / macOS
- **Self-contained publish** — end users need no runtime installed
- Chosen over WPF because WPF is Windows-only and the game targets Linux first.

## Build from source

Requires the .NET 8 SDK.

```bash
dotnet restore
dotnet build
dotnet run --project src/Launcher
```

## Roadmap

- [ ] Avalonia project scaffold
- [ ] Read update manifest, compare versions
- [ ] Download and apply package
- [ ] SHA-256 integrity verification
- [ ] Settings UI (resolution / quality / language)
- [ ] Version rollback

## Related

| | |
|---|---|
| Game repo | `github.com/MochiIceSnow/silicon-oasis` *(soon)* |
| Website | `kjsio.com` *(soon)* |
| Developer | KJ Studio / MochiIceSnow |

## License

**MIT** — see [LICENSE](LICENSE). Fork it, learn from it, ship your own.

---

<details>
<summary>中文说明</summary>

**硅基绿洲启动器** —— 官方启动器，负责更新检测、版本回滚、文件完整性校验与画质设置。

Unity 游戏本体无法自我更新，所以独立出一个启动器；除此之外不做多余功能（不带登录、不带公告、不带社区），因为它每次启动都要被等待，越轻越好。

技术栈：Avalonia UI + .NET 8，支持 Windows / Linux / macOS。选 Avalonia 而不是 WPF 的原因是新版 WPF 仅支持 Windows，而本游戏以 Linux 为优先保障平台。

当前处于早期开发阶段，暂无可用构建。

</details>
