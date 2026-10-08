# Impact of AI on Product Development

> AI memengaruhi product development bukan hanya pada bagian model, tetapi juga pada cara perusahaan menemukan masalah, merancang fitur, mengumpulkan data, membuat prototype, mengevaluasi produk, melakukan deployment, dan memperbaiki sistem setelah digunakan.

---

# 1. Overview

Pada materi sebelumnya kita telah memahami bahwa AI Engineer bertugas membangun sistem yang menggunakan teknologi AI untuk menyelesaikan masalah nyata.

Sekarang pertanyaannya:

> **Bagaimana AI memengaruhi proses pengembangan sebuah produk?**

Dalam software development tradisional, alurnya dapat digambarkan:

```text
Problem
   ↓
Requirements
   ↓
Design
   ↓
Development
   ↓
Testing
   ↓
Deployment
   ↓
Maintenance
```

Ketika AI menjadi bagian dari produk, proses tersebut menjadi lebih kompleks.

```text
Business Problem
       ↓
User Need
       ↓
AI Feasibility
       ↓
Data
       ↓
AI Approach
       ↓
Prototype
       ↓
Evaluation
       ↓
Application
       ↓
Deployment
       ↓
Monitoring
       ↓
Feedback
       ↓
Improvement
```

AI bukan sekadar sebuah fitur tambahan.

AI dapat memengaruhi:

- Product Strategy
- UX/UI
- Software Architecture
- Data Architecture
- Engineering
- Testing
- Deployment
- Monitoring
- Business Model

Google People + AI Guidebook juga menekankan bahwa pengembangan produk berbasis AI perlu dimulai dari kebutuhan pengguna, kemudian mempertimbangkan data, evaluasi, mental model pengguna, explainability, feedback, control, serta graceful failure. [1]

---

# 2. Traditional Software vs AI-Powered Product

Untuk memahami dampaknya, bandingkan software tradisional dengan AI-powered software.

## Traditional Software

Contoh:

> Aplikasi menghitung total harga belanja.

```text
Input
 ↓
Business Logic
 ↓
Output
```

Misalnya:

```python
total = price * quantity
```

Jika input yang sama diberikan, hasilnya akan sama selama aturan program tidak berubah.

---

## AI-Powered Software

Contoh:

> Aplikasi merekomendasikan produk kepada pengguna.

```text
User Data
     ↓
AI Model
     ↓
Prediction
     ↓
Recommendation
```

Output dapat bergantung pada:

- data pengguna
- model
- training data
- konteks
- konfigurasi
- feedback
- waktu

Karena itu, AI system biasanya lebih bersifat probabilistik dibandingkan program yang sepenuhnya deterministic.

---

# 3. AI Changes the Product Development Process

Software tradisional biasanya memiliki logika yang ditentukan programmer.

```text
Business Rule
      ↓
Code
      ↓
Output
```

AI system:

```text
Data
 ↓
Model
 ↓
Prediction
 ↓
Output
```

Akibatnya, developer tidak hanya memikirkan:

> "Apakah kode saya benar?"

Tetapi juga:

> "Apakah model menghasilkan output yang benar dan berguna?"

Ini menghasilkan kebutuhan tambahan:

```text
Code Testing
      +
Data Testing
      +
Model Evaluation
      +
System Evaluation
```

---

# 4. Start with User Needs

AI product development seharusnya dimulai dari kebutuhan pengguna.

Bukan:

> "Kita punya LLM. Apa yang bisa kita buat?"

Tetapi:

> "Masalah pengguna apa yang dapat diselesaikan dengan lebih baik menggunakan AI?"

Google PAIR merekomendasikan untuk menentukan terlebih dahulu apakah AI benar-benar memberikan nilai pada masalah pengguna. AI cocok untuk beberapa kasus seperti rekomendasi, prediksi, natural-language understanding, dan image recognition, tetapi rule atau heuristic bisa lebih baik ketika predictability dan transparency sangat penting. [2]

---

# 5. AI Does Not Automatically Mean Better Product

Ini adalah konsep penting.

Jangan berpikir:

```text
AI
 ↓
Better Product
```

Hubungan sebenarnya:

```text
User Problem
      ↓
Potential Solution
      ↓
Evaluate AI
      ↓
Does AI add value?
      ↓
Yes / No
```

Contoh:

### Problem

> User ingin mengetahui apakah saldo rekening di bawah batas minimum.

Solusi:

```python
if balance < minimum_balance:
    alert_user()
```

Tidak membutuhkan AI.

---

### Problem

> User ingin mengetahui produk apa yang kemungkinan besar akan dibeli.

Solusi potensial:

```text
Historical User Behavior
        ↓
Recommendation Model
        ↓
Recommended Products
```

AI dapat memberikan nilai.

---

# 6. AI Changes Product Requirements

Pada software tradisional, requirement dapat ditulis:

> "Ketika user melakukan X, sistem harus menghasilkan Y."

Pada AI system, requirement sering lebih probabilistik.

Contoh traditional:

```text
Input:
2 + 2

Expected:
4
```

Contoh AI:

```text
Input:
"Jelaskan produk ini."

Expected:
Jawaban harus relevan,
akurat,
dan mudah dipahami.
```

