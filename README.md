# @snow-the/dsh-bundle-core

基礎信任面：總線、快照、插件健檢、會話修復

## 成員

- `dsh-session-bus` → `@snow-the/dsh-session-bus`
- `dsh-snapshot` → `@snow-the/dsh-snapshot`
- `dsh-plugin-doctor` → `@snow-the/dsh-plugin-doctor`
- `dsh-session-repair` → `@snow-the/dsh-session-repair`

## 它解決什麼

profile 的 `dsh.profile.bundles` 從 19 條收成 5 條，讓「裝了什麼、哪一塊負責什麼」一眼看得懂。

## 它不解決什麼

- **不搬程式碼**：成員仍是獨立套件，可以單獨安裝、單獨測試、單獨升級。
- **不保證相依**：這個聚合包的 `dependencies` 是空的，成員由 profile 提供（本機是 `file:` 連結）。要發佈到 npm 就得把成員寫進 `dependencies`，那是另一件事。
- **不是 plugin**：入口是 `export {}`，沒有 `apply`，不會被當成插件載入。
