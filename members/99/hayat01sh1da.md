# @hayat01sh1da

## 1. プロフィール

<img width="300" alt="みゆき" src="https://github.com/user-attachments/assets/f014b5f4-65f5-4d38-a2fc-16135b3e1362" />

- 氏名: 石田隼人
- 出身: 埼玉県
- 開発ドメイン: 教育(一身上の都合でお休み中)
- 趣味:
  - 愛猫(三毛猫♀)との戯れ🐈
  - アコースティックギター🎸
  - カラオケ🎤
  - LIVE 鑑賞(去年から今年にかけては Oasis と B'z と小田和正、今月は Pearl 主催イベントで Shane Gaalaas とラルクの yukihiro)
 
## 2. Ruby / Rails 周り(WIP)

- DHH の例の Keynote Speech は行間をめっちゃ汲み取る必要があるなと思った
  - Rails World という集大成の場で「Rails はもう終わり、これからは Rust だ！」は額面通りに受け取ってしまうと、とりわけコミッターやメンテナーが「やってらんねえよ」と匙を投げるリスクがあるので、そんな誰でも分かりそうな結末に着地するような愚かなことは作者自身がするとは思えなかった
  - Rails という良い意味で枯れた = アーキテクチャ(Philosophy)やフレームワーク層の最適解に則っていたから移行出来た単なる一例ではないだろうか？
  - "Rails is dead." は漸進的にはそうなるとは思うが、すぐにはそうならないと思った
    - Rails のフレームワーク層の挙動を堅牢・高速に出来る && アプリ層に書くコードの可読性を損なわない代替フレームワーク・言語の候補がある → Rails にこだわる必要はなくなっていく
    - 複雑なドメインが落とし込まれたプロダクトは以降難易度が高いので簡単にはいかないはず
  - "Rails is dead."  → "Ruby is dead." ?
    - Ruby がこれほど広まったのは Rails の普及が大きく寄与してきたので、Rails が終わったら Ruby を製品で採用する理由がなくなりそう

## 3. その他開発回り

- AI はコードを書かせるよりも、運用保守を試行錯誤しながら最適化していく方が有効な使い道という個人的所感

## 4. 最近の四方山

<img width="300" alt="Gibson Custom Shop Hummingbird Torch -Ebony Gloss-" src="https://github.com/user-attachments/assets/db853c35-b4ac-4fc7-963e-1797d8f3379a" />

↑ Gibson Custom Shop Hummingbird Torch -Ebony Gloss- というお高い(¥536,000)エレアコギターを8月の頭に一括で買ってしまい緊縮財政中(懇親会不参加でお願いします)

---

<details>
<summary>個人メモ</summary>

## 5. The History of Ruby

### 5.1 Timeline

```mermaid
timeline
    title Ruby: from a toy language to 4.0
    section Birth (1.x)
        1993 : Matz starts designing Ruby (named on 24 Feb 1993)
        1995 : First public release 0.95 on Japanese newsgroups
        1996 : Ruby 1.0 (25 Dec)
        2003 : Ruby 1.8 - the version Rails was born on
        2007 : Ruby 1.9.0 - YARV VM (Koichi Sasada) and M17N strings
    section Maturity (2.x)
        2013 : Ruby 2.0 (20th anniversary) - keyword args, refinements, Module#prepend
        2013-2019 : A minor release every Christmas, from 2.1 (generational GC) to 2.7 (pattern matching, experimental)
        2018 : Ruby 2.6 - MJIT, the first JIT
    section Performance and concurrency (3.x)
        2020 : Ruby 3.0 - "Ruby 3x3" achieved, Ractor, Fiber Scheduler, RBS
        2021 : Ruby 3.1 - YJIT (Shopify), debug.gem, error_highlight
        2022 : Ruby 3.2 - production-ready YJIT, WASI support, Data class
        2023 : Ruby 3.3 - Prism parser, M:N threads, faster YJIT
        2024 : Ruby 3.4 - Prism by default, it block param, frozen string literal warnings
    section 30th anniversary (4.x)
        2025 : Ruby 4.0 (25 Dec) - ZJIT (experimental), Ruby Box (namespace isolation), Ractor improvements
        2026 : 4.0.x patch releases (4.0.7 on 15 Sep 2026), with 3.4.x still maintained
```

### 5.2 Minor releases per major version

```mermaid
xychart-beta
    title "Ruby: minor releases per major line"
    x-axis ["1.x (1996-2007)", "2.x (2013-2019)", "3.x (2020-2024)", "4.x (2025-)"]
    y-axis "Minor releases" 0 --> 10
    bar [6, 8, 5, 1]
```

> 1.x = 1.0, 1.2, 1.4, 1.6, 1.8, 1.9 (1.1/1.3/1.5/1.7 were development branches) / 2.x = 2.0 to 2.7 / 3.x = 3.0 to 3.4 / 4.x = 4.0

### 5.3 Support lifecycle of recent branches

```mermaid
gantt
    title Ruby branch lifecycle (release to EOL, approximate)
    dateFormat YYYY-MM-DD
    axisFormat %Y
    section 2.x
        2.7 : 2019-12-25, 2023-03-31
    section 3.x
        3.0 : 2020-12-25, 2024-04-23
        3.1 : 2021-12-25, 2025-03-26
        3.2 : 2022-12-25, 2026-03-31
        3.3 : 2023-12-25, 2027-03-31
        3.4 : 2024-12-25, 2028-03-31
    section 4.x
        4.0 : 2025-12-25, 2029-03-31
```

> EOL dates for 3.3 and later follow the usual "about 3 years and 3 months" pattern. They are planned dates, not confirmed ones.

### 5.4 Key points

- **1.x: building the language (1993-2012)**
  - Matz wanted "a language more powerful than Perl and more object-oriented than Python", built on the idea of **developer happiness**.
  - Ruby 1.8 got worldwide attention because of Rails (2004-). Ruby 1.9 replaced the AST interpreter with the **YARV** bytecode VM and added encoding-aware strings. The 1.8 to 1.9 migration was painful and took the community years.
- **2.x: steady yearly releases (2013-2019)**
  - Since 2.1, a new minor version has come out **every 25 December**, and this rhythm continues today.
  - Main additions: keyword arguments, refinements, generational and incremental GC (2.1/2.2), `&.` (2.3), MJIT (2.6), compaction GC and experimental pattern matching (2.7).
- **3.x: speed, concurrency and types (2020-2024)**
  - **Ruby 3x3**: Ruby 3.0 is about 3x faster than 2.0 on benchmarks such as Optcarrot.
  - Concurrency: Ractor (actor-style parallelism), the Fiber Scheduler (non-blocking I/O) and M:N threads (3.3).
  - Types: RBS signatures and TypeProf, without changing the language syntax.
  - JIT: **YJIT** (made by Shopify, 3.1) replaced MJIT as the JIT to use in practice. It is production ready since 3.2 and powers large Rails apps.
  - Tooling: the **Prism** parser became the default in 3.4.
- **4.x: the 30th-anniversary major release (2025-)**
  - Ruby 4.0 came out on 25 Dec 2025, 30 years after Ruby 1.0. Its main features are experimental: **ZJIT** (a method-based JIT, the next step after YJIT) and **Ruby::Box** (isolated namespaces for definitions and loaded libraries).
  - As of Oct 2026, the latest releases are **4.0.7** (15 Sep 2026) and **3.4.11** (23 Sep 2026).

## 6. The History of Rails

### 6.1 Timeline

```mermaid
timeline
    title Ruby on Rails: from Basecamp extraction to "No PaaS Required"
    section Birth
        2004 : DHH extracts Rails from Basecamp, open-sourced in July
        2005 : Rails 1.0 (Dec) - "Blog in 15 minutes", MVC, ActiveRecord, convention over configuration
    section REST and growth
        2007 : Rails 2.0 - RESTful resources by default
        2009 : Rails 2.3 - Rack, engines, templates
    section Merb merger
        2010 : Rails 3.0 - merged with Merb, Bundler, ARel, unobtrusive JS
        2011 : Rails 3.1 - Asset Pipeline (Sprockets), jQuery, CoffeeScript
    section Modernisation
        2013 : Rails 4.0 - Turbolinks, strong parameters, Russian-doll caching
        2014 : Rails 4.2 - Active Job, Web Console
        2016 : Rails 5.0 - Action Cable, API-only mode
        2018 : Rails 5.2 - Active Storage, encrypted credentials
        2019 : Rails 6.0 - Action Mailbox, Action Text, multi-DB, Zeitwerk, Webpacker by default
    section Hotwire era
        2021 : Rails 7.0 - Hotwire (Turbo and Stimulus), import maps, no Node.js needed
        2023 : Rails 7.1 - Dockerfile generation, async queries, normalizes
        2024 : Rails 7.2 - dev containers, RuboCop and Brakeman by default, new maintenance policy
    section No PaaS Required
        2024 : Rails 8.0 (Nov) - Solid Queue/Cache/Cable, Kamal 2, Thruster, Propshaft, built-in authentication
        2025 : Rails 8.1 (Oct) - Active Job Continuations, structured event reporting, local CI
        2026 : 8.1.x patch releases (8.1.4 on 24 Sep 2026), no Rails 9 announced at Rails World 2026
```

### 6.2 Time between major versions

```mermaid
xychart-beta
    title "Rails: months since the previous major version"
    x-axis ["2.0 (2007)", "3.0 (2010)", "4.0 (2013)", "5.0 (2016)", "6.0 (2019)", "7.0 (2021)", "8.0 (2024)"]
    y-axis "Months" 0 --> 40
    bar [24, 33, 34, 36, 38, 28, 35]
```

### 6.3 Minor releases per major version

```mermaid
xychart-beta
    title "Rails: minor releases per major line"
    x-axis ["1.x", "2.x", "3.x", "4.x", "5.x", "6.x", "7.x", "8.x"]
    y-axis "Minor releases" 0 --> 5
    bar [3, 4, 3, 3, 3, 2, 3, 2]
```

> 1.0-1.2 / 2.0-2.3 / 3.0-3.2 / 4.0-4.2 / 5.0-5.2 / 6.0-6.1 / 7.0-7.2 / 8.0-8.1 (as of Oct 2026)

### 6.4 How the frontend approach changed

```mermaid
flowchart LR
    A["Prototype.js / RJS<br/>(1.x-2.x)"] --> B["jQuery + UJS<br/>Asset Pipeline (3.x)"]
    B --> C["Turbolinks<br/>(4.x-5.x)"]
    C --> D["Webpacker<br/>(6.x)"]
    D --> E["Hotwire + import maps<br/>(7.x)"]
    E --> F["Propshaft, no build step<br/>(8.x)"]
```

### 6.5 Key points

- **Extracted, not designed**: Rails was taken out of a real product (Basecamp). The ideas that shaped the whole ecosystem were **Convention over Configuration**, **DRY** and later **The Rails Doctrine** (2016).
- **The Merb merger (3.0)** made Rails modular (Railties, ARel, Bundler) and ended the split in the community.
- **The "majestic monolith"** came back in the 7.x era. Instead of following SPA trends, Rails moved to **HTML-over-the-wire** with Hotwire and dropped the Node.js toolchain.
- **Rails 8, "No PaaS Required"**: the Solid trifecta (database-backed queue, cache and websockets) removes Redis. Kamal 2 and Thruster deploy to any server, and built-in authentication removes the need for Devise in simple cases. The aim is that **one developer can build and run a full app**.
- **Release policy (since 7.2)**: a minor version gets about **1 year of bug fixes and 2 years of security fixes**. Releases follow a **yearly rhythm, announced around Rails World** (2023: 7.1, 2024: 8.0, 2025: 8.1).
- **As of Oct 2026**: the latest stable version is **8.1.4** (24 Sep 2026), and 8.0.x still gets security fixes.

## 7. The Summary of DHH's Keynote Speech at Rails World 2026

- Video: [Rails World 2026 Opening Keynote - DHH](https://www.youtube.com/watch?v=vDjW_dRyKXY)
- Date / venue: 23 Sep 2026, Palmer Events Center, Austin, TX
- Follow-up session: "AI and the future of Ruby & Rails - a chat with Matz & DHH" (24 Sep)

### 7.1 Structure of the talk

```mermaid
flowchart TD
    A["1. The Brownie camera moment<br/>Frontier AI became available to everyone (24 Nov 2025)"] --> B["2. The 1,000x programmer<br/>The 10x debate is over"]
    B --> C["3. Pencils down<br/>37signals stops writing code by hand"]
    C --> D["4. Proof in products<br/>Basecamp 5 / HEY (6 native apps + Rust mail core) / Omarchy"]
    D --> E["5. Where Rails fits in the agent age<br/>Conventions = token efficiency"]
    E --> F["6. Call to action<br/>Give every app a CLI"]
    F --> G["Long live Ruby. Long live Rails."]
```

### 7.2 DHH's own output (as he described it)

```mermaid
xychart-beta
    title "Lines of code written by DHH (as quoted in the keynote)"
    x-axis ["Avg. year before agents", "August 2026 alone (with agents)"]
    y-axis "Lines" 0 --> 160000
    bar [30000, 150000]
```

### 7.3 Key points

1. **The "Brownie camera" moment**
   - DHH named **24 Nov 2025** as the day frontier AI became usable by everyone. He compared it to the Kodak Brownie camera, which turned photography from a specialist job into something anyone could do. Programmers turn from "coders" into **makers**.
2. **From 10x to 1,000x**
   - He said the "10x programmer" debate is over. The gap between the worst programmer **without** agents and the best one **with** agents "approaches **1,000x**".
   - His own numbers: about **150,000 lines in August 2026 alone**, compared to a long-term average of about **30,000 lines a year**.
3. **"Pencils down"**
   - *"It's pencils down, people. Writing code by hand is no longer an economically viable skill for most programmers at most companies."*
   - 37signals no longer writes code by hand. Agent-written code is the default, and people code by hand only to fix what the agents got wrong. DHH said he had "retired from being a professional programmer".
4. **Lessons from 37signals' products**
   - **Basecamp 5**: an early experiment where designers "vibe-coded" with agents left the architecture "like Swiss cheese". Even so, the product shipped successfully with agent speed-ups.
   - **HEY**: it moves from one web app to **six native apps** written by agents. The **mail server core was rewritten in Rust**, which reported a ~99% CPU and ~95% memory reduction (the numbers vary between reports). He said it could in theory run on a Raspberry Pi.
   - **Omarchy** (DHH's Linux distribution): about $20M has been pledged to it. Install time went from 3m33s (Rails World 2025) to 35s, and to 9s in the lab. Agent-built apps such as *Hype* (Markdown slides) ship as binaries of about 0.5 MB.
5. **Why Rails still fits**
   - Convention over Configuration = **token efficiency**. Agents need less context to produce correct code, and that suits the one-person framework.
   - Evil Martians' agent evaluations on Rails already scored about 95% on the first benchmarks, so harder benchmarks are needed.
   - Traditional code abstractions can become a bottleneck when many agents change the same application at once. Architecture needs to be rethought for that.
6. **Call to action: build a CLI for every app**
   - Agents work best through command-line interfaces. His example was HEY's agent-powered conceptual search, which found a 5-year-old email from almost no context.

### 7.4 How it was received

- Critics said that, although the talk was billed as "what's new in Rails, what's coming next", it **barely mentioned Rails**. There were **no new Rails features and no Rails 9**. The Rust rewrite of HEY was read by many as "Rails/Ruby is dead".
- DHH ended with *"Long live Ruby. Long live Rails."* He presents Rails as a productive, convention-heavy layer for small teams working with agents, while hot paths with heavy performance needs (like HEY's mail core) move to Rust.

> Sources: [Rails World 2026 talk page](https://app.railsworld.com/talks/rails-world-2026-opening-keynote), [Dealroom summary](https://dealroom.co/news/talk-vDjW_dRyKXY-pencils-down-dhh-declares-the-end-of-hand-written-code/), [Dark Factory Dev](https://darkfactory.dev/news/2026-09-25-morning/story-1), [Hacker News thread](https://news.ycombinator.com/item?id=49817680). The YouTube transcript itself could not be fetched, so the numbers above come from these secondary reports.

</details>
