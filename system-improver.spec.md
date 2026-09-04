# Spec: System Improver (Genesis v0.1)

## 1. 系统本原定义（First Principles）
- **地位隔离**：
  - `02-[spec]-knowledge-humanzone/**` 为人类意图空间（主要交付物），对AI系统是**绝对只读（Read-Only）**，除非人类明确要求AI修改其中内容。
  - 项目中的代码、配置、技能、文档等均为衍生交付物（Derived Artifacts）。
- **平凡公理（Null Identity）**：
  - 若 `02-[spec]-knowledge-humanzone/` 下除本规范外无其他内容，系统处于完全平凡状态（No-Op），不修改项目内任何文件，不制造任何副作用。

## 2. 调和生命周期（Reconsiliation SOP）
每次人类要求执行系统改进时，AI系统执行以下四步：
1. **意图解析**：扫描 `02-[spec]-knowledge-humanzone/` 下的所有内容，提取人类显式声明的约束和断言。
2. **现状审计**：检查项目内衍生交付物（代码、测试、配置等）是否与提取出的约束存在偏差（Drift）。
3. **收敛修复**：针对偏差，执行严格忠实于 `02-[spec]-knowledge-humanzone/` 下内容的修复，使之收敛。
4. **建议提炼（可选）**：若发现未受管的高频重复模式或野生资产，仅把建议输出为.md文档并保存至 `90-worklog/suggestions-for-humanzone-update/`下，严禁私自修改 `02-[spec]-knowledge-humanzone/`。

## 3. For human only. Ignore if you are AI
初次使用时，将下面的提示词丢给你的AI：

- 根据 @02-[spec]-knowledge-humanzone/9999-system-improver/system-improver.spec.md，在 `10-[artifact]-skills/9999-system-improver/SKILL.md` 生成对应的初始技能（作为衍生交付物），然后软连接到你的默认技能目录，作为一个新的“improve-system” skill 存在。
