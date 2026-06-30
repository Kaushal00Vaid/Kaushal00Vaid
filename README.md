<h1 align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&pause=1000&color=6366F1&center=true&vCenter=true&width=700&lines=Hi+%2C+I'm+Kaushal+Vaid;BS+Data+Science;AI+%7C+Development+%7C+Finance;Teaching+Assistant+%7C+Developer" alt="Typing SVG" />
</h1>

<p align="center">
  <i>AI Engineer • Data Science Student @ IIT Madras</i>
</p>

---

### About me
- Building ML/DL systems end-to-end — from architecture selection to diagnosing why training collapses (see CeleGAN: four GAN variants, including a documented `loss_D` collapse fix in SRGAN)
- BS Data Science student at IIT Madras, third year
- **Teaching Assistant** for Statistics and Java — hundreds of students
- Full-stack engineer (Node.js, Next.js, PostgreSQL) — background used to ship ML work as deployed products, not just notebooks

**ML/DL Learning Log:** https://kaushal-ml-journey.vercel.app
<sub>(Continuously updated — learning, experimenting, and refining as I go)</sub>

---

### 🌐 Connect with me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge\&logo=linkedin\&logoColor=white)](https://linkedin.com/in/kaushal-vaid)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge\&logo=github\&logoColor=white)](https://github.com/Kaushal00Vaid)
[![Medium](https://img.shields.io/badge/Medium-12100E?style=for-the-badge\&logo=medium\&logoColor=white)](https://medium.com/@kaushalvaid)
[![X](https://img.shields.io/badge/X-000000?style=for-the-badge\&logo=x\&logoColor=white)](https://x.com/kaushal_vaid)
[![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge\&logo=kaggle\&logoColor=white)](https://www.kaggle.com/kaushalvaid)
[![Email](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge\&logo=gmail\&logoColor=white)](mailto:kaushalvaid123@gmail.com)


---

## 🧠 Tech Stack

### Languages

<p>
<img src="https://skillicons.dev/icons?i=python,ts,java" />
</p>

### Machine Learning & Deep Learning

<p>
<img src="https://skillicons.dev/icons?i=sklearn,pytorch" />
</p>

### Backend & Systems

<p>
<img src="https://skillicons.dev/icons?i=nodejs,express,fastapi,flask" />
</p>

### Databases & Caching

<p>
<img src="https://skillicons.dev/icons?i=postgres,mongodb,redis,sqlite" />
</p>

### DevOps & Tooling

<p>
<img src="https://skillicons.dev/icons?i=git,docker,vercel" />
</p>


---

### Featured Projects
**CeleGAN — Progressive GAN Implementation Suite**  [Github Repository](https://github.com/Kaushal00Vaid/celeGAN)
*Four GAN architectures built progressively on CelebA — VanillaGAN → DCGAN → cGAN → SRGAN — each isolating one architectural variable to diagnose its specific failure mode.*
- Diagnosed and partially resolved discriminator dominance in DCGAN/cGAN via label smoothing and update-rate tuning
- Identified root cause of SRGAN's `loss_D` collapse (BCE+Sigmoid gradient saturation) — applied partial mitigations, documented the correct fix (WGAN-GP) not yet implemented
- **Stack:** PyTorch, CelebA, Kaggle T4×2 GPUs

**Comment Category Prediction**  [Github Repository](https://github.com/Kaushal00Vaid/Comment_Category_Prediction)
*Ranked 54/2744 (top 1.97%) classifying online comments into 4 categories from a mix of raw text, engagement metadata, and 73%+ missing demographic data, under scikit-learn-only constraints.*
- Built a 60/40 soft-vote ensemble of Logistic Regression (sparse TF-IDF, high-dimensional linear signal) and LightGBM (non-linear feature interactions) — a deliberate bias-variance trade-off rather than a single-model approach
- EDA directly drove feature engineering: correlation heatmaps surfaced `if_2 == 10` as a strong predictor before any model was trained; word clouds informed hand-built identity/threat/political lexicons
- Abandoned LinearSVC (capped ~0.72 Macro F1, no improvement path) and HistGradientBoosting (marginal gain, zeroed out of final ensemble) after testing — kept only what measurably helped
- **Stack:** scikit-learn, LightGBM, TF-IDF (word + char n-grams), SVD

**Messy Audio Genre Classification**  [Github Repository](https://github.com/Kaushal00Vaid/Messy-Audio-Genre-Classification)
*Multi-stem music genre classification under deliberately degraded test conditions — cross-mixed stems, tempo shifts, heavy environmental noise — to bridge the domain gap between clean training data and real-world audio.*
- V1's naive augmentation (50% stem-summing, single noise clip) collapsed to ~0.10 F1 — rebuilt the entire pipeline around 100% cross-stem mixing, per-stem tempo augmentation, and 0–15 dB layered noise injection
- Best result: EfficientNet-B3 fine-tuned, 0.80933 macro F1, beating a from-scratch CNN, ResNet50, and ResNet18 baselines
- **Stack:** PyTorch, torchaudio, librosa, EfficientNet, MixUp, 5-crop TTA

**Olist Brazilian E-Commerce Analysis**  [Live Dashboard](https://olist-analysis-kaushal00vaid.streamlit.app/) | [Github Repository](https://github.com/Kaushal00Vaid/OLIST-Brazilian-Ecommerce-Analysis)
*SQL-first analysis of 100k+ orders identifying the exact delay threshold (4–7 days) where customer tolerance collapses, confirmed independently by review scores and Portuguese-language NLP sentiment.*
- Replaced VADER (97% neutral on Portuguese — invalid signal) with a custom keyword lexicon; replaced NTILE seller ranking with absolute thresholds once score compression made quartiles meaningless
- RFM segmentation (K-Means) deliberately dropped the frequency dimension after cohort analysis showed 96.1% of customers are single-purchase
- **Stack:** PostgreSQL, pandas, scikit-learn, Streamlit, Plotly

**Nodeflow - Full-Stack Workflow Automation Platform** [Deployed Link](https://nodeflow-gold.vercel.app) | 
[Github Repository](https://github.com/Kaushal00Vaid/nodeflow) \
*An open-source N8N/Zapier alternative focused on type-safe, distributed automation.*
- **Custom DAG Engine**: Architected a topological sorting engine integrated with Inngest to manage reliable, level-based FIFO execution queues.
- **Dynamic State Management**: Engineered a real-time data interpolation system, allowing downstream nodes to dynamically parse and reference variables from previous steps.
- **Type-Safe Integrations**: Built robust API integrations for OpenAI, Gemini, Stripe, Discord, and Slack using tRPC and Zod.
- **Stack**: Next.js, tRPC, PostgreSQL, Prisma, Inngest, Vercel AI SDK, Better Auth.


**Gradely — Quiz Practice Platform**    [Github Repository](https://github.com/Kaushal00Vaid/QuizMaster-V2)   \
Flask-based system with Redis caching, Celery background jobs, rate limiting, and role-based access.

**URL Shortener + Discord Bot**  [Github Repository](https://github.com/Kaushal00Vaid/URL-Shortener-Discord-Bot)  \
Discord bot for URL shortening and debugging errors inside servers.

---

### GitHub Stats

<div align="center">
<br/>
<img src="https://github-readme-stats-sigma-five.vercel.app/api?username=Kaushal00Vaid&show_icons=true&theme=github_dark&hide_border=true&title_color=F7EE00&icon_color=6e7681&text_color=8b949e&bg_color=0d1117&rank_icon=github&card_width=420&border_radius=6" height="155"/>
<img src="https://github-readme-stats-sigma-five.vercel.app/api/top-langs/?username=Kaushal00Vaid&layout=compact&theme=github_dark&hide_border=true&title_color=F7EE00&text_color=8b949e&bg_color=0d1117&langs_count=6&card_width=280&border_radius=6" height="155"/>
<br/><br/>
<img src="https://github-readme-activity-graph.vercel.app/graph?username=Kaushal00Vaid&bg_color=0d1117&color=F7EE00&line=F7EE00&point=ffffff&area=true&area_color=1c1a10&hide_border=true&radius=6&custom_title=activity" />
<br/>

---

<p align="center">
  <i>Stay Hungry, Stay Foolish.</i>
</p>