Tidak selalu ada satu output yang benar secara literal.

Karena itu requirement AI perlu memperhatikan:

- accuracy
- relevance
- safety
- latency
- consistency
- usefulness
- cost

---

# 7. Product Success Metrics Change

Dalam software biasa, metrik bisa berupa:

```text
Page Load Time
Error Rate
Uptime
Conversion Rate
```

Pada AI product, perlu tambahan:

```text
Model Accuracy
Precision
Recall
F1
RMSE
Response Quality
Groundedness
Hallucination
Latency
Token Usage
Cost
```

Misalnya sebuah chatbot memiliki:

```text
99.9% Uptime
```

Tetapi:

```text
30% Answer Incorrect
```

Apakah produknya sukses?

Belum tentu.

Availability yang tinggi tidak menjamin kualitas AI yang tinggi.

---

# 8. AI Introduces Probabilistic Behavior

Software tradisional:

```text
Input A
  ↓
Function
  ↓
Output A
```

AI:

```text
Input
 ↓
Model
 ↓
Output
```

Output model dapat dipengaruhi oleh probabilitas.

Contoh LLM:

```text
Prompt
 ↓
LLM
 ↓
Response
```

Respons dapat berbeda atau memiliki variasi meskipun prompt terlihat sama.

Karena itu testing AI berbeda dari testing software tradisional.

---

# 9. AI Changes UX Design

AI juga mengubah cara user berinteraksi dengan produk.

Traditional UI:

```text
Button
Form
Dropdown
Table
```

AI UI dapat melibatkan:

```text
Chat
Voice
Natural Language
Recommendations
Predictions
Generated Content
```

Contoh:

### Traditional Search

```text
Keyword
 ↓
Search
 ↓
Results
```

### AI Search

```text
Natural Language Question
          ↓
       Retrieval
          ↓
        AI Model
          ↓
       Response
```

---

# 10. Users Need a Correct Mental Model

Pengguna harus memahami apa yang dapat dan tidak dapat dilakukan AI.

Google PAIR menyebut konsep ini sebagai **mental model**.

Mental model adalah pemahaman pengguna tentang bagaimana sebuah sistem bekerja dan bagaimana tindakan mereka memengaruhi sistem tersebut. Ketika pemahaman pengguna tidak sesuai dengan kemampuan nyata sistem, dapat terjadi ekspektasi yang salah, frustrasi, penyalahgunaan, atau pengguna meninggalkan produk. [3]

Contoh buruk:

```text
"AI ini selalu benar."
```

Pengguna dapat terlalu percaya pada AI.

Contoh lebih baik:

```text
"AI-generated answer.
Verify important information."
```

---

# 11. Trust Becomes a Product Concern

AI dapat membuat keputusan atau rekomendasi.

Contoh:

```text
AI:
"Produk ini direkomendasikan kepada Anda."
```

Pengguna mungkin bertanya:

> "Mengapa produk ini direkomendasikan?"

Dalam beberapa kasus, product harus memberikan penjelasan atau konteks.

Contoh:

```text
Recommended because:

- You viewed similar products
- You purchased category X
- Users with similar preferences liked this item
```

Trust menjadi bagian dari product design.

---

# 12. Human-in-the-Loop

Tidak semua keputusan harus sepenuhnya otomatis.

Untuk keputusan yang memiliki risiko tinggi, manusia dapat tetap menjadi bagian dari proses.

```text
AI
 ↓
Recommendation
 ↓
Human Review
 ↓
Final Decision
```

Contoh:

```text
AI
 ↓
Flags suspicious transaction
 ↓
Fraud Analyst
 ↓
Final Decision
```

AI membantu manusia, bukan selalu menggantikannya.

---

# 13. AI Changes Data Requirements

Dalam traditional software:

```text
Database
 ↓
Business Logic
```

Dalam AI product:

```text
Data
 ↓
Model
 ↓
Prediction
```

Data menjadi komponen utama.

Pertanyaan yang harus dijawab:

- Data berasal dari mana?
- Apakah data cukup?
- Apakah data relevan?
- Apakah data memiliki bias?
- Apakah data terbaru?
- Apakah data boleh digunakan?
- Apakah data memiliki label?
- Bagaimana kualitas data?

NIST memasukkan aktivitas desain AI seperti menentukan tujuan sistem, memahami asumsi dan konteks, mengumpulkan dan membersihkan data, serta mendokumentasikan karakteristik dataset sebagai bagian dari lifecycle AI. [4]

---

# 14. Data Quality Affects Product Quality

Prinsip sederhana:

```text
Poor Data
   ↓
Poor Model
   ↓
Poor Prediction
   ↓
Poor Product
```

Contoh:

Jika data training hanya berasal dari satu kelompok pengguna:

```text
Training Data
     ↓
Biased Model
     ↓
Biased Prediction
```

Maka masalah data menjadi masalah produk.

---

# 15. AI Changes Architecture

Traditional application:

```text
Frontend
    ↓
Backend
    ↓
Database
```

AI application:

```text
Frontend
    ↓
Backend
    ↓
AI Service
    ├── Model
    ├── Vector Database
    ├── Prompt
    ├── Tools
    └── External APIs
```

Arsitektur menjadi lebih kompleks.

