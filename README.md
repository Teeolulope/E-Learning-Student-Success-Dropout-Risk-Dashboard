# E-Learning-Student-Success-Dropout-Risk-Dashboard
An interactive Power BI dashboard analysing 5,000 students on an e-learning platform to understand what drives course completion, engagement, and dropout — and to flag at-risk students before they disappear.

📌 **Project Goal**

Design an analytical dashboard for an E-Learning Operations and Student Success team to help them understand the factors that influence learner engagement, course completion, and dropout risk across diverse student populations.

The dashboard is built to be reviewed on a recurring basis to monitor course performance, evaluate digital access barriers, identify at-risk student segments, and assess how subscription type, internet quality, and learning behaviour affect outcomes — ultimately supporting decisions on content design, access equity, and intervention strategy.


🗂️ **Dataset**


5,000 student records across 3 regions (Latin America, South/Southeast Asia, Sub-Saharan Africa)
Fields include demographics, device & internet type, subscription tier, login frequency, video watch time, quiz performance, completion rate, course category, and dropout status

<img width="1888" height="917" alt="Screenshot 2026-06-19 102309" src="https://github.com/user-attachments/assets/cf95f0e9-87ad-4a3e-9625-535f3941b165" />

📊 Dashboard Pages

**1.** **Course Performance**

Answers: which courses are working, and which aren't?


Which courses have the highest completion? — ranked bar chart by completion rate
Do better courses lose fewer students? — combo chart comparing dropout rate against the category average
Does poor internet hurt course completion? — heatmap of completion rate by course category × internet type
Do completers score higher? — scatter plot of completion rate vs average quiz score


Key finding: Programming and Data Analytics lead on both completion (66% and 64%) and quiz scores, while Vocational and Healthcare consistently underperform on both (40% and 42% completion). Poor internet cuts completion by 15–20 percentage points across every course category regardless of subject.

<img width="1165" height="655" alt="Screenshot 2026-06-19 101447" src="https://github.com/user-attachments/assets/1a698282-0431-449b-8b66-100b8717c77c" />


**2. Engagement & Dropout Behaviour**

Answers: how does student behaviour predict dropout?


Does poor internet worsen low login risk? — clustered bar of dropout rate by login frequency, split by internet type
How fast does inactivity lead to dropout? — line chart of dropout rate by days since last active
Which login and watch time combo is riskiest? — heatmap cross-referencing login frequency and watch time buckets
Does higher engagement lead to better scores? — scatter plot of engagement score vs average quiz score by engagement level


**Key finding:** Students logging in fewer than 10 days a month drop out at nearly 40%. Login frequency matters more than total watch time — students who log in often but watch in short sessions (21.7% dropout) outperform infrequent "binge" viewers who watch a lot in rare sessions (31–35% dropout). Consistency of habit beats volume of content consumed. Inactivity beyond 30 days is a strong early warning signal for intervention.


**3. Dropout Risk & Access Barriers**

Answers: who is at risk right now, and why?


How many students are at risk right now? — risk segmentation table (High / Medium / Low) with count, dropout rate, and average score per segment
Where is dropout risk highest? — heatmap of dropout rate by region × internet type
Which internet type has the most dropouts? — bar chart by internet type
Do struggling students drop out more on poor internet? — clustered bar comparing dropout rate for above-average vs below-average completers, split by internet type


**Key finding:** Intermittent internet users drop out at 33% — 65% higher than WiFi users (20%). South/Southeast Asia combined with poor internet is the highest-risk segment in the dataset (35.19%). 347 students are currently flagged as High Risk, with a 34.87% dropout rate and an average score of just 43 — more than double the dropout rate of Low Risk students (15.16%).

<img width="1161" height="655" alt="Screenshot 2026-06-19 101507" src="https://github.com/user-attachments/assets/ac316b6a-1216-4ce9-8f8d-d8fb28eb1232" />



🎯 **Core Insights Across the Dashboard**

**Internet quality is the single strongest predictor of dropout** — stronger than region, subscription type, or device. The gap between WiFi and intermittent/poor internet users is consistently the largest gap in every analysis.

**Login frequency beats total engagement volume.** A student who shows up regularly, even briefly, is less likely to drop out than one who engages in long, infrequent sessions.

**Subscription type and device type have measurable but comparatively weak impact** on dropout (4–5 percentage point gaps) compared to internet quality (12.8 point gap) — explored but intentionally not over-emphasised in the dashboard since the data doesn't support it as a major lever.

**Course design matters.** Vocational and Healthcare courses underperform across every metric regardless of student access conditions, suggesting a content/format issue independent of infrastructure.

**347 students are currently identifiable as high-risk** using a simple behavioural rule (low login frequency + low watch time), giving the Student Success team a concrete, actionable list rather than a vague risk category.



✅ **Recommendations**

Based on the patterns surfaced across all three pages, the following actions would have the most impact on improving completion and reducing dropout:


**Prioritise connectivity-friendly content delivery.** Since internet quality is the strongest predictor of dropout, offering lightweight/offline video formats or downloadable content packs for students on intermittent or mobile-data connections could meaningfully reduce dropout in the highest-risk segment (South/Southeast Asia + poor internet, 35.19%).

**Shift engagement campaigns from "watch more" to "log in more."** The data shows consistency of login beats volume of content watched. Push notifications or reminder nudges timed around the 14–day inactivity mark (before the 30-day danger zone) would intervene earlier than current patterns suggest students typically receive outreach.

**Redesign or restructure Vocational and Healthcare courses.** These categories underperform across completion, quiz score, and dropout regardless of student access conditions — pointing to a content or format issue rather than an infrastructure one. A review of pacing, video length, and assessment design in these categories is recommended.

**Use the High Risk segment (347 students) as an active outreach list, not just a reporting metric.** With an average score of 43 and 34.87% dropout, this group is identifiable today and small enough for targeted, personal intervention rather than blanket messaging.

**Deprioritise subscription tier and device type as intervention levers.** Both show real but comparatively small effects on dropout (4–5 percentage points) next to internet quality (12.8 points) — limited budget for student success initiatives is better spent on connectivity and engagement habit-building than on subscription upgrades or device giveaways.



🛠️ **Tools Used**


Power BI Desktop — dashboard build, DAX measures, Power Query transformations
DAX — custom measures (Dropout Rate, Risk Segments, Login/Watch Time Buckets, category rankings)
Power Query (M) — data cleaning, bucketing, and conditional column creation
