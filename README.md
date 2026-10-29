# Product Display Board Skill

工业产品宣传展示板生成技能包。给定一张产品实拍图 + 一句产品信息，产出一段可直接喂给 AI 绘图工具的完整提示词，快速生成左右分栏版式的工业产品宣传展示板效果图。

## 目录结构

```
.
├── README.md
├── LICENSE
└── skills/
    └── product-display-board/
        └── SKILL.md
```

## 技能说明

- **名称**：`product-display-board`
- **触发场景**：用户提供模板图/产品图，要求"以模板为参考""生成同款展示板""按这个版式出图"
- **输入**：产品实拍图、产品全称、核心卖点、规格参数、配件清单
- **输出**：一段完整的中文生图提示词（左右分栏、浅灰背景、铝合金工具箱 + EVA 海绵内衬、3×2 参数卡片），可直接复制到 AI 绘图工具出图

典型用途：无人机实训箱、工具箱、教学套件、工业设备等产品的宣传展示板 / 详情页首屏图。

## 在支持 SKILL.md 规范的 Agent 中调用

只要把本仓库 clone 到本地技能目录，或通过对应平台的插件安装命令拉取，Agent 会自动识别 `skills/product-display-board/SKILL.md`。

### 手动安装

```bash
# clone 到你的技能根目录
git clone https://github.com/17702371576/product-display-board-skills.git /path/to/skills-root/

# 或单独取这一个技能
git clone --depth 1 https://github.com/17702371576/product-display-board-skills.git /tmp/pdb
cp -r /tmp/pdb/skills/product-display-board /path/to/your-skills/
```

## 使用示例

```
用户：帮我做一个 GJ-550 无人机组装调试箱的宣传展示板，参考左右分栏版式。
Agent：按 skills/product-display-board/SKILL.md 中的"生成词模板"填充参数，
       输出完整提示词，可直接提交给图像生成工具。
```

## License

MIT