Contoh RAG:

```text
User
 ↓
Application
 ↓
Retriever
 ↓
Vector Database
 ↓
Relevant Documents
 ↓
LLM
 ↓
Response
```

---

# 16. AI Can Become a New System Layer

AI dapat ditempatkan sebagai service tersendiri.

Contoh:

```text
                         SYSTEM

Frontend
   ↓
Laravel Backend
   ↓
AI Service
   ↓
FastAPI
   ↓
Model / LLM
   ↓
Database
```

Keuntungan:

- AI service dapat dikembangkan secara independen
- Python AI ecosystem mudah digunakan
- deployment dapat dipisahkan
- scaling dapat dilakukan secara terpisah

Ini sangat relevan untuk developer yang sudah memiliki background backend.

---

# 17. AI Changes Prototyping

AI dapat mempercepat proses pembuatan prototype.

Traditional:

```text
Idea
 ↓
Design
 ↓
Backend
 ↓
Frontend
 ↓
Testing
```

Dengan existing AI APIs:

```text
Idea
 ↓
Prompt / API
 ↓
Prototype
 ↓
User Testing
```

Misalnya:

> Membuat chatbot internal.

Tidak harus melatih model sendiri.

Dapat menggunakan:

```text
Existing LLM
     +
Company Documents
     +
RAG
```

Kemudian prototype dapat diuji lebih awal.

---

# 18. Build vs Buy vs Integrate

Ketika membangun AI product, perusahaan perlu memutuskan:

> Apakah harus membuat model sendiri?

Tidak selalu.

Ada beberapa pilihan:

```text
Option 1
Build Model From Scratch

Option 2
Fine-tune Existing Model

Option 3
Use Existing Model

Option 4
Use AI API
```

Pertimbangan:

- budget
- data
- performance
- privacy
- latency
- control
- maintenance
- time-to-market

Contoh:

Jika perusahaan hanya membutuhkan chatbot customer support, melatih LLM dari nol biasanya bukan pilihan pertama.

Alternatif:

```text
Existing LLM
     +
RAG
     +
Company Knowledge
```

---

# 19. Time-to-Market

AI dapat mempercepat beberapa jenis product development.

Contoh:

```text
Traditional Approach

6 Months
    ↓
Production
```

Dengan existing AI capabilities:

```text
Prototype
   ↓
User Test
   ↓
Iteration
   ↓
Production
```

Keuntungan utamanya bukan sekadar coding lebih cepat.

Yang lebih penting:

> **Tim dapat menguji ide lebih cepat.**

---

# 20. AI Changes Experimentation

AI product development sangat bergantung pada eksperimen.

Contoh:

```text
Version A
   ↓
Evaluate
   ↓
Version B
   ↓
Evaluate
   ↓
Version C
   ↓
Evaluate
```

Eksperimen dapat terjadi pada:

- model
- prompt
- retrieval strategy
- chunk size
- embedding model
- temperature
- architecture
- UI
- workflow

Karena itu AI Engineer perlu terbiasa dengan iterative development.

---

# 21. Evaluation Becomes Part of Development

Pada aplikasi tradisional:

```text
Build
 ↓
Test
 ↓
Deploy
```

Pada AI:

```text
Build
 ↓
Evaluate
 ↓
Improve
 ↓
Evaluate
 ↓
Test
 ↓
Deploy
 ↓
Monitor
 ↓
Evaluate Again
```

Evaluasi menjadi proses yang berulang.

---

# 22. Offline vs Online Evaluation

## Offline Evaluation

Dilakukan sebelum model atau feature digunakan secara luas.

Contoh:

```text
Evaluation Dataset
        ↓
AI Model
        ↓
Metrics
```

Contohnya:

```text
Accuracy
RMSE
Precision
Recall
```

Untuk LLM:

```text
Question
Expected Answer
Actual Answer
        ↓
Evaluation
```

---

## Online Evaluation

Dilakukan ketika sistem sudah digunakan.

Contoh:

```text
Real Users
    ↓
Production AI
    ↓
User Feedback
    ↓
Monitoring
    ↓
Evaluation
```

Contoh metrics:

```text
CTR
Conversion
User Rating
Task Success
Latency
Error Rate
```

---

# 23. AI Changes Testing

Traditional software:

```text
Input
 ↓
Function
 ↓
Expected Output
```

AI:

```text
Input
 ↓
AI System
 ↓
Output
 ↓
Evaluation
```

Karena output dapat memiliki variasi, pengujian perlu menggunakan kumpulan kasus dan kriteria evaluasi.

Contoh chatbot:

```text
100 Test Questions
        ↓
LLM
        ↓
Evaluation
        ↓
Quality Score
```

---

# 24. Edge Cases Become More Important

AI system harus diuji terhadap input yang tidak biasa.

Contoh:

```text
Normal Input
↓
Valid

Ambiguous Input
↓
Test

Unexpected Input
↓
Test

Malicious Input
↓
Test
```

Untuk LLM application:

- prompt injection
- irrelevant question
- malformed input
- sensitive data
- adversarial prompt

Untuk ML:

- out-of-distribution data
- missing features
- extreme values
- corrupted data

---

# 25. AI Must Handle Failure Gracefully

