---
theme: default
title: Field Notes
author: WAKATO
aspectRatio: 16/9
canvasWidth: 980
colorSchema: light
transition: fade
fonts:
  provider: none
defaults:
  layout: atmos-content
layout: atmos-cover
kicker: ENGINEERING / FIELD NOTES
---

# Beyond the<br>Architecture.

複雑さの先にある、設計の本質。

<span class="atmos-caption">WAKATO &nbsp; / &nbsp; @0ts_st</span>

---
layout: atmos-content
kicker: 01 / CONTEXT
---

# 設計は、何のためにあるのか。

複雑さをなくすのではなく、変化に耐えられる形へ整える。

- 変更の影響範囲を小さくする
- 責務と依存の方向を明確にする
- チームが理解できる構造を保つ

<v-click>

**選択の理由を、コードに残す。**

</v-click>

---
layout: atmos-section
kicker: 02 / STRUCTURE
---

# 境界を、<br>デザインする。

Structure follows intention.

---
layout: atmos-content
kicker: 02 / STRUCTURE
---

# 依存の方向を制御する。

<div class="grid grid-cols-2 gap-12 items-center">

<div>

ビジネスロジックを<br>外部技術の変更から守る。

<Counter />

</div>

<svg viewBox="0 0 360 270" role="img" aria-label="同心円によるレイヤー構造の模式図" class="w-full">
  <circle cx="180" cy="135" r="112" fill="#d9e2de" stroke="#6f8c88"/>
  <circle cx="180" cy="135" r="79" fill="#e4eae5" stroke="#6f8c88"/>
  <circle cx="180" cy="135" r="43" fill="#f1f0eb" stroke="#507773"/>
  <g fill="#334b4e" font-size="11" text-anchor="middle" font-family="sans-serif">
    <text x="180" y="49">INFRASTRUCTURE</text>
    <text x="180" y="74">USE CASE</text>
    <text x="180" y="139">DOMAIN</text>
  </g>
</svg>

</div>

---
layout: atmos-code
kicker: 03 / IMPLEMENTATION
---

# 小さなインターフェースから始める。

```go
type Repository interface {
    Find(ctx context.Context, id string) (User, error)
}

type Service struct {
    repo Repository
}

func (s *Service) Get(ctx context.Context, id string) (User, error) {
    return s.repo.Find(ctx, id)
}
```

依存の方向を、型で表現する。

---
layout: atmos-quote
kicker: 04 / REFLECTION
---

# 複雑さは消せない。<br>しかし、制御することはできる。

---
layout: atmos-closing
kicker: END OF SESSION
---

# Thank you.

Let's talk about engineering.

<span class="atmos-caption">WAKATO &nbsp; / &nbsp; @0ts_st</span>
