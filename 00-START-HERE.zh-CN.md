# 湛泉的游戏开发仓库总入口

这份文件用于把账号中的游戏相关仓库分成 **成品项目、完整开源游戏、游戏引擎、渲染与底层库、资料索引** 五类，避免把大型上游镜像和自己的项目混在一起。

## 最先看这里

| 目标 | 直接选择 | 说明 |
|---|---|---|
| 继续开发自己的 3D 游戏 | [`wanwu-chengjie`](https://github.com/yniantongtian-oss/wanwu-chengjie) | 当前账号中最接近正式产品的游戏项目 |
| 零代码或低代码做游戏 | [`GDevelop`](https://github.com/yniantongtian-oss/GDevelop) | 带编辑器的完整游戏创作平台 |
| 做通用 2D/3D 独立游戏 | [`godot`](https://github.com/yniantongtian-oss/godot) | 通用开源游戏引擎 |
| 做浏览器 2D 游戏 | [`phaser`](https://github.com/yniantongtian-oss/phaser) | Web 2D 游戏框架 |
| 做浏览器 3D 游戏 | [`three.js`](https://github.com/yniantongtian-oss/three.js) 或 [`Babylon.js`](https://github.com/yniantongtian-oss/Babylon.js) | Web 3D 渲染与游戏开发 |
| 用 C/C++ 快速做小游戏 | [`raylib`](https://github.com/yniantongtian-oss/raylib) | API 简洁，适合学习与原型 |
| 用 Rust 做游戏 | [`bevy`](https://github.com/yniantongtian-oss/bevy) | ECS 驱动的 Rust 游戏引擎 |
| 找可参考的完整游戏 | [`awesome-open-source-games`](https://github.com/yniantongtian-oss/awesome-open-source-games) | 开源游戏案例索引 |
| 找美术、音频和开发工具 | [`magictools`](https://github.com/yniantongtian-oss/magictools) | 游戏开发资源与工具索引 |

---

## A. 自己的成品项目

### 1. 万物成界

仓库：[`wanwu-chengjie`](https://github.com/yniantongtian-oss/wanwu-chengjie)

定位：输入文本、表情或图片，生成 60–90 秒的 3D 异世界挑战。

直接运行：

```bash
git clone https://github.com/yniantongtian-oss/wanwu-chengjie.git
cd wanwu-chengjie
npm ci
npm run dev
```

完整检查：

```bash
npm run check
```

这个仓库应该作为游戏开发工作的主仓库。新增玩法、视觉效果、关卡生成、性能优化和部署功能都优先在这里完成。

---

## B. 完整开源游戏

这些仓库本身是可玩的完整游戏或游戏重制工程，适合学习大型项目结构、玩法系统和内容管线。

| 仓库 | 类型 | 建议用途 |
|---|---|---|
| [`OpenRA`](https://github.com/yniantongtian-oss/OpenRA) | 即时战略游戏引擎与重制项目 | 学习 RTS、地图、单位、联网与模组系统 |
| [`openage`](https://github.com/yniantongtian-oss/openage) | 经典 RTS 引擎重制 | 学习 C++/Python 混合工程与资源转换 |
| [`luanti`](https://github.com/yniantongtian-oss/luanti) | 体素沙盒游戏引擎与平台 | 学习开放世界、体素、模组和多人服务器 |

这些大型仓库更适合作为参考源或二次开发基础，不建议和自己的游戏业务代码混在一起。

---

## C. 完整游戏引擎与框架

### 通用编辑器型引擎

| 仓库 | 语言/平台 | 最适合 |
|---|---|---|
| [`godot`](https://github.com/yniantongtian-oss/godot) | C++ / GDScript / C# | 2D、3D、独立游戏、跨平台发布 |
| [`GDevelop`](https://github.com/yniantongtian-oss/GDevelop) | JavaScript / 编辑器 | 不写代码或少写代码快速做游戏 |
| [`cocos2d-x`](https://github.com/yniantongtian-oss/cocos2d-x) | C++ | 移动端 2D、传统商业游戏项目 |

### 编程框架型引擎

| 仓库 | 语言 | 最适合 |
|---|---|---|
| [`bevy`](https://github.com/yniantongtian-oss/bevy) | Rust | ECS、大型系统化玩法、Rust 学习 |
| [`libgdx`](https://github.com/yniantongtian-oss/libgdx) | Java/Kotlin | Android、桌面、多平台 2D/3D |
| [`MonoGame`](https://github.com/yniantongtian-oss/MonoGame) | C# | 代码驱动的 2D/3D 游戏 |
| [`raylib`](https://github.com/yniantongtian-oss/raylib) | C | 教学、原型、小游戏和图形学入门 |
| [`ebiten`](https://github.com/yniantongtian-oss/ebiten) | Go | Go 语言 2D 游戏 |
| [`pyxel`](https://github.com/yniantongtian-oss/pyxel) | Python | 像素游戏、教学和 Game Jam |
| [`phaser`](https://github.com/yniantongtian-oss/phaser) | TypeScript/JavaScript | 浏览器 2D 游戏 |
| [`engine`](https://github.com/yniantongtian-oss/engine) | JavaScript / WebGL / WebGPU | PlayCanvas 浏览器 3D 游戏 |
| [`Babylon.js`](https://github.com/yniantongtian-oss/Babylon.js) | TypeScript | 浏览器 3D 游戏与可视化 |

### 使用原则

这些仓库大多是上游大型项目的镜像或 Fork：

1. **只是用引擎做游戏**：优先安装发布版本，不要直接修改引擎源码。
2. **要研究引擎底层**：从自己的 Fork 创建独立分支，再提交 Pull Request。
3. **不要把游戏素材和业务代码直接写进引擎仓库**：为每个游戏单独建项目仓库。
4. **不要同时维护多个同类引擎**：每个实际项目只选一个主引擎。

---

## D. Web 3D、渲染和交互库

| 仓库 | 类型 | 适合场景 |
|---|---|---|
| [`three.js`](https://github.com/yniantongtian-oss/three.js) | Web 3D 渲染库 | 自由度高的浏览器 3D 项目 |
| [`Babylon.js`](https://github.com/yniantongtian-oss/Babylon.js) | Web 3D 引擎 | 更完整的游戏功能和工具链 |
| [`aframe`](https://github.com/yniantongtian-oss/aframe) | WebXR 声明式框架 | VR、AR、沉浸式网页 |
| [`pixijs`](https://github.com/yniantongtian-oss/pixijs) | Web 2D 渲染库 | 高性能 2D、粒子、UI 和特效 |

你的《万物成界》已经采用 Three.js / React Three Fiber 路线，因此短期内不应再切换到 Babylon.js、PlayCanvas 或 Godot。除非准备新建完全独立的游戏项目。

---

## E. ECS、调试界面和底层组件

| 仓库 | 分类 | 用途 |
|---|---|---|
| [`entt`](https://github.com/yniantongtian-oss/entt) | C++ ECS | 实体组件系统、事件和资源管理 |
| [`flecs`](https://github.com/yniantongtian-oss/flecs) | C/C++ ECS | 大规模实体与数据驱动架构 |
| [`imgui`](https://github.com/yniantongtian-oss/imgui) | C++ 即时模式 GUI | 游戏内调试器、编辑器、性能面板 |
| [`egui`](https://github.com/yniantongtian-oss/egui) | Rust 即时模式 GUI | Rust 工具和游戏编辑界面 |

这些不是完整游戏引擎。只有在对应语言项目真正需要 ECS 或调试工具时再引入。

---

## F. 游戏开发资料与案例索引

| 仓库 | 内容 | 使用方式 |
|---|---|---|
| [`awesome-gamedev`](https://github.com/yniantongtian-oss/awesome-gamedev) | 引擎、资产、音频、图形工具、学习资料 | 开发前查工具和资源 |
| [`awesome-open-source-games`](https://github.com/yniantongtian-oss/awesome-open-source-games) | 浏览器、桌面和移动端开源游戏 | 找完整项目作为结构参考 |
| [`magictools`](https://github.com/yniantongtian-oss/magictools) | 美术、贴图、音频、关卡编辑和开发工具 | 制作素材或选择工具时查找 |

这些仓库是目录，不是要直接运行的游戏工程。

---

## 推荐的仓库管理结构

以后新增游戏相关仓库时，统一采用下面的逻辑：

```text
games/              自己开发的可玩游戏
prototypes/         7 天以内的实验和玩法原型
engines/            需要研究或修改的引擎 Fork
tools/              自己写的编辑器、构建器、生成器
references/         上游游戏、引擎和资料镜像
assets/             可复用且许可证明确的素材
```

GitHub 账号无法真正建立上述顶层文件夹，因此用仓库命名来表达：

```text
game-项目名
prototype-项目名
engine-项目名
gamedev-tool-项目名
gamedev-reference-项目名
```

现有大型上游仓库可以保留原名，自己的新项目则使用统一前缀。

---

## 当前最合理的开发路线

### 主线：把《万物成界》做成可发布产品

1. 保持 React + TypeScript + Three.js / React Three Fiber 技术栈。
2. 完善移动端触控、资源加载、首屏速度和低端设备兼容。
3. 加入稳定的世界生成输入协议与失败回退。
4. 建立关卡种子复现、性能基准和视觉回归测试。
5. 接入静态部署、错误监控和用户反馈。

### 支线：只保留两个学习方向

- **引擎学习**：Godot 或 Bevy 二选一。
- **完整游戏研究**：OpenRA 或 Luanti 二选一。

不要同时深挖十几个引擎，否则仓库会越来越多，但没有一个产品真正完成。

---

## 新项目选择规则

创建新游戏前先回答四个问题：

1. 是 2D 还是 3D？
2. 是浏览器、手机还是桌面？
3. 是编辑器驱动还是纯代码驱动？
4. 计划多久做出第一个可玩版本？

推荐决策：

```text
浏览器 2D       → Phaser
浏览器 3D       → Three.js / React Three Fiber
无代码快速原型   → GDevelop
通用独立游戏     → Godot
C/C++ 教学原型   → raylib
Rust 游戏        → Bevy
Python 像素游戏  → Pyxel
Go 语言 2D       → Ebitengine
```

同一个项目只保留一个主引擎、一个渲染方案和一套构建系统。
