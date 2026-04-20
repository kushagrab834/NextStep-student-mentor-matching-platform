# NextStep-student-mentor-matching-platform
This project focuses on matching students currently in dilemma regarding their career/academic future decisions with the appropriate  mentors who faced similar dilemma during their journey and help the student navigate through their current situation.

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