AI dapat salah.

Karena itu sistem sebaiknya tidak hanya mendesain:

```text
Success Path
```

tetapi juga:

```text
Failure Path
```

Google PAIR menyarankan desain **graceful failure** untuk membantu pengguna ketika model maupun konteks menghasilkan kesalahan. [1]

Contoh:

### Bad

```text
AI:
I don't know.
```

### Better

```text
AI:
Saya tidak menemukan informasi yang cukup
untuk menjawab pertanyaan ini.

Dokumen yang tersedia tidak membahas topik tersebut.
```

---

# 26. AI Changes Product Feedback

Feedback user menjadi sangat penting.

Traditional:

```text
User
 ↓
Feedback
 ↓
Developer
```

AI:

```text
User
 ↓
AI System
 ↓
Feedback
 ↓
Evaluation
 ↓
Improvement
```

Feedback dapat berupa:

```text
👍 Good Answer
👎 Bad Answer
Report
Correction
Rating
```

Feedback tersebut dapat digunakan untuk:

- menemukan masalah
- memperbaiki prompt
- memperbaiki retrieval
- memperbaiki data
- meningkatkan model
- mengetahui kebutuhan pengguna

---

# 27. AI Product Development is Iterative

AI product jarang selesai dalam satu kali development.

Lebih tepat:

```text
Build
 ↓
Evaluate
 ↓
Deploy
 ↓
Collect Feedback
 ↓
Analyze
 ↓
Improve
 ↓
Repeat
```

Ini disebut iterative development.

---

# 28. AI Changes Monitoring

Traditional application monitoring:

```text
CPU
Memory
Latency
Error Rate
Uptime
```

AI application membutuhkan metrik tambahan.

### Machine Learning

```text
Model Performance
Data Drift
Prediction Distribution
```

### LLM

```text
Token Usage
Latency
Cost
Response Quality
Hallucination
Retrieval Quality
```

Monitoring dibutuhkan karena performa AI di dunia nyata dapat berbeda dari hasil saat development.

NIST menempatkan operation and monitoring sebagai bagian dari lifecycle AI, bukan aktivitas yang hanya dilakukan setelah semua pekerjaan selesai. [5]

---

# 29. AI Can Change the Cost Structure

Traditional application biasanya memiliki biaya:

```text
Server
Database
Storage
Bandwidth
```

AI application dapat menambahkan:

```text
Model Inference
GPU
LLM API
Embedding
Vector Database
Token Usage
```

Contoh LLM:

```text
Users
   ↓
More Requests
   ↓
More Tokens
   ↓
Higher Cost
```

Karena itu AI Engineer harus mempertimbangkan cost sejak tahap desain.

---

# 30. AI + Cost Optimization

Beberapa strategi:

```text
Model Selection
      ↓
Prompt Optimization
      ↓
Caching
      ↓
Smaller Model
      ↓
Reduce Context
      ↓
Reduce Unnecessary Calls
```

Contoh:

Jika pertanyaan sederhana dapat dijawab dengan model kecil:

```text
Simple Question
     ↓
Small Model
```

Tidak selalu perlu model terbesar.

---

# 31. AI Changes Security Requirements

AI product dapat memiliki risiko tambahan.

Contohnya:

- Prompt Injection
- Data Leakage
- Model Abuse
- Sensitive Information Exposure
- Unauthorized Tool Access

Untuk AI Agent, risiko dapat meningkat karena model memiliki kemampuan melakukan tindakan.

Contoh:

```text
LLM
 ↓
Tool
 ↓
Database
```

Jika tidak ada access control yang benar:

```text
Malicious Request
 ↓
Agent
 ↓
Unauthorized Tool
 ↓
Sensitive Data
```

Karena itu AI Engineer harus memahami security.

---

# 32. AI Changes Privacy Requirements

AI product dapat memproses data pengguna dalam jumlah besar.

Contoh:

```text
User Message
CV
Documents
Customer Data
Transaction Data
```

Pertanyaan penting:

- Apakah data boleh dikirim ke external API?
- Apakah data perlu dianonimkan?
- Berapa lama data disimpan?
- Siapa yang dapat mengaksesnya?
- Apakah data digunakan untuk training?
- Bagaimana secret dan credential disimpan?

Privacy harus dipertimbangkan sejak awal.

---

# 33. Responsible AI Becomes a Product Concern

NIST AI RMF menyarankan agar karakteristik trustworthiness dipertimbangkan mulai dari pre-design, design, development, deployment, use, hingga testing dan evaluation. [6]

Beberapa aspek:

```text
Validity
Reliability
Safety
Security
Resilience
Transparency
Explainability
Privacy
Fairness
```

Jadi responsible AI bukan hanya tugas legal atau compliance.

AI Engineer juga perlu memahami implikasi teknisnya.

---

# 34. AI Changes Team Structure

AI product development biasanya melibatkan banyak role.

```text
                 Product Manager
                       │
              ┌────────┴────────┐
              ↓                 ↓
        AI Engineer        UX / UI Designer
              │
      ┌───────┼────────┐
      ↓       ↓        ↓
 Data Scientist  Data Engineer  Software Engineer
              │
              ↓
        DevOps / Platform
```

