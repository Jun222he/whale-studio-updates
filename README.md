# Whale Studio Updates

Whale Studio 的自動更新 manifest 與 release assets。

end user 的 IDE 透過「系統更新」頁面從這個 repo 抓 `manifest.json`，比對版本後提示更新。

## Release 命名規則

- IDE：tag = `ide-vX.Y.Z`，asset = `whale-studio-X.Y.Z.zip`
- Server：tag = `server-vX.Y.Z`，asset = `l1jgo-vX.Y.Z.zip`

## manifest.json 結構

```json
{
  "ide": { "version", "url", "sha256", "size", "changelog", "releasedAt" },
  "server": { "version", "url", "sha256", "size", "changelog", "releasedAt" }
}
```

兩段都 optional — 只發 server 更新就只寫 server 段。
