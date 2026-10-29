# Speech Script — Risk, Budget & Frontend Design (A10: Local Food Rescue & Redistribution Platform)
### Target length: ~10 minutes · English level: simple / high-school · Format: English then Chinese
### Matches the 12-slide deck (frontend section added, Risk/Budget sections trimmed to make room)

---

## 1. Title (0:00–0:15)

**EN:** Good morning everyone. Today I will talk about three things: risk management, budget planning, and frontend design, for our project — the Local Food Rescue and Redistribution Platform, project A10. We are building this for the South Australian Food Rescue Network.

**CN:** 大家早上好。今天我要讲三部分内容:风险管理、预算规划,还有前端设计——都是我们项目的内容,本地食物救援与再分配平台,项目编号 A10。我们是为南澳食物救援网络做这个项目的。

---

## 2. Agenda (0:15–0:35)

**EN:** Here is my plan. First, the project. Second, our risk framework and matrix. Third, our priority risks. Fourth, our frontend design, built with Vue. Fifth, our budget plan. And finally, a short reflection. This will take about ten minutes.

**CN:** 这是我的安排:第一,项目介绍;第二,风险框架和风险矩阵;第三,优先级风险;第四,我们用 Vue 做的前端设计;第五,预算计划;最后,简单的反思总结。大概十分钟。

---

## 3. Project Context (0:35–1:30)

**EN:** Let me explain the problem first. Supermarkets, cafés, farms, and community events often have extra food. They want to donate it. But right now, donors and charities only use phone calls or text messages. This is slow, and food often goes bad before anyone collects it.

Our platform solves this. Donors post food online. Charities reserve it. The system tracks food type, quantity, expiry date, and pickup time. It also sends notifications and keeps records for safety and reporting.

Our host organisation is the South Australian Food Rescue Network. Our team has five members: full-stack, backend, frontend, database, and QA/security.

**CN:** 我先说说这个问题。超市、咖啡店、农场和社区活动经常有多余的食物,他们想捐出去。但现在,捐赠者和慈善机构只能靠打电话或发消息,这个方式很慢,食物经常还没被取走就过期了。

我们的平台可以解决这个问题。捐赠者在线发布食物信息,慈善机构预订它。系统会记录食物种类、数量、过期时间和取货时间,还会发送通知,并保存记录用于安全和报告。

我们的合作机构是南澳食物救援网络。我们团队有五个人:全栈、后端、前端、数据库和质量/安全测试。

---

## 4. Risk Framework & Matrix (1:30–2:30)

**EN:** Now let's talk about risk. A risk is anything uncertain that could hurt our timeline, budget, quality, or success. We use four categories: team risks, technical risks, product risks, and legal risks.

We give the **most weight** to team risks, not just project risks — because the team is the part we can control fastest. This was not just theory. We really did lose a team member during this project, and because we already planned for this kind of risk, we reorganised our roles and recovered in just a few days.

For the matrix: most examples only have three levels — low, medium, high. I built a full five-by-five matrix myself, and placed all nine of our real risks directly on it, from green to red.

**CN:** 现在来说说风险。风险是指任何可能影响我们进度、预算、质量或项目成功的不确定事件。我们分成四类:团队风险、技术风险、产品风险和法律风险。

我们把**最大的权重**放在团队风险上,而不只是项目风险,因为团队是我们能最快控制的部分。这不只是理论——我们真的在项目中经历了一个成员的离开,正因为提前规划了这种风险,我们才能在几天内重新分配角色并恢复正常。

关于矩阵:大多数例子只有三个等级——低、中、高。我自己做了一个完整的 5×5 矩阵,把我们真实的九个风险都标了进去,颜色从绿到红。

---

## 5. Priority Risks (2:30–3:35)

**EN:** Let's look at our two most important risks. R01 is team member attrition. Probability is 1.0 — it already happened. The impact is about 45 hours of extra work. Our fix: we reorganised the remaining five roles, and we now hold weekly meetings to check our progress.

R03 is about our API. When team members work on different parts of the system, their code can become out of sync. Our fix: we design the API contract first, using OpenAPI and Swagger, and we check it together every week — before writing any code.

The other seven risks — like scope creep, booking conflicts, and data privacy — each also has a clear, specific action, not just a general idea.

**CN:** 我们来看两个最重要的风险。R01 是团队成员流失,概率是 1.0——因为它已经发生了,影响大约是 45 小时的额外工作量。我们的解决办法是:重新分配剩下五个人的角色,现在每周开会检查进度。

R03 是关于我们的 API。当团队成员开发系统不同部分时,代码可能会不同步。我们的解决办法是:先设计好 API 契约,用 OpenAPI 和 Swagger,并且每周一起检查——在写代码之前。

另外七个风险——比如范围蔓延、预订冲突和数据隐私——每一个也都有具体的应对措施,而不只是笼统的想法。

---

## 6. Frontend Design — Tech Stack (3:35–4:45)

**EN:** Now, my part — frontend design. I am building this with **Vue 3**, using the Composition API. For tools, we use **Vite** to build fast, **Pinia** to manage data like donation status, and **Vue Router** to move between pages.

For style, we use **Tailwind CSS** — this makes every screen responsive by default, which means it works well on both phone and computer. For talking to the backend, we use **Axios**, and it follows the same API contract our backend team writes. This means the frontend and backend can never become out of sync — this connects directly back to risk R03.

We also use **Vitest** to test our components, and a chart tool called **vue-chartjs** for the admin reports.

**CN:** 现在是我负责的部分——前端设计。我打算用 **Vue 3**,并使用 Composition API。工具方面,我们用 **Vite** 来快速构建项目,用 **Pinia** 来管理数据(比如捐赠状态),用 **Vue Router** 来实现页面跳转。

