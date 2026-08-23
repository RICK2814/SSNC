<div align="center">

<!-- 🌌 Animated Hero -->
<a href="https://github.com/RICK2814/SSNC">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:00C6FF,50:0072FF,100:7F00FF&height=220&section=header&text=SIKSHA%20SAHAYAK&fontSize=52&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Smart%20Digital%20Learning%20%26%20Assessment%20Platform&descAlignY=60&descSize=18" width="100%" alt="Siksha Sahayak animated banner"/>
</a>

<a href="https://github.com/RICK2814/SSNC">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=21&duration=2800&pause=900&color=00C6FF&center=true&vCenter=true&width=850&lines=Learn+%E2%86%92+Practice+%E2%86%92+Assess+%E2%86%92+Improve;Django-powered+educational+management+system;Structured+study+materials+%2B+question+banks+%2B+quizzes;Built+for+students%2C+teachers+and+administrators" alt="Animated typing headline"/>
</a>

<p>
  <img src="https://img.shields.io/badge/Django-5.x-092E20?style=for-the-badge&logo=django&logoColor=white" alt="Django"/>
  <img src="https://img.shields.io/badge/Python-3.x-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python"/>
  <img src="https://img.shields.io/badge/SQLite-Production%20ready%20with%20DB%20adapter-003B57?style=for-the-badge&logo=sqlite&logoColor=white" alt="SQLite"/>
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5"/>
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3"/>
</p>

<p>
  <img src="https://img.shields.io/github/stars/RICK2814/SSNC?style=for-the-badge&logo=github&label=STARS" alt="GitHub stars"/>
  <img src="https://img.shields.io/github/forks/RICK2814/SSNC?style=for-the-badge&logo=github&label=FORKS" alt="GitHub forks"/>
  <img src="https://img.shields.io/github/last-commit/RICK2814/SSNC?style=for-the-badge&label=LAST%20COMMIT" alt="Last commit"/>
  <img src="https://img.shields.io/github/license/RICK2814/SSNC?style=for-the-badge&label=LICENSE" alt="License"/>
</p>

</div>

---

## ⚡ What is Siksha Sahayak?

**Siksha Sahayak** is a Django-based digital learning and assessment platform designed to organize curriculum, study materials, question banks, quizzes, student accounts and assessment workflows in one place.

The project is structured around a simple learning loop:

```text
┌──────────────┐    ┌──────────────┐    ┌──────────────┐    ┌──────────────┐
│   CURRICULUM │ ─▶ │   MATERIALS  │ ─▶ │   PRACTICE   │ ─▶ │  ASSESSMENT  │
│ Subjects     │    │ Chapters     │    │ Question Bank│    │ Quizzes      │
│ Class Levels │    │ Study Notes  │    │ Explanations │    │ Attempts     │
└──────────────┘    └──────────────┘    └──────────────┘    └──────────────┘
          ▲                                                        │
          └────────────────────── RESULTS ◀────────────────────────┘
```

---

## 🧠 Core Modules

| Module | Purpose |
|---|---|
| 👤 **Accounts** | Student profiles, authentication and user management |
| 📚 **Materials** | Subjects, class levels, chapters and study materials |
| ❓ **Assessments** | Question bank, quizzes, practice attempts and quiz attempts |
| 🛡️ **Admin** | Django admin interface for managing academic content |
| 🧪 **Curriculum Seeder** | Automated population of structured academic content |
| 🎯 **Learning Flow** | Study → practice → quiz → review |

---

## 🚀 Advanced Curriculum Engine

The curriculum is designed so content can scale across classes and subjects without manually rebuilding the application structure.

### Content hierarchy

```text
CLASS LEVEL
    │
    ├── SUBJECT
    │      │
    │      ├── CHAPTER / TOPIC
    │      │      │
    │      │      ├── 📖 Advanced Study Material
    │      │      ├── ❓ Question Bank
    │      │      └── 🧠 20-Question Quiz
    │      │
    │      └── ...
    │
    └── ...
```

### Current seeded learning model

- 📘 Structured subjects and class levels
- 📖 Advanced topic-wise study material
- ❓ Important question-bank entries
- 🧠 **20-question quizzes per topic**
- 🎚️ Difficulty levels for questions
- 💡 Answer explanations
- ⏱️ Configurable quiz timing
- 🛠️ Django admin management

---

## 📊 Platform Architecture

```mermaid
flowchart LR
    U[👨‍🎓 Student] --> W[🌐 Django Web App]
    A[🧑‍🏫 Admin] --> W
    W --> AC[👤 Accounts]
    W --> MA[📚 Materials]
    W --> AS[🧠 Assessments]
    AC --> DB[(🗄️ Database)]
    MA --> DB
    AS --> DB
    AS --> R[📈 Results & Attempts]
    MA --> C[🎯 Curriculum Engine]
    C --> Q[❓ Question Bank]
    Q --> Z[📝 Quizzes]
```

---

## ✨ Feature Matrix

<div align="center">

| Feature | Status |
|:---:|:---:|
| 🔐 Authentication & authorization | ✅ |
| 👨‍🎓 Student profiles | ✅ |
| 🏫 Class levels | ✅ |
| 📚 Subjects & chapters | ✅ |
| 📖 Study materials | ✅ |
| ❓ Question bank | ✅ |
| 🧠 Topic quizzes | ✅ |
| 🎯 Practice attempts | ✅ |
| 📊 Quiz attempts / results | ✅ |
| 🛠️ Django admin | ✅ |
| 🌱 Automated curriculum seeding | ✅ |
| 📱 Responsive UI foundation | ✅ |