Tanggung jawab bisa berbeda pada setiap perusahaan.

Dalam startup, satu engineer dapat menangani banyak area.

Dalam perusahaan besar, setiap area dapat menjadi tim sendiri.

---

# 35. Collaboration with Product Manager

Product Manager bertanya:

> "Apa yang ingin kita selesaikan untuk user?"

AI Engineer membantu menjawab:

> "Apakah AI adalah solusi yang masuk akal dan bagaimana cara membangunnya?"

Contoh:

```text
User Problem
     ↓
Product Requirement
     ↓
AI Feasibility
     ↓
Architecture
     ↓
Implementation
```

---

# 36. Collaboration with UX Designer

AI membutuhkan UX yang berbeda dari software biasa.

Designer harus memikirkan:

- bagaimana menunjukkan hasil AI
- bagaimana user melakukan koreksi
- bagaimana menampilkan uncertainty
- bagaimana menjelaskan AI
- bagaimana menangani error
- kapan user tetap perlu mengambil keputusan

Contoh:

```text
AI Recommendation
       ↓
Show Recommendation
       ↓
Explain Why
       ↓
User Accept / Reject
```

---

# 37. Collaboration with Data Scientist

Data Scientist dapat berfokus pada:

```text
Data
 ↓
Analysis
 ↓
Experiment
 ↓
Model
 ↓
Evaluation
```

AI Engineer kemudian dapat menangani:

```text
Model
 ↓
API
 ↓
Application
 ↓
Deployment
 ↓
Monitoring
```

Namun pembagiannya tidak selalu tetap.

---

# 38. AI Engineer and Product Architecture

Ketika AI menjadi bagian utama produk, AI Engineer harus memikirkan architecture.

Contoh aplikasi RAG:

```text
                        USER
                          ↓
                     Frontend
                          ↓
                       Backend
                          ↓
                    AI Orchestrator
                    /             \
                   ↓               ↓
             Retriever           LLM
                   ↓               ↓
             Vector DB        Model Provider
                   ↓               ↓
             Documents        Response
```

AI Engineer harus menentukan:

- di mana model dijalankan
- bagaimana data dikirim
- bagaimana retrieval dilakukan
- bagaimana error ditangani
- bagaimana API berkomunikasi
- bagaimana sistem di-scale

---

# 39. Product Architecture Must Include Failure

Contoh:

```text
User
 ↓
AI Agent
 ↓
External API
```

Bagaimana jika API gagal?

Sistem perlu memiliki:

```text
Timeout
Retry
Fallback
Error Handling
Logging
```

Contoh:

```text
AI Request
     ↓
External API
     ↓
Failure
     ↓
Retry
     ↓
Still Failed
     ↓
Fallback Response
```

AI Engineer harus memikirkan sistem secara menyeluruh.

---

# 40. AI Changes Documentation

AI system juga membutuhkan dokumentasi.

Contoh:

```text
Model Documentation
Prompt Documentation
Data Documentation
API Documentation
Architecture Documentation
Evaluation Documentation
```

Dokumentasi dapat menjelaskan:

- model yang digunakan
- versi model
- sumber data
- batasan model
- evaluation results
- known failure cases
- deployment configuration

---

# 41. AI Changes Versioning

Pada software biasa:

```text
Application v1
Application v2
Application v3
```

Pada AI:

```text
Application v3
   +
Model v5
   +
Prompt v8
   +
Dataset v4
   +
Embedding Model v2
```

Satu perubahan dapat memengaruhi hasil sistem.

Karena itu versioning menjadi lebih penting.

---

# 42. Reproducibility

AI Engineer harus dapat menjawab:

> "Bagaimana kita mendapatkan hasil ini?"

Contohnya:

```text
Code Version
     +
Dataset Version
     +
Model Version
     +
Configuration
     +
Prompt Version
     ↓
Result
```

Jika semua komponen tidak dicatat, akan sulit mereproduksi hasil eksperimen.

---

# 43. AI Changes the Definition of "Done"

Traditional software:

```text
Feature implemented
      ↓
Tests pass
      ↓
Done
```

AI:

```text
Feature implemented
      ↓
Model evaluated
      ↓
Safety checked
      ↓
Performance checked
      ↓
Cost checked
      ↓
User tested
      ↓
Deployment
      ↓
Monitoring
      ↓
Done
```

Bahkan setelah deployment, pekerjaan belum sepenuhnya selesai.

---

# 44. AI Product Lifecycle

Secara keseluruhan:

```text
                  AI PRODUCT LIFECYCLE

                Business / User Need
                         ↓
                  Problem Definition
                         ↓
                    AI Feasibility
                         ↓
                    Data Planning
                         ↓
                   Prototype / MVP
                         ↓
                Model / AI Development
                         ↓
                      Evaluation
                         ↓
                   Product Integration
                         ↓
                       Testing
                         ↓
                     Deployment
                         ↓
                    Monitoring
                         ↓
                  User Feedback
                         ↓
                     Improvement
                         ↓
                       Repeat
```

NIST menggambarkan lifecycle AI secara luas dan menempatkan design, development, deployment, operation/monitoring, serta testing/evaluation sebagai aktivitas yang saling terhubung. [4][5]

---

