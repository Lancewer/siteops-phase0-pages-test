# Approval Brief — chg_20260907_task_01（Gate: execution）

> 本简报为视图：引用内容逐字来自工件原文，以【证据】段 sha256 为锚；历史版本见 Git 记录。

## 【红旗】

无

## 【意图】

> 原文逐字引用（change.yaml intent）

新建一个极简的计算器页面

- public/index.html 存在且为有效 HTML（含 DOCTYPE、viewport meta、显示区元素）
- 页面含数字键 0-9、运算符 + − × ÷、C 与 = 键
- 四则运算抽查全部正确（2+3=5、7−4=3、6×8=48、9÷3=3、10÷4=2.5、连续运算 1+2+3=6）
- 除零显示 Error，C 键复位显示 0
- 页面无任何 http(s) 外部资源引用，本地直接打开可用
- 未写入任何 scope 之外的路径（无 .env*、secrets/**、siteops/changes/** 变更）

## 【权限边界】

允许写入路径：
- public/**

禁止写入路径：
- .env*
- secrets/**
- siteops/changes/**

允许路由前缀：（无）

## 【计划】

- T001 新建极简计算器页面 public/index.html — 交付单文件、零依赖的静态计算器页面：内联 CSS 网格布局，原生 JS 实现 四则运算、连续运算、除零报错与清空复位，满足 spec.md 全部验收用例。（预估 diff 规模上限 — 文件 / 300 行（任务声明））

## 【证据】

- change.yaml（meta/intent 来源，不参与 hash 锁定） — sha256:7a6ebdbfeeeb5096ec41eb86d09f716df757206cdaaa3db69f949c48f34f258d — `siteops/changes/chg_20260907_task_01/change.yaml`
- intent `siteops/changes/chg_20260907_task_01/intent.md` — sha256:f458b267979010d0eb0ddc106480b72605af3eea76862dffad294b743cd004ab
- context `siteops/changes/chg_20260907_task_01/context.md` — sha256:8e1c3d40ca859677f5ca75a90a48ff27eb7b1889ff8814c65862027899ba1342
- spec `siteops/changes/chg_20260907_task_01/spec.md` — sha256:79917bf8a86398829c7f5a3d61e6054842d7425808e4613585c2460d75bde3ea
- plan `siteops/changes/chg_20260907_task_01/plan.md` — sha256:d12334901df169d851982a6b77458cbc120f03c08371b9ebb15b56a3c775c9c7
- tasks `siteops/changes/chg_20260907_task_01/tasks.yaml` — sha256:ca174d05bc9c6cc93873cb40414a9feb266aaa59063b88ebe1095d206ac3dcae
- contract `siteops/changes/chg_20260907_task_01/contract.md` — sha256:d8add7de879dc7bb32372044bdf64260454db83051c77c1fb5a681582b82772b
- verification `siteops/changes/chg_20260907_task_01/verification.yaml` — （工件缺失）