</div>

---

## 🛠️ Technology Stack

<div align="center">

<img src="https://skillicons.dev/icons?i=python,django,html,css,sqlite,git,github,vscode&perline=8" alt="Technology stack"/>

</div>

---

## 📁 Project Structure

```text
SSNC/
├── accounts/                 # User and student account functionality
├── assessments/             # Questions, quizzes and attempts
├── materials/               # Subjects, chapters and study content
├── siksha_sahayak/           # Django project configuration
├── static/                   # Static assets
├── templates/                # HTML templates
├── CURRICULUM_SETUP.md       # Curriculum setup guide
├── build.sh                 # Deployment/build helper
├── manage.py                 # Django management entry point
├── requirements.txt         # Python dependencies
├── .gitignore
└── README.md
```

---

## ⚙️ Local Setup

### 1. Clone

```bash
git clone https://github.com/RICK2814/SSNC.git
cd SSNC
```

### 2. Create a virtual environment

**Windows PowerShell**

```powershell
py -3.13 -m venv .venv
.venv\Scripts\activate
```

**macOS / Linux**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Apply migrations

```bash
python manage.py migrate
```

### 5. Create the admin account

```bash
python manage.py createsuperuser
```

### 6. Seed the curriculum

```bash
python manage.py seed_curriculum
```

### 7. Run the application

```bash
python manage.py runserver
```

Open:

```text
http://127.0.0.1:8000/
```

Admin:

```text
http://127.0.0.1:8000/admin/
```

---

## 🧪 Curriculum Seeder

The project includes an automated curriculum population command:

```bash
python manage.py seed_curriculum
```

It is intended to generate the structured academic hierarchy, study materials, question-bank content and quizzes used by the application.

> **Tip:** Run the seeder once on a fresh database and verify the generated records in Django Admin before running it again.

---

## 🔐 Production Security Checklist

Before deployment:

- [ ] Set `DEBUG=False`
- [ ] Move `SECRET_KEY` into an environment variable
- [ ] Configure `ALLOWED_HOSTS`
- [ ] Use PostgreSQL or another production database
- [ ] Configure static-file serving
- [ ] Configure media/file storage if required
- [ ] Never commit `.env`, credentials or database secrets
- [ ] Run `python manage.py check --deploy`

Example environment variables:

```env
SECRET_KEY=replace-with-a-secure-production-secret
DEBUG=False
ALLOWED_HOSTS=your-domain.example.com
DATABASE_URL=your-production-database-url
```

---

## ☁️ Deployment

The project can be deployed on platforms that support Django/WGI applications.

Typical production commands:

```bash
pip install -r requirements.txt
python manage.py collectstatic --noinput
python manage.py migrate
gunicorn siksha_sahayak.wsgi:application
```

For Render-style deployment, the build/start configuration can be:

**Build**

```bash
pip install -r requirements.txt && python manage.py collectstatic --noinput && python manage.py migrate
```

**Start**

```bash
gunicorn siksha_sahayak.wsgi:application
```

---

## 🎯 Why this project?

Siksha Sahayak is built around a practical idea: **learning content should lead directly to measurable practice and assessment.** Instead of keeping notes, questions and quizzes disconnected, the platform links them through the same class → subject → topic hierarchy.

```text
                 ┌─────────────────────┐
                 │     LEARN SMART     │
                 └──────────┬──────────┘
                            ▼
                  📖 Study Material
                            │
                            ▼
                     ❓ Practice
                            │
                            ▼
                      🧠 Quiz
                            │
                            ▼
                    📊 Performance
                            │
                            ▼
                    🎯 Improve Skills
                            │
                            └───────────────↺
```

---

## 🌟 Roadmap

- [x] Django academic foundation
- [x] Accounts and student profiles
- [x] Subjects and class levels
- [x] Chapter/topic organization
- [x] Study materials
- [x] Question bank
- [x] Topic quizzes
- [x] Practice and quiz attempts
- [x] Automated curriculum seeding
- [ ] Rich student analytics dashboard
- [ ] Progress visualization
- [ ] Personalized learning recommendations
- [ ] Advanced search and filtering
- [ ] API layer for mobile clients
- [ ] Gamification / badges / streaks

---

## 🤝 Contributing

Contributions are welcome.

```bash
git checkout -b feature/your-feature
git add .
git commit -m "Add your feature"
git push origin feature/your-feature
```

Then open a Pull Request on GitHub.

---

## 📄 License

This project is distributed under the repository's **MIT License**.

---

<div align="center">

### ⚡ Built to make learning more structured, measurable and accessible.

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=18&duration=3200&pause=1000&color=7F00FF&center=true&vCenter=true&width=700&lines=Learn+%7C+Practice+%7C+Assess+%7C+Improve;Siksha+Sahayak+%E2%80%94+Digital+Learning+Platform" alt="Animated footer"/>

<a href="https://github.com/RICK2814/SSNC">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:7F00FF,50:0072FF,100:00C6FF&height=120&section=footer&animation=twinkling" width="100%" alt="Animated footer banner"/>
</a>

</div>
