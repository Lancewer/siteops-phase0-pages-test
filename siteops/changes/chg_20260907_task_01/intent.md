# Intent — chg_20260907_task_01

## 变更概述
新建一个极简的计算器页面。站点无既有框架与构建配置（framework 未配置，package_manager/install/build 命令均为空），按 plainspec 方式交付：纯静态 HTML + 内联 CSS/JS，单文件即可运行，无需构建步骤。

## 用户意图（原文）
> 新建一个极简的计算器页面

## 关键决策
- 交付形态：`public/index.html` 单文件静态页面（无框架、无构建、无外部依赖）。
- 功能范围：四则运算（加、减、乘、除）、清除（C）、等号（=）；键盘数字与运算符输入可选实现，属 nice-to-have。
- 不引入任何第三方库/CDN，保证可离线打开。
- 仅允许写入 `public/**`；不触碰 `.env*`、`secrets/**`、`siteops/changes/**`。

## 成功标准（与 change.yaml intent.success_criteria 一致）
1. `public/index.html` 存在且为非空有效 HTML 文件（含 `<!DOCTYPE html>` 与基本结构）。
2. 页面包含计算器 UI：数字键 0–9、运算符 + − × ÷、清除键、等号键、显示区。
3. 四则运算结果正确：抽查 2+3=5、7−4=3、6×8=48、9÷3=3、10÷4=2.5、连续运算 1+2+3=6、除零显示错误。
4. 页面无外部网络依赖（无 http(s) 引用的 script/link/img 资源），本地直接打开即可使用。
5. 未写入任何 scope 之外的路径（无 `.env*`、`secrets/**`、`siteops/changes/**` 变更）。

## 非目标（Non-goals）
- 不做科学计算、百分比、括号、历史记录等进阶功能。
- 不做路由、多页面、主题切换、响应式精调（仅保证基本可用布局）。
- 不配置 Pages 部署、不修改站点配置。
