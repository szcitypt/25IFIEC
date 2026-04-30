# MTC-YK — 课程/审批用提交包说明

本目录 **`MTC-YK`** 由完整工程 **`MTC-Cursor`**（同源：MnemoTranscode / MTC）精简复制而来，便于审阅与存档：已排除 `node_modules`、Python 缓存、`frontend` 构建缓存及本机 **`backend/.env`**（避免泄露密钥）。

## 与上游目录关系

| 路径 | 说明 |
|------|------|
| `d:\Fish-code\MTC\MTC-Cursor` | 日常开发主仓库（含本地 `node_modules` 等） |
| `d:\Fish-code\MTC\MTC-YK` | **本包**：结构一致、无依赖目录、无私密 env |
| `d:\Fish-code\MTC\` 下的 `*.pptx` / `*.docx` / 截图 | 路演材料在上级 `MTC` 目录，未重复打包进本文件夹 |

## 建议阅读顺序（审批）

1. **`docs/实现过程-审批版.md`** — 提炼后的实现过程与技术要点（中文）。  
2. **`docs/ARCHITECTURE.md`** — 系统分层与组件关系。  
3. **`docs/SPEC.md`** — 功能规格与业务边界。  
4. **`README.md`** — 与原仓库一致的全量说明与启动方式。

## 本地可运行性（老师或助教验收）

1. 安装 **Docker / Docker Compose**、**Node.js 18+**、**Python 3.11+**（与主 README 一致）。  
2. `cp backend/.env.example backend/.env`（或在 Windows 上复制后重命名），填写至少 **`SECRET_KEY`**、**LLM_API_KEY** 等。  
3. `frontend` 目录执行 **`npm install`** 后 **`npm run dev`**（本机热重载）；或按主 README 使用 **`infra/docker-compose.yml`** 起全栈。  
4. Windows 混合开发可用项目根 **`scripts/start-stable.ps1`**（参见 `README.md` 与 `docs/stable-dev-windows.md`）。

## 可选精简

若课程要求「仅源代码与文档」，可手动删除 **`MTC-YK/.cursor`**（编辑器规则与 Skill，不参与运行时）。

——  
*MTC — Memory To Code（MnemoTranscode）*