# 45. Example: AI Customer Support

Misalnya perusahaan ingin membangun AI customer support.

## Traditional Customer Support

```text
Customer
   ↓
Search FAQ
   ↓
Read Answer
```

---

## AI Customer Support

```text
Customer
   ↓
AI Assistant
   ↓
Understand Question
   ↓
Retrieve Information
   ↓
Generate Answer
   ↓
Customer
```

Jika membutuhkan action:

```text
Customer
   ↓
AI Agent
   ↓
Order API
   ↓
Check Order
   ↓
LLM
   ↓
Answer
```

---

# 46. Product Development Responsibilities

Dalam project tersebut:

### Product Manager

```text
Define user problem
Define product goal
```

### UX Designer

```text
Design interaction
Design feedback
Design error states
```

### Data Engineer

```text
Prepare data pipeline
```

### AI Engineer

```text
Build AI system
Integrate model
Build API
Evaluation
Deployment
Monitoring
```

### Software Engineer

```text
Build application
Backend
Database
Integration
```

---

# 47. Example: AI Job Analyzer

Misalkan kita membuat:

> AI Job Analyzer

Tujuan:

> Membantu user menemukan lowongan yang sesuai dengan skill mereka.

Product lifecycle:

```text
User Problem
     ↓
"Which jobs fit my skills?"
     ↓
AI Solution
     ↓
CV Analysis
     ↓
Job Retrieval
     ↓
Skill Matching
     ↓
Recommendation
```

Architecture:

```text
CV
 ↓
PDF Parser
 ↓
LLM
 ↓
Skill Extraction
 ↓
Embedding
 ↓
Vector DB
 ↓
Job Retrieval
 ↓
Matching
 ↓
Recommendation
```

Product considerations:

```text
Accuracy
Privacy
Latency
Cost
Explainability
Security
```

---

# 48. Example: Commodity Prediction Application

Project prediksi harga komoditas juga dapat dilihat sebagai AI product.

```text
                COMMODITY AI SYSTEM

Price Data
     +
Weather Data
     ↓
Data Pipeline
     ↓
Database
     ↓
Preprocessing
     ↓
LSTM / BiLSTM / GRU
     ↓
Evaluation
     ↓
Best Model
     ↓
Inference API
     ↓
Web Application
     ↓
User
```

Product perspective:

```text
User Need:
"Mengetahui perkiraan harga komoditas."

AI:
Predict future price.

Product:
Display prediction
+
Historical data
+
Model performance
+
Supporting information
```

Jadi model hanyalah salah satu komponen produk.

---

# 49. AI Product Trade-offs

AI Engineer sering harus memilih antara beberapa trade-off.

## Accuracy vs Latency

```text
Higher Accuracy
       ↕
Higher Latency
```

## Accuracy vs Cost

```text
Larger Model
       ↓
Potentially Better Quality
       ↓
Higher Cost
```

## Automation vs Control

```text
More Automation
       ↕
Less Human Control
```

## Flexibility vs Predictability

```text
Generative AI
       ↕
Traditional Rules
```

Tidak ada satu solusi yang selalu terbaik.

---

# 50. AI Product Maturity

Sebuah AI product dapat berkembang secara bertahap.

## Level 1 — AI Feature

```text
Existing App
    +
Simple AI Feature
```

Contoh:

> Auto summarization.

---

## Level 2 — AI Application

```text
Application
    +
AI Core
```

Contoh:

> Document assistant.

---

## Level 3 — AI System

```text
Application
    +
LLM
    +
RAG
    +
Tools
    +
Database
    +
Monitoring
```

---

## Level 4 — Agentic System

```text
AI Agent
   ├── Reasoning
   ├── Tools
   ├── Memory / Context
   ├── RAG
   └── External Systems
```

Tingkat kompleksitas meningkat bersama kebutuhan reliability, security, evaluation, dan observability.

---

# 51. What Makes an AI Product Good?

AI product yang baik bukan hanya memiliki model yang pintar.

Produk yang baik harus memenuhi:

```text
Useful
+
Reliable
+
Fast Enough
+
Affordable
+
Safe
+
Understandable
+
Maintainable
```

Dengan kata lain:

> **AI quality ≠ model quality saja.**

Lebih tepat:

```text
AI Product Quality
=
Model Quality
+
Data Quality
+
System Quality
+
UX Quality
+
Operational Quality
```

---

# 52. Important Principle: AI is a Component

Jangan berpikir:

```text
Product = AI Model
```

Lebih tepat:

```text
Product
│
├── User Interface
├── Backend
├── Database
├── Business Logic
├── AI Model
├── Data
├── Infrastructure
└── Monitoring
```

AI merupakan salah satu bagian dari product.

---

# 53. What AI Engineer Should Think About

Ketika diberikan sebuah AI feature, AI Engineer seharusnya bertanya:

### User

```text
Who is the user?
What problem are they solving?
```

### Data

```text
What data do we have?
Is it enough?
Is it reliable?
```

### Model

```text
Which model should we use?
Do we need to train?
Can we use an existing model?
```

### Product

```text
How does the AI fit into the application?
```

### Evaluation

```text
How do we know that the AI works?
```

### Production

```text
How do we deploy it?
How do we monitor it?
```

