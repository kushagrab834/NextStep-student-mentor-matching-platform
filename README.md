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
## 🎓 Year 4: The Endgame Phase
In the final year, the focus shifts from preparation to permanent commitment. Students are locking in their post-graduation lives. The algorithm's matching logic evolves from "Strategy" to **Risk Appetite and Regret Minimization**.

### 1. Dilemma Categories
| Category | Description | Key Focus |
| :--- | :--- | :--- |
| **`ACCEPT_PPO_VS_PLACEMENTS`** | Signing a guaranteed Pre-Placement Offer (PPO) vs. risking it to sit for final placements. | **Risk vs. Reward** |
| **`BUILD_STARTUP_VS_STABILITY`** | Rejecting corporate jobs entirely to pursue a startup venture full-time. | **Entrepreneurial Leap** |
| **`DEFERRED_PLACEMENT_VS_JOINING`** | Using IITB's deferred placement policy to work on a social project/startup for 2 years without losing the campus safety net. | **Time Investment** |
| **`INDIA_VS_ABROAD_HIGHER_ED`** | Preparing for CAT/GATE (staying in India) vs. GRE/GMAT (global MS/PhD). | **Geographic Vision** |

### 2. Year 4 Student Schema: The Final Choice
The Year 4 schema captures "The Hand They Are Dealt." We use the high-stress `ACCEPT_PPO_VS_PLACEMENTS` dilemma as the example here.

```json
{
  "profile": {
    "academic_year": 4,
    "branch": "Your_Branch",
    "cgpa_bracket": "8.5 - 9.0"
  },
  "current_dilemma": {
    "category": "ACCEPT_PPO_VS_PLACEMENTS",
    "context_specifics": {
      "ppo_offer": "SDE at Morgan Stanley",
      "target_placements": "Day 1 Quant/HFT (Jane Street, Tower Research)",
      "deadline_to_accept": "August 15th",
      "current_leaning": "Want to reject PPO, but terrified of going unplaced."
    },
    "psychology": {
      "core_value_driver": "Financial Upside & Prestige",
      "primary_blocker": "Fear of the 'Worst Case Scenario' (Recession market)",
      "risk_tolerance": "Medium-High"
    }

````

---

## 🧠 The Mentor Schema: The "Time Machine"
To make the matching logic work, the Mentor Schema cannot just be a static professional profile. It must act as a "Time Machine." It captures not only where the mentor is *now*, but the specific crossroads they faced at IITB, the choices they made, and how they feel about those choices in hindsight.

Below is a highly detailed, algorithm-ready Mentor Schema designed to perfectly mirror the 4-year student progression. It is populated with a realistic profile of a senior who built an educational startup and completed an international tech internship.

### 1. The Comprehensive Mentor Schema
```json
{
  "mentor_id": "M_042",
  "current_professional_profile": {
    "name": "Aryan",
    "graduation_year": 2024,
    "current_role": "Founder & Technical Lead",
    "company": "EdTech Mentorship Startup / Tokyo AI Labs",
    "location": "Tokyo / Mumbai",
    "industry_keywords": ["EdTech", "Video Analytics", "Machine Learning", "Entrepreneurship", "Mentorship"]
  },
  "campus_legacy": {
    "branch": "Electrical Engineering",
    "cgpa_at_graduation": "8.5 - 9.0",
    "notable_affiliations": ["UGAC Data Analytics Team", "E-Cell"],
    "exploration_stack_year_1": ["WCC", "IITB Racing", "Finance Club"]
  },
  "mentoring_meta": {
    "advice_style": "High-Risk/Ambitious",
    "communication_vibe": "Direct & Tactical",
    "weekly_bandwidth_hours": 3,
    "willing_to_review_resume": true
  },
  "historical_dilemmas": [
    {
      "category": "TECH_DOMAIN_DIVERSION",
      "year_faced": 2,
      "context_specifics": {
        "options_considered": ["Web Development", "Machine Learning / AI"],
        "path_taken": "Machine Learning / AI",
        "primary_reason": "Wanted to build complex systems rather than just interfaces."
      },
      "outcome": "Secured a 3rd-year internship in Tokyo developing video analytic models.",
      "hindsight_sentiment": "Positive"
    },
    {
      "category": "APP_VS_INTERN",
      "year_faced": 3,
      "context_specifics": {
        "research_target": "Applied ML Labs in Japan/US",
        "corporate_fallback": "SDE roles via PT Cell",
        "path_taken": "Committed fully to Apping, skipped Day 1 PT Cell."
      },
      "outcome": "Landed the Tokyo residency.",
      "hindsight_sentiment": "Positive"
    },
    {
      "category": "BUILD_STARTUP_VS_STABILITY",
      "year_faced": 4,
      "context_specifics": {
        "startup_idea_stage": "Bootstrapping an educational mentorship platform",
        "safety_net_offer": "Pre-Placement Offer (PPO) from an MNC",
        "path_taken": "Rejected the PPO to scale the startup."
      },
      "outcome": "Currently operating the startup while acting as a Tech Lead.",
      "hindsight_sentiment": "Mixed (High stress, but high reward)"
    },
    {
      "category": "STEP_DOWN_VS_PUSH_THROUGH",
      "year_faced": 3,
      "context_specifics": {
        "commitments": ["UGAC Tech Hackathons", "Heavy Core Academics", "Intern Prep"],
        "path_taken": "Pushed through burnout without dropping PORs."
      },
      "outcome": "Completed the tenure successfully.",
      "hindsight_sentiment": "Negative (Regrets not stepping down; the resume boost wasn't worth the mental toll)"
    }
  ]
}

````














  }
}

````
