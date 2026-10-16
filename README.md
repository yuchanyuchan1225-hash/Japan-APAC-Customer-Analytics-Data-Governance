# Japan APAC Customer Analytics & Data Governance — Lifecycle Measurement

[日本語](#日本語) · [中文](#中文) · [English](#english)

---

## 日本語

### 概要

日本市場を起点とする APAC の顧客分析を想定し、注文データから F1（観測期間内の初回成立注文）と F2（2回目以降の成立注文）を扱う際に必要な、顧客識別・注文粒度・例外管理・検算の考え方をまとめた公開ケースです。

このリポジトリは、実務で用いた分析設計を抽象化したものです。実在企業名、顧客情報、注文情報、内部ルール、実績値、元プロジェクトのコードは収録していません。数値例は合成データです。

### このケースで扱うこと

- 商品行と注文行を分けて、注文金額の二重計上を防ぐ
- 会員・ゲスト購入をまたぐ本人性を、根拠付きの分析用キーとして扱う
- F1 / F2 を「観測期間内」の定義として運用する
- 取消注文、内部利用、業務例外を通常の顧客行動と分離する
- 顧客群の売上と F2 注文売上を同じ指標として扱わない
- 再計算と報告で必要な QA ルールを残す

### 公開版の範囲

公開するのは方法論、ページ、合成例のみです。実データ、原始抽出、ID 対応表、顧客や注文の明細、社内ルール、実績を再現できる相対値は含めません。

### Ownership

#### Insight Ownership

注文と顧客データの断絶を分析課題として定義し、F1/F2、顧客群、成立注文を混同しない指標体系を設計。

#### Execution Ownership

データ確認、注文粒度の整理、本人性ルール、例外分類、QA、報告用定義までを一連の分析プロセスとして構築。

#### Ownership Boundaries

公開版は方法論と合成例に限定。実在する顧客、注文、企業、内部運用ルール、実績値は非公開。

---

## 中文

### 概述

这是一个以日本市场为起点、具有 APAC 参考价值的客户分析公开方法论案例，围绕 F1（观察期内首笔已完成订单）与 F2（第二笔及以后已完成订单），重点是顾客识别、订单粒度、例外处理和结果校验。

本仓库从实际分析设计中提炼而来，但不包含真实企业名称、顾客信息、订单信息、内部规则、经营结果或原项目代码。页面中的数字均为合成示例。

### 案例涵盖的判断

- 区分商品行和订单行，避免订单金额重复统计
- 用有依据的分析身份键连接会员与游客购买
- 将 F1 / F2 明确限定为“观察期内”的生命周期定义
- 将取消订单、内部使用和业务例外与正常顾客行为分离
- 不把复购顾客群销售额误称为 F2 订单销售额
- 保留再计算与报告所需的 QA 规则

### 公开边界

公开版只包含方法论、网页和合成示例。不包含真实数据、原始导出、ID 对照表、顾客或订单明细、内部规则，以及可反推实际业绩的相对数值。

### Ownership

#### Insight Ownership

将订单与顾客数据的断裂定义为分析问题，并设计区分 F1/F2、顾客群与已完成订单的指标体系。

#### Execution Ownership

完成从源数据确认、订单粒度整理、身份规则、例外分类、QA 到报告定义的一整套分析流程。

#### Ownership Boundaries

公开版仅展示方法论和合成示例。真实顾客、订单、企业信息、内部规则和经营结果均不公开。

---

## English

### Overview

This public methodology case starts with a Japan-market customer analytics context and has wider APAC relevance. It explains the controls needed to measure F1 (a first completed order within an observation window) and F2 (a later completed order): customer identity, order grain, exception handling, and reconciliation.

It abstracts an applied analytical design. The repository does not contain company names, customer or order records, internal operating rules, production outcomes, or source-project code. All numerical examples are synthetic.

### What the case covers

- Separating item lines from order records to prevent double counting
- Resolving account and guest evidence into a documented analytical identity
- Treating F1 and F2 as observation-window definitions
- Separating cancellations, internal use, and operational exceptions from ordinary demand
- Keeping repeat-customer contribution distinct from F2-order revenue
- Retaining QA rules needed for reproducible reporting

### Public boundary

This edition contains only methodology, web pages, and synthetic examples. It excludes production data, source exports, identity bridges, customer or order details, internal rules, and relative metrics that could reconstruct actual performance.

### Ownership

#### Insight Ownership

Defined disconnected order and customer records as a measurement problem, then designed a metric system that keeps lifecycle stages, customer groups, and completed orders distinct.

#### Execution Ownership

Built the analysis process from source review and order-grain design through identity rules, exception classification, QA checks, and reporting definitions.

#### Ownership Boundaries

The public edition contains methodology and synthetic examples only. Production customers, orders, company information, internal operating rules, and outcomes remain private.

---

## Local preview

Open `index.html` in a browser. Japanese is the default page. The Chinese and English editions are available at `zh.html` and `en.html`.
