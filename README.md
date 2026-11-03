# 🎮 AI 3D 解压按按乐工坊 (AI Decompress Toy Studio)

> **Zero-Code 3D Fidget Toy Creator Powered by AIGC & Precision Mechanical Switch Engineering**  
> 零门槛 AIGC 个性化 3D 潮玩定制与实体机械轴按按乐制造工坊

[![Vue 3](https://img.shields.io/badge/Vue-3.x-42b883?style=flat&logo=vuedotjs)](https://vuejs.org/)
[![Three.js](https://img.shields.io/badge/Three.js-r128+-black?style=flat&logo=threedotjs)](https://threejs.org/)
[![FastAPI](https://img.shields.io/badge/FastAPI-0.100+-009688?style=flat&logo=fastapi)](https://fastapi.tiangolo.com/)
[![Python CAD](https://img.shields.io/badge/CAD-Trimesh%20%2F%20OpenCASCADE-blue?style=flat)](https://github.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## ✨ 核心特性 (Key Features)

1. **🎨 2D 图片一键生成 3D 浮雕与立体手办**
   - **极简光滑模式**：细腻搪胶曲面，支持自适应轮廓高光与圆润倒角。
   - **体素积木模式**（借鉴 Minecraft 风格）：3D 实体像素方块手办，全方位立体造型。
2. **⚙️ 工业级机械轴内胆与万能 5 脚底座**
   - **手办上盖**：几何中心精密掏出 Cherry MX 标准十字插槽（$4.10 \times 1.30\text{ mm}$，公差 $+0.18\text{ mm}$）与 $14.2 \times 14.2 \times 5.0\text{ mm}$ 行程避空腔。
   - **万能底座**：$20 \times 20 \times 8\text{ mm}$ 独立底盘，配备 $14.0 \times 14.0\text{ mm}$ 卡轴咬合框，通用 5 脚孔位（完全兼容 3 脚与 5 脚机械轴盲插），边角集成 $\Phi 3.5\text{ mm}$ 挂绳孔。
3. **⌨️ 交互式客制化调色与轴体体验**
   - 预设经典手感：青轴（爽脆）、红轴（轻音线性）、茶轴（微段落）、静音轴。
   - 3D 轴体实时自定义：自由调节轴芯颜色、轴壳透明度（透光水晶壳、奶白润光滑、经典黑壳）。
4. **🌿 日系清新文具手绘视觉**
   - 抹茶绿（`#91BF6E`）与奶油黄（`#FEF8DA`）温暖配色，圆润手绘风格功能按键。
   - 真实按压弹跳动效与高保真咔哒机械点击音效。

---

## 🏗️ 架构与技术栈 (Tech Stack)

```
DecompressToy/
├── frontend/                # 前端 (Uni-app Vue3 + Vite + TypeScript + Three.js)
│   ├── src/
│   │   ├── components/
│   │   │   ├── FidgetViewer.vue         # 经典键帽 3D 渲染与矩阵排版
│   │   │   └── FigurineFidgetViewer.vue # 独立异形手办与机械轴选配
│   │   └── pages/index/index.vue        # 3 栏拖拽主工作台
├── backend/                 # 后端 (FastAPI + Trimesh + NumPy)
│   ├── cad/
│   │   ├── mx_stem_base.py              # 标准 Cherry 轴座母口模具生成
│   │   └── mx_universal_dock.py         # 万能 5 脚独立底托 CAD 生成
│   ├── figurine/
│   │   └── voxel_figurine_builder.py    # 2D 轮廓体素化生成器
│   └── api/
└── docs/                    # 完整设计与工程资产文档
    ├── PRD.md                           # 产品需求文档 (基于《产品定义实战课》标准)
    ├── API_CONTRACT.md                  # RESTful 接口交互规范
    └── PROMPTS_WORKFLOW.md              # 全流程经过验证的黄金提示词手册
```

---

## 🚀 极速起步 (Quick Start)

### 1. 前端启动 (Web / H5)
```bash
cd frontend
npm install
npm run dev -- --host
```
* 本地访问：`http://localhost:5173`
* 局域网手机访问：`http://[你的局域网IP]:5173`

### 2. 后端服务启动
```bash
cd backend
pip install -r requirements.txt
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

---

## 🖨️ 3D 打印与免工具物理拼装 (Assembly Guide)

1. **切片建议**：
   - 工艺推荐：SLA 光敏树脂（韧性/高精树脂）或 FDM（层高 $\le 0.16\text{ mm}$）。
2. **装配步骤（3 秒徒手完成）**：
   - 第一步：将机械轴（3 脚或 5 脚均可）对准底座卡槽，垂直向下卡紧至底座定位板。
   - 第二步：将手办上盖的底部十字槽对准轴芯，向下一按卡牢。
   - 第三步：穿上挂绳，开盒即按，享受解压！

---

## 📄 开源许可证 (License)
本项目基于 [MIT License](LICENSE) 开源。