样式方面,我们用 **Tailwind CSS**——这让每个页面默认都是响应式的,也就是说在手机和电脑上都能正常显示。和后端通信方面,我们用 **Axios**,并且遵循后端团队写的同一份 API 契约。这意味着前端和后端永远不会不同步——这正好呼应了我们之前说的 R03 风险。

我们还用 **Vitest** 来测试组件,用一个叫 **vue-chartjs** 的图表工具来做管理员报表。

---

## 7. Frontend Design — UX Flow & Key Screens (4:45–5:55)

**EN:** Let me show you the user experience. To post food, a donor uses a simple **three-step form**: Step 1 is food details — category, quantity, and storage information. Step 2 is expiry date and pickup time. Step 3 is review and publish. We kept it short on purpose, because a long form stops people from using the app — this is exactly the risk we called R07.

Beyond that, we are building four key screens: a **donor dashboard** to track listings, a **browse and reserve** screen for charities, an **admin reporting** screen with charts, and a **notifications feed** for real-time updates.

Every screen is designed **mobile-first**. This means we design for the phone screen first, then make it bigger for tablet and computer — because most donors will use their phone.

**CN:** 我来给大家展示一下用户体验。要发布食物,捐赠者只需要填一个简单的**三步表单**:第一步是食物详情——类别、数量和储存信息;第二步是过期时间和取货时间;第三步是确认并发布。我们特意把它设计得很简短,因为太长的表单会让人不想用这个应用——这正好对应了我们之前说的 R07 风险。

除此之外,我们还会做四个关键页面:**捐赠者仪表盘**用来追踪发布记录,**浏览和预订**页面给慈善机构用,**管理员报表**页面带图表,还有**通知栏**用于实时更新。

每个页面都采用**移动优先**的设计方式,也就是说我们先为手机屏幕设计,再放大适配平板和电脑——因为大多数捐赠者会用手机操作。

---

## 8. Budget — Team, Rates & Infrastructure (5:55–7:10)

**EN:** Now, the budget. These hourly rates are not random — they come from real Australian market salary data. Full-stack developers cost $55 an hour, because they do the most complex work. QA and security engineers cost $42 an hour.

Notice that I did not give one single total price. This is on purpose — I give a rate for each role, and the client can choose how many hours they need. This is closer to how real projects work.

We also planned real costs for tools: cloud hosting is $30 a month, our database is $20 a month, and our tools like GitHub and Figma are free. We also added a 10% contingency reserve, just in case.

**CN:** 接下来是预算。这些小时费率不是随便定的,而是基于真实的澳大利亚市场薪资数据。全栈开发者的费率是每小时 55 澳元,因为他们要做最复杂的工作;QA 和安全工程师的费率是每小时 42 澳元。

大家会注意到,我没有给出一个总价。这是我特意这样做的——我给出每个角色的费率,让客户自己决定需要多少工时,这更接近真实项目的做法。

我们也规划了真实的工具费用:云主机每月 30 澳元,数据库每月 20 澳元,像 GitHub 和 Figma 这样的工具是免费的。我们还额外加了 10% 的应急预算,以防万一。

---

## 9. My Role & Reflection (7:10–8:10)

**EN:** So, across risk, budget, and frontend design, my job was to make uncertain things clear and concrete. I built the risk framework, designed the risk matrix from scratch, researched every budget number, and chose our Vue tech stack and screen designs.

What did I learn? First, finding a risk is only the first step — you must keep watching it, because it can become real at any time, just like R01 did. Second, good design is also a way to manage risk — our mobile-first design is really the solution for R07. Design and risk management are not two separate things — they work together.

**CN:** 所以,不管是风险、预算还是前端设计,我的工作都是把不确定的东西变得清晰、具体。我搭建了风险框架,从零设计了风险矩阵,研究了每一个预算数字,还选定了我们的 Vue 技术栈和页面设计。

我学到了什么?第一,发现风险只是第一步,还需要持续关注它,因为它随时可能变成现实,就像 R01 一样。第二,好的设计本身也是一种风险管理方式——我们的移动优先设计其实就是 R07 的解决方案。设计和风险管理不是两件分开的事,它们是配合在一起的。

---

## 10. Thank You / Q&A (8:10–8:30)

**EN:** Thank you very much for listening. I am happy to answer any questions — about our risks, our budget, or the frontend design.

**CN:** 非常感谢大家的聆听。我很乐意回答任何问题——关于我们的风险、预算,或者前端设计。

---

### Timing note / 时间说明
The script above is written to fill about 10 minutes at a natural pace (roughly 120–130 English words per minute). If you find yourself running short, slow down on sections 6–7 (Frontend Design) and add a sentence or two about *why* you personally chose Vue — that's a great, easy place to sound confident and prepared for questions.

上面的稿子按照每分钟 120-130 个英文单词的正常语速设计,大约刚好 10 分钟。如果你发现讲得比较快、时间有富余,可以在第 6-7 部分(前端设计)多讲一两句"为什么我个人选择用 Vue"——这是一个很好的展示自信、也方便应对提问的地方。

### Practice tips / 练习小贴士
- Read the English section out loud 2–3 times before checking the Chinese — this builds fluency instead of translation-in-your-head.
- 建议先大声朗读英文部分 2-3 遍,再看中文核对意思,这样更容易建立英语语感,而不是在脑子里做翻译。
- The bolded tech names (Vue 3, Vite, Pinia, etc.) are the words most likely to trip up pronunciation — practice saying them out loud a few extra times on their own.
- 加粗的技术名词(Vue 3、Vite、Pinia 等)是最容易读错的地方,建议单独多练习几遍发音。