### Risk

```text
What happens when it is wrong?
```

---

# 54. AI Engineering Mindset

Perubahan mindset yang penting:

### Beginner

> "Model apa yang paling bagus?"

### AI Engineer

> "Solusi apa yang paling tepat untuk masalah ini?"

---

### Beginner

> "Saya harus menggunakan AI."

### AI Engineer

> "Apakah AI memberikan nilai dibandingkan solusi non-AI?"

---

### Beginner

> "Model saya memiliki accuracy tinggi."

### AI Engineer

> "Apakah sistem ini menyelesaikan masalah pengguna dengan baik?"

---

### Beginner

> "Sudah deploy."

### AI Engineer

> "Bagaimana saya mengetahui sistem tetap bekerja dengan baik?"

---

# 55. Key Takeaways

1. AI dapat mengubah seluruh proses product development.

2. AI product development harus dimulai dari **user problem**, bukan dari model yang ingin digunakan.

3. Tidak semua masalah membutuhkan AI.

4. AI membuat data menjadi bagian penting dari product development.

5. AI membuat evaluasi menjadi proses yang lebih kompleks.

6. AI product perlu memperhatikan:

```text
Accuracy
Latency
Cost
Security
Privacy
Reliability
UX
```

7. AI dapat mengubah user interface dan user experience.

8. Pengguna perlu memiliki mental model yang benar terhadap kemampuan dan keterbatasan AI.

9. AI system harus dirancang untuk menangani error dan failure.

10. Monitoring dan feedback merupakan bagian dari product lifecycle.

11. AI Engineer tidak hanya memikirkan model, tetapi juga:

```text
Data
+
Model
+
Software
+
Infrastructure
+
UX
+
Product
```

12. Model yang bagus belum tentu menghasilkan product yang bagus.

13. AI product development bersifat iterative:

```text
Build
 ↓
Evaluate
 ↓
Deploy
 ↓
Monitor
 ↓
Improve
 ↓
Repeat
```

---

# 56. My Understanding

> AI memengaruhi product development karena AI bukan hanya komponen backend, tetapi dapat memengaruhi cara produk dirancang, diuji, digunakan, dan diperbaiki.

> Dalam software tradisional, sebagian besar perilaku sistem ditentukan melalui aturan yang ditulis programmer. Dalam AI system, sebagian perilaku berasal dari pola yang dipelajari model dari data.

> Oleh karena itu, AI Engineer harus memperhatikan bukan hanya kode, tetapi juga data, model, evaluation, UX, deployment, monitoring, security, privacy, dan cost.

> Tidak semua masalah membutuhkan AI. Keputusan menggunakan AI harus didasarkan pada nilai yang diberikan kepada pengguna dan produk.

> Produk AI yang baik bukan hanya produk dengan model paling akurat, tetapi produk yang mampu menyelesaikan masalah pengguna secara reliable, aman, efisien, dan dapat dipelihara.

---

# 57. Questions I Should Be Able to Answer

## Product

1. Bagaimana AI mengubah product development?
2. Mengapa product development harus dimulai dari user problem?
3. Mengapa tidak semua fitur membutuhkan AI?
4. Apa perbedaan AI feature dengan AI product?

## Data

5. Mengapa data menjadi semakin penting dalam AI product?
6. Bagaimana kualitas data memengaruhi kualitas produk?
7. Apa saja risiko data yang perlu diperhatikan?

## UX

8. Apa itu mental model pengguna?
9. Mengapa trust penting dalam AI product?
10. Apa itu human-in-the-loop?
11. Mengapa AI harus memiliki graceful failure?

## Engineering

12. Bagaimana AI memengaruhi system architecture?
13. Mengapa AI model sering dibuat sebagai API/service?
14. Mengapa monitoring penting setelah deployment?
15. Mengapa versioning lebih kompleks pada AI system?

## Business

16. Bagaimana menentukan apakah AI memberikan value?
17. Apa trade-off antara accuracy, latency, dan cost?
18. Mengapa model terbaik belum tentu menjadi solusi terbaik?

## Production

19. Apa perbedaan offline evaluation dan online evaluation?
20. Apa saja yang harus dimonitor pada AI application?
21. Mengapa AI product harus terus dievaluasi setelah deployment?

---

# 58. Mini Exercise

## Exercise 1 — Does AI Add Value?

Problem:

> Sebuah toko ingin memberi peringatan ketika stok barang kurang dari 10.

Pertanyaan:

Apakah membutuhkan AI?

Jawaban:

```text
Tidak.

Rule-based logic sudah cukup.

if stock < 10:
    send_alert()
```

---

## Exercise 2

Problem:

> Sebuah toko ingin memprediksi produk mana yang akan dibeli customer minggu depan.

Kemungkinan solusi:

```text
Historical Purchase
+
Customer Behavior
+
Product Data
      ↓
Machine Learning
      ↓
Prediction
```

AI dapat memberikan value.

---

## Exercise 3

Problem:

> Universitas memiliki 10.000 dokumen dan mahasiswa ingin bertanya menggunakan bahasa natural.

Desain sederhana:

```text
Documents
    ↓
Chunking
    ↓
Embedding
    ↓
Vector Database
    ↓
Retriever
    ↓
LLM
    ↓
Answer
```

