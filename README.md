# NextStep-student-mentor-matching-platform
This project focuses on matching students currently in dilemma regarding their career/academic future decisions with the appropriate mentors who faced similar dilemma during their journey and help the student navigate through their current situation.

We infer the student dilemma mainly based on their year and match with the suitable mentors:

---

## 🧭 Year 1: The Discovery Phase
In the first year, students transition from a single-track focus (JEE) to a multi-track environment. The system's primary goal here is **Interest Alignment** rather than career-mapping.

### 1. Dilemma Categories
| Category | Description | Key Focus |
| :--- | :--- | :--- |
| **`EXPLORATION_DILEMMA`** | For students who are "undecided" and want to sample various domains. | **Discovery Engine** |
| **`TECH_CORE_VS_NON_TECH_POR`** | Choosing between technical depth (Racing/AUV) and campus management (MI/TF). | **Identity Formation** |
| **`NON_TECH_VOLUNTEERING_VS_INTERN`** | Social impact (Enactus/Abhyuday) vs. early-stage corporate exposure. | **Value Alignment** |
| **`STEP_DOWN_VS_PUSH_THROUGH`** | Navigating the "over-commitment" crisis and mental health prioritization. | **Resilience** |
| **`TECH_DOMAIN_DIVERSION`** | Sampling different technical specializations (e.g., Web Dev vs. AI/ML). | **Skill Sampling** |

### 2. Year 1 Student Schema
To handle the ambiguity of a first-year student, the schema utilizes a flexible `context_specifics` block that prioritizes **Keywords** over **Outcomes**.

```json
{
  "profile": {
    "academic_year": 1,
    "branch": "Your_Branch",
    "cgpa_bracket": "N/A"
  },
  "current_dilemma": {
    "category": "EXPLORATION_DILEMMA",
    "context_specifics": {
      "curiosity_tags": ["AI/ML", "Finance", "Consulting", "Robotics"],
      "exploration_stack": ["Finance Club", "IITB Racing"],
      "primary_curiosity": "Is it possible to do both Tech and Finance?",
      "exploratory_objective": "Finding a passion"
    },
    "psychology": {
      "core_value_driver": "Breadth of Knowledge",
      "primary_blocker": "FOMO",
      "risk_tolerance": "Medium"
    }
  }
}

````

## ⚖️ Year 2: The Bifurcation Phase
In the second year, the "Wide-Net" exploration of the first year begins to narrow. Students are forced to choose a "side" to build a competitive resume for the upcoming internship season. The algorithm transitions from matching "vague curiosities" to matching **Strategic Paths** and **Skill Scaling**.

### 1. Dilemma Categories
| Category | Description | Key Focus |
| :--- | :--- | :--- |
| **`TECH_VS_NON_TECH_FORK`** | Choosing between preparing for SDE/Data Science roles vs. Consulting/Finance/PM. | **Preparation Strategy** |
| **`TECH_DOMAIN_DIVERSION`** | Deciding on a technical specialization (e.g., SDE vs. AI/ML). | **Technical Depth** |
| **`INTERN_RESEARCH_VS_FIELD`** | Summer lab intern on campus vs. an off-campus startup internship. | **Environment Choice** |
| **`DOMAIN_ADVANCEMENT_BLOCK`** | Stuck at an intermediate level in a domain (e.g., Web Dev, ML) and unsure how to reach professional/research grade. | **Skill Scaling** |

### 2. Year 2 Student Schema: The Fork & The Block
The Year 2 schema introduces fields to capture the "Fork in the Road" or the "Sunk Cost" of time already invested.

```json
{
  "profile": {
    "academic_year": 2,
    "branch": "Your_Branch",
    "cgpa_bracket": "8.0 - 9.0"
  },
  "current_dilemma": {
    "category": "DOMAIN_ADVANCEMENT_BLOCK",
    "context_specifics": {
      "current_domain": "Machine Learning",
      "time_invested": "18 months",
      "current_milestones": ["Completed 3 Online Courses", "Basic Kaggle participation"],
      "progression_blocker": "Stuck on toy datasets; need research projects."
    },
    "psychology": {
      "core_value_driver": "Mastery & Competence",
      "primary_blocker": "Lack of high-level roadmap",
      "risk_tolerance": "Low"
    }
  }
}

````

## ♟️ Year 3: The High-Stakes Strategy Phase
In the third year, broad exploration ends and execution begins. Students are aggressively preparing for the PT Cell (Placement Team) internship drive or applying to foreign universities ("Apping"). The system transitions from matching "Paths" to matching **Execution Tactics and Risk Hedging**.

### 1. Dilemma Categories
| Category | Description | Key Focus |
| :--- | :--- | :--- |
| **`APP_VS_INTERN`** | Applying for foreign university research ("Apping") vs. sitting for PT Cell corporate internships. | **Career Trajectory** |
| **`PREP_PATH_SELECTION`** | Allocating limited prep time: SDE (LeetCode) vs. Consulting (Case Prep) vs. Quant (Math). | **Resource Allocation** |
| **`PIVOT_INDUSTRY` (Late Phase)** | Realizing late in the degree that the core branch isn't a fit and attempting a rapid pivot. | **Damage Control & Speed** |
| **`MINOR_OR_DOUBLEDOWN`** | Deciding whether to drop a Minor degree to protect CGPA for the upcoming intern season. | **Academic Triage** |

### 2. Year 3 Student Schema: The Execution Plan
The Year 3 schema focuses heavily on the student's *target metrics* and *fallback options*. We use the `APP_VS_INTERN` dilemma here as the primary example.

```json
{
  "profile": {
    "academic_year": 3,
    "branch": "Your_Branch",
    "cgpa_bracket": "8.5 - 9.0"
  },
  "current_dilemma": {
    "category": "APP_VS_INTERN",
    "context_specifics": {
      "research_target": "US/Europe Labs (Robotics)",
      "corporate_fallback": "FMCG Supply Chain roles via PT Cell",
      "current_prep_state": "Emailed 50 professors, 0 positive replies.",
      "leaning_towards": "Apping, but getting anxious about having no backup."
    },
    "psychology": {
      "core_value_driver": "Prestige & Academic Excellence",
      "primary_blocker": "High uncertainty and fear of graduating empty-handed",
      "risk_tolerance": "High"
    }
  }
}
````
