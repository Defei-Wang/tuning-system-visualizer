# Tuning System Visualizer | 音律代数推演可视化

[English](#english) | [中文](#chinese)

---

<h2 id="english">English</h2>

### Abstract
An interactive, zero-dependency browser visualization tool designed to prove the algebraic inconsistency of Pythagorean Tuning and demonstrate the mathematical necessity of the 12-Tone Equal Temperament (12-TET).

The core logic addresses the fundamental conflict in acoustics: the impossibility of forming a closed loop using rational number frequency ratios (pure fifths, $3:2$) within the bounds of perfect octaves ($2:1$).

### Mathematical Model
1. **The Logarithmic Scale (Cents):**
   The human perception of pitch is logarithmic. To convert frequency ratios into linear additions, one octave is defined as 1200 Cents:
   $$n = 1200 \times \log_2\left(\frac{f_2}{f_1}\right)$$
2. **Pythagorean Comma (System Boundary):**
   Iterating a pure fifth ($3:2$) 12 times yields $1200 \times \log_2(1.5) \times 12 \approx 8423.46$ cents. Subtracting 7 perfect octaves ($8400$ cents) leaves a remainder of **23.46 cents**. The system fails to close.
3. **12-TET Resolution:**
   Introduces the irrational number $\sqrt[12]{2}$ to linearly distribute the 23.46-cent error across all keys, forcing system boundary alignment at exactly 700.00 cents per fifth.

### Features
* **Web Audio API Engine:** Generates pure sine waves mapping to computed frequencies.
* **Acoustic Interference Testing:** Plays dual-system frequencies simultaneously to expose the "Beat Frequency" (amplitude modulation) caused by microtonal discrepancies.
* **Pure Static Deployment:** No backend dependencies. Vanilla JS/CSS/HTML.

---

<h2 id="chinese">中文</h2>

### 摘要
一个无依赖的浏览器原生交互式可视化工具，旨在通过代数推演与声学干涉，验证五度相生律的系统非自洽性，并展示十二平均律在系统闭环重构中的数学必然性。

核心逻辑直击声学底层悖论：在绝对八度（$2:1$）的边界内，基于有理数频率比（纯正五度，$3:2$）推演的离散系统无法实现代数闭环。

### 数学模型
1. **对数尺度（音分 Cents）：**
   人耳对频率的感知呈对数关系。为将比率转化为线性加减，系统定义绝对八度为 1200 音分：
   $$n = 1200 \times \log_2\left(\frac{f_2}{f_1}\right)$$
2. **毕达哥拉斯音差（系统边界）：**
   纯正五度（$3:2$）累加 12 次结果为 $1200 \times \log_2(1.5) \times 12 \approx 8423.46$ 音分。扣除 7 个绝对八度（$8400$ 音分）后，残余 **23.46 音分**。系统无法闭合。
3. **十二平均律重构：**
   引入无理数 $\sqrt[12]{2}$，将 23.46 音分的代数误差线性均摊，强制每个五度精确对齐至 700.00 音分，实现边界闭合与自由转调。

### 核心功能
* **物理声学引擎：** 基于 Web Audio API 实时合成推演坐标对应的正弦物理声波。
* **拍频干涉测试：** 同步触发两套系统的发声器，利用微观频率差引发的振幅调制（Beat Frequency）直接暴露物理冲突。
* **纯静态架构：** 零后端计算，原生 JS/CSS/HTML。