Teknologi:

```text
RAG + LLM
```

---

# 59. Practical Exercise

Bayangkan kamu adalah AI Engineer pada sebuah perusahaan.

Perusahaan ingin membuat:

> **AI Customer Support**

Tentukan:

```text
1. User Problem
2. Business Goal
3. Data Required
4. AI Approach
5. Architecture
6. Evaluation Metrics
7. Failure Cases
8. Security Risks
9. Privacy Risks
10. Monitoring Metrics
```

Architecture sederhana:

```text
Customer
   ↓
Chat Interface
   ↓
Backend
   ↓
AI Orchestrator
   ├── LLM
   ├── RAG
   ├── Order API
   └── Product Database
   ↓
Response
```

---

# 60. Real-World Checklist

Ketika membangun AI feature, gunakan checklist berikut:

```text
[ ] Define user problem
[ ] Define business goal
[ ] Determine whether AI adds value
[ ] Identify required data
[ ] Select AI approach
[ ] Build prototype
[ ] Define evaluation metrics
[ ] Test AI behavior
[ ] Design failure handling
[ ] Consider security
[ ] Consider privacy
[ ] Integrate with application
[ ] Deploy
[ ] Monitor
[ ] Collect user feedback
[ ] Improve
```

---

# 61. Connection to Previous Material

Materi sebelumnya:

```text
What is an AI Engineer?
```

Kita belajar bahwa AI Engineer:

```text
Problem
 ↓
AI System
 ↓
Production
```

Materi ini memperluas konsep tersebut:

```text
                  PRODUCT DEVELOPMENT

User Problem
      ↓
Product Requirement
      ↓
AI Feasibility
      ↓
Data
      ↓
AI System
      ↓
Application
      ↓
Evaluation
      ↓
Deployment
      ↓
Monitoring
      ↓
Feedback
      ↓
Improvement
```

Dengan demikian:

> AI Engineer berperan dalam memastikan teknologi AI benar-benar memberikan value di dalam sebuah produk.

---

# 62. Final Mental Model

Saya harus mengingat:

```text
                 AI PRODUCT

              User Problem
                   ↓
             Product Goal
                   ↓
            Does AI Add Value?
                 /     \
               No       Yes
               ↓         ↓
          Non-AI       Data
          Solution       ↓
                     AI System
                         ↓
                      Product
                         ↓
                      Testing
                         ↓
                     Deployment
                         ↓
                     Monitoring
                         ↓
                      Feedback
                         ↓
                    Improvement
                         ↺
```

---

# 63. Next Topic

Materi berikutnya:

**AI Engineer vs ML Engineer**

Pertanyaan utama:

> Apa perbedaan fokus, tanggung jawab, skill, dan workflow antara AI Engineer dan Machine Learning Engineer?

Materi berikutnya akan membantu menentukan posisi mana yang paling sesuai dengan kemampuan dan target karier saya.

---

# Sources

## Primary Source

1. Simply Learn — _How to Become an AI Engineer_
   - YouTube video/transcript yang menjadi sumber awal roadmap.
   - Digunakan sebagai sumber utama struktur pembahasan mengenai AI Engineer dan product development.

## Additional References

2. Google People + AI Research (PAIR) — _People + AI Guidebook_
   - https://pair.withgoogle.com/guidebook-v2/
   - Panduan human-centered design untuk produk yang menggunakan AI.
   - Digunakan untuk user needs, AI value, UX, trust, feedback, control, dan failure handling.

3. Google People + AI Research (PAIR) — _Patterns_
   - https://pair.withgoogle.com/guidebook-v2/patterns
   - Digunakan untuk menentukan kapan AI memberikan value dan kapan pendekatan rule-based lebih sesuai.

4. Google People + AI Research (PAIR) — _Mental Models_
   - https://pair.withgoogle.com/guidebook-v2/chapter/mental-models/
   - Digunakan untuk menjelaskan mental model pengguna, ekspektasi pengguna, dan trust terhadap AI.

5. NIST — _Artificial Intelligence Risk Management Framework (AI RMF)_
   - https://www.nist.gov/itl/ai-risk-management-framework
   - Digunakan untuk lifecycle AI, trustworthy AI, design, development, deployment, use, dan evaluation.

6. NIST — _AI RMF Core_
   - https://airc.nist.gov/airmf-resources/airmf/5-sec-core/
   - Digunakan untuk konsep Govern, Map, Measure, dan Manage serta continuous risk management sepanjang lifecycle AI.

7. NIST — _Appendix A: Descriptions of AI Actor Tasks_
   - https://airc.nist.gov/airmf-resources/airmf/appendices/app-a-descriptions-of-ai-actor-tasks/
   - Digunakan untuk pembahasan mengenai peran product manager, data engineer, AI developer, evaluator, domain expert, dan aktor lain dalam lifecycle AI.

8. NIST — _AI Risk Management Framework FAQs_
   - https://www.nist.gov/itl/ai-risk-management-framework/ai-risk-management-framework-faqs
   - Digunakan untuk konsep trustworthiness dan pertimbangan AI pada tahap pre-design, design, development, deployment, use, testing, dan evaluation.
