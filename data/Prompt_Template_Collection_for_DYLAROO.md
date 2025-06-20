# The DYLAROO Prompt Template Collection

## Introduction

This collection provides a comprehensive set of over 50 practical and reusable prompt templates for a wide range of tasks, from software development to creative songwriting. Each template is designed to be easily customized and adapted to your specific needs.

The templates are organized into the following categories:
1.  [Development Templates](#1-development-templates)
2.  [Songwriting Templates](#2-songwriting-templates)
3.  [Creative Writing Templates](#3-creative-writing-templates)
4.  [Business/Project Templates](#4-businessproject-templates)
5.  [Learning and Analysis Templates](#5-learning-and-analysis-templates)
6.  [Meta-Prompts](#6-meta-prompts)

## 1. Development Templates

### 1.1 Code Generation

---

#### **Template 1: Generate a Function from a Description**

**Purpose:** To generate a complete function in a specified language based on a detailed description.

**Template:**
```
Act as an expert [LANGUAGE] developer.
Your task is to create a function that performs the following action: [DETAILED_DESCRIPTION_OF_FUNCTION].

**Function Name:** `[FUNCTION_NAME]`
**Parameters:**
*   `[PARAM_1_NAME]`: ([PARAM_1_TYPE]) - [PARAM_1_DESCRIPTION]
*   `[PARAM_2_NAME]`: ([PARAM_2_TYPE]) - [PARAM_2_DESCRIPTION]
**Return Value:** ([RETURN_TYPE]) - [RETURN_VALUE_DESCRIPTION]

**Constraints & Edge Cases:**
*   [CONSTRAINT_1]
*   [CONSTRAINT_2]
*   Handle the case where [EDGE_CASE_DESCRIPTION].

Please provide the complete function code, including type hints and a brief explanation of the implementation.
```

**Usage Instructions:**
Fill in the `[VARIABLES]` with the specifics of your function requirements. Be as detailed as possible in the description.

**Example:**
```
Act as an expert Python developer.
Your task is to create a function that performs the following action: Calculates the factorial of a non-negative integer.

**Function Name:** `calculate_factorial`
**Parameters:**
*   `n`: (int) - The non-negative integer for which to calculate the factorial.
**Return Value:** (int) - The factorial of the input integer `n`.

**Constraints & Edge Cases:**
*   The input `n` will always be a non-negative integer.
*   The factorial of 0 is 1.
*   Handle the case where the input is greater than 20 (return an error or handle large numbers).

Please provide the complete function code, including type hints and a brief explanation of the implementation.
```

**Expected Output:**
A complete Python function for `calculate_factorial`, including error handling for large numbers and a clear explanation of the code.

**Customization Tips:**
*   For more complex functions, add a "Logic" section detailing the step-by-step process.
*   You can specify a particular coding style or library to use.

---

#### **Template 2: Code Optimization and Refactoring**

**Purpose:** To optimize existing code for better performance, readability, or maintainability.

**Template:**
```
I need you to act as a senior [LANGUAGE] developer and code optimizer.

**Current Code:**
```[LANGUAGE]
[PASTE_EXISTING_CODE_HERE]
```

**Optimization Goals:**
- [GOAL_1] (e.g., improve performance, reduce memory usage, enhance readability)
- [GOAL_2] (e.g., follow best practices, add error handling)
- [GOAL_3] (e.g., make code more modular, add type hints)

**Constraints:**
- Maintain the same functionality
- [ADDITIONAL_CONSTRAINT_1]
- [ADDITIONAL_CONSTRAINT_2]

Please provide:
1. The optimized code with clear comments explaining changes
2. A summary of improvements made
3. Performance impact estimation (if applicable)
4. Any trade-offs or considerations
```

**Example:**
```
I need you to act as a senior Python developer and code optimizer.

**Current Code:**
```python
def find_duplicates(lst):
    duplicates = []
    for i in range(len(lst)):
        for j in range(i+1, len(lst)):
            if lst[i] == lst[j] and lst[i] not in duplicates:
                duplicates.append(lst[i])
    return duplicates
```

**Optimization Goals:**
- Improve time complexity from O(n²) to O(n)
- Add type hints for better code documentation
- Make the function more pythonic

**Constraints:**
- Maintain the same functionality
- Keep it readable for junior developers

Please provide:
1. The optimized code with clear comments explaining changes
2. A summary of improvements made
3. Performance impact estimation (if applicable)
4. Any trade-offs or considerations
```

**Customization Tips:**
- Specify the current performance bottlenecks if known
- Add specific coding standards or style guides to follow

---

#### **Template 3: Algorithm Implementation**

**Purpose:** To implement a specific algorithm or data structure from scratch.

**Template:**
```
Act as a computer science expert and implement the [ALGORITHM_NAME] algorithm in [LANGUAGE].

**Algorithm Requirements:**
- [REQUIREMENT_1]
- [REQUIREMENT_2]
- [REQUIREMENT_3]

**Input:** [INPUT_DESCRIPTION]
**Output:** [OUTPUT_DESCRIPTION]
**Time Complexity Target:** [COMPLEXITY] (if applicable)
**Space Complexity Target:** [COMPLEXITY] (if applicable)

**Additional Requirements:**
- Include comprehensive comments explaining each step
- Add input validation and error handling
- Provide test cases with expected outputs
- Explain the algorithm's approach and why it works

**Test Cases:**
1. Input: [TEST_INPUT_1] → Expected Output: [TEST_OUTPUT_1]
2. Input: [TEST_INPUT_2] → Expected Output: [TEST_OUTPUT_2]
3. Edge Case: [EDGE_CASE] → Expected Output: [EDGE_OUTPUT]
```

---

### 1.2 Debugging and Troubleshooting

---

#### **Template 4: Debug Error Analysis**

**Purpose:** To analyze and fix bugs or errors in existing code.

**Template:**
```
I need help debugging a [LANGUAGE] issue. Act as an experienced debugging expert.

**Problem Description:**
[DETAILED_DESCRIPTION_OF_THE_PROBLEM]

**Error Message/Symptoms:**
```
[PASTE_ERROR_MESSAGE_OR_DESCRIBE_SYMPTOMS]
```

**Code Context:**
```[LANGUAGE]
[PASTE_RELEVANT_CODE_SECTIONS]
```

**Environment Details:**
- [LANGUAGE] Version: [VERSION]
- Operating System: [OS]
- Dependencies: [LIST_KEY_DEPENDENCIES]
- Context: [ADDITIONAL_CONTEXT]

**What I've tried:**
1. [ATTEMPTED_SOLUTION_1]
2. [ATTEMPTED_SOLUTION_2]

Please provide:
1. Root cause analysis
2. Step-by-step debugging approach
3. Corrected code with explanations
4. Prevention strategies for similar issues
```

---

#### **Template 5: Performance Troubleshooting**

**Purpose:** To identify and resolve performance issues in code.

**Template:**
```
I need help with performance analysis and optimization for my [LANGUAGE] application.

**Performance Issue:**
[DESCRIBE_PERFORMANCE_PROBLEM] (e.g., slow response times, high memory usage, CPU spikes)

**Current Metrics:**
- Response Time: [TIME]
- Memory Usage: [MEMORY]
- CPU Usage: [CPU]
- [OTHER_METRICS]

**Code to Analyze:**
```[LANGUAGE]
[PASTE_CODE_THAT_MIGHT_BE_CAUSING_ISSUES]
```

**Use Case Context:**
- Expected load: [LOAD_DESCRIPTION]
- Data size: [DATA_SIZE]
- Frequency of execution: [FREQUENCY]

Please provide:
1. Performance bottleneck identification
2. Profiling recommendations
3. Optimization strategies ranked by impact
4. Code improvements with before/after comparisons
5. Monitoring suggestions
```

---

### 1.3 Code Review and Quality

---

#### **Template 6: Comprehensive Code Review**

**Purpose:** To conduct a thorough code review focusing on multiple quality aspects.

**Template:**
```
Please conduct a comprehensive code review of the following [LANGUAGE] code. Act as a senior developer performing a pull request review.

**Code to Review:**
```[LANGUAGE]
[PASTE_CODE_HERE]
```

**Review Focus Areas:**
- [ ] Code correctness and logic
- [ ] Performance and efficiency
- [ ] Security vulnerabilities
- [ ] Code readability and maintainability
- [ ] Best practices adherence
- [ ] Error handling and edge cases
- [ ] Testing considerations
- [ ] Documentation quality

**Specific Concerns:**
[LIST_ANY_SPECIFIC_AREAS_OF_CONCERN]

**Project Context:**
[BRIEF_PROJECT_DESCRIPTION_AND_CONSTRAINTS]

Please provide:
1. **Critical Issues** (must fix before merge)
2. **Suggestions** (improvements for better code quality)
3. **Nitpicks** (minor style/preference issues)
4. **Positive Feedback** (what's done well)
5. **Overall Assessment** and recommendation (approve/changes needed/reject)
```

---

### 1.4 Documentation and Comments

---

#### **Template 7: Generate Technical Documentation**

**Purpose:** To create comprehensive technical documentation for code or systems.

**Template:**
```
Create comprehensive technical documentation for the following [TYPE] (function/class/module/API/system).

**Code/System to Document:**
```[LANGUAGE]
[PASTE_CODE_OR_DESCRIBE_SYSTEM]
```

**Documentation Requirements:**
- **Audience:** [TARGET_AUDIENCE] (e.g., junior developers, API consumers, system administrators)
- **Format:** [DOCUMENTATION_FORMAT] (e.g., README, API docs, inline comments, wiki)
- **Detail Level:** [LEVEL] (high-level overview, detailed implementation, both)

**Include:**
- [ ] Purpose and overview
- [ ] Installation/setup instructions
- [ ] Usage examples with expected outputs
- [ ] Parameter/configuration details
- [ ] Return values/responses
- [ ] Error conditions and handling
- [ ] Performance considerations
- [ ] Dependencies and requirements
- [ ] Troubleshooting guide
- [ ] [ADDITIONAL_REQUIREMENTS]

**Style Preferences:**
[DOCUMENTATION_STYLE_PREFERENCES]
```

---

#### **Template 8: Add Inline Code Comments**

**Purpose:** To add clear, helpful comments to existing code.

**Template:**
```
Please add comprehensive inline comments to the following [LANGUAGE] code. Focus on making the code self-documenting for developers who are [SKILL_LEVEL] with [LANGUAGE].

**Code to Comment:**
```[LANGUAGE]
[PASTE_CODE_HERE]
```

**Commenting Guidelines:**
- Explain the "why" not just the "what"
- Comment complex algorithms and business logic
- Explain non-obvious variable names or magic numbers
- Add TODO/FIXME/NOTE comments where appropriate
- Use [COMMENT_STYLE] commenting style

**Code Context:**
[BRIEF_DESCRIPTION_OF_WHAT_THE_CODE_DOES]

**Target Audience:**
[DESCRIBE_WHO_WILL_READ_THIS_CODE]

Please return the code with thoughtful, clear comments that enhance understanding without cluttering the code.
```

---

## 2. Songwriting Templates

### 2.1 Lyric Generation and Development

---

#### **Template 9: Genre-Specific Lyric Generator**

**Purpose:** To generate lyrics tailored to specific musical genres and themes.

**Template:**
```
Act as a professional songwriter specializing in [GENRE] music. Write lyrics for a song with the following specifications:

**Song Details:**
- **Genre:** [GENRE] (e.g., pop, rock, country, hip-hop, folk, R&B)
- **Theme/Topic:** [MAIN_THEME]
- **Mood/Emotion:** [EMOTIONAL_TONE] (e.g., uplifting, melancholic, energetic, contemplative)
- **Target Audience:** [AUDIENCE] (e.g., young adults, general audience, specific demographic)

**Structure Requirements:**
- **Song Length:** [APPROXIMATE_LENGTH] (e.g., 3-4 minutes, radio-friendly)
- **Verse Count:** [NUMBER] verses
- **Chorus:** [STYLE] (e.g., catchy and repetitive, anthemic, intimate)
- **Bridge:** [INCLUDE/EXCLUDE] - [BRIDGE_STYLE] if included
- **Other Sections:** [PRE_CHORUS/OUTRO/INTRO_REQUIREMENTS]

**Lyrical Specifications:**
- **Perspective:** [POINT_OF_VIEW] (1st person, 3rd person, storytelling)
- **Rhyme Scheme:** [SCHEME] (ABAB, AABB, or flexible)
- **Language Style:** [STYLE] (simple/accessible, poetic/metaphorical, conversational, edgy)
- **Key Message:** [CORE_MESSAGE_OR_STORY]

**Avoid:**
- [CLICHES_TO_AVOID]
- [TOPICS_TO_AVOID]
- [LANGUAGE_RESTRICTIONS]

Please provide complete lyrics with clear section labels and suggest a potential title.
```

**Example:**
```
Act as a professional songwriter specializing in indie folk music. Write lyrics for a song with the following specifications:

**Song Details:**
- **Genre:** Indie folk
- **Theme/Topic:** Finding peace after a difficult breakup
- **Mood/Emotion:** Bittersweet but ultimately hopeful
- **Target Audience:** Young adults (20-35)

**Structure Requirements:**
- **Song Length:** 3-4 minutes, radio-friendly
- **Verse Count:** 2 verses
- **Chorus:** Intimate but memorable, not too anthemic
- **Bridge:** Include - reflective and introspective
- **Other Sections:** Simple intro, gentle outro

**Lyrical Specifications:**
- **Perspective:** 1st person, personal experience
- **Rhyme Scheme:** Flexible, prioritize natural flow over strict rhyming
- **Language Style:** Poetic but accessible, nature metaphors welcome
- **Key Message:** Growth comes from letting go, finding strength in solitude

**Avoid:**
- Cliché breakup lines ("you broke my heart", "love is blind")
- Overly dramatic or bitter language
- References to specific technology or pop culture

Please provide complete lyrics with clear section labels and suggest a potential title.
```

---

#### **Template 10: Lyric Improvement and Refinement**

**Purpose:** To improve existing lyrics with specific focus areas.

**Template:**
```
I need help refining and improving my song lyrics. Act as an experienced songwriter and lyric coach.

**Current Lyrics:**
```
[PASTE_YOUR_CURRENT_LYRICS_HERE]
```

**Improvement Goals:**
- [ ] Strengthen the emotional impact
- [ ] Improve rhyme scheme and flow
- [ ] Enhance imagery and metaphors
- [ ] Better storytelling/narrative coherence
- [ ] Make chorus more memorable/catchy
- [ ] Improve word choice and vocabulary
- [ ] [SPECIFIC_GOAL_1]
- [ ] [SPECIFIC_GOAL_2]

**Song Context:**
- **Genre:** [GENRE]
- **Intended Mood:** [MOOD]
- **Target Audience:** [AUDIENCE]
- **Key Message:** [MESSAGE]

**Specific Issues I've Noticed:**
- [ISSUE_1]
- [ISSUE_2]
- [ISSUE_3]

**Constraints:**
- Keep the overall theme and story
- Maintain [SPECIFIC_ELEMENTS_TO_PRESERVE]
- Song structure should remain [CURRENT_STRUCTURE]

Please provide:
1. Revised lyrics with improvements highlighted
2. Explanation of changes made and why
3. Alternative word/phrase suggestions for key lines
4. Overall assessment and additional recommendations
```

---

### 2.2 Song Structure and Arrangement

---

#### **Template 11: Song Structure Planner**

**Purpose:** To plan the overall structure and arrangement of a song.

**Template:**
```
Help me plan the structure and arrangement for a [GENRE] song. Act as a music producer and songwriter.

**Song Concept:**
- **Title:** [WORKING_TITLE]
- **Genre:** [GENRE]
- **Tempo:** [BPM] BPM (or [TEMPO_DESCRIPTION] if unsure)
- **Key:** [KEY] (or suggest appropriate key)
- **Duration Target:** [LENGTH]
- **Mood/Energy:** [ENERGY_DESCRIPTION]

**Story/Theme:**
[BRIEF_DESCRIPTION_OF_SONG_THEME_OR_STORY]

**Arrangement Preferences:**
- **Instrumentation:** [DESIRED_INSTRUMENTS]
- **Vocal Style:** [VOCAL_APPROACH]
- **Dynamics:** [DYNAMIC_RANGE] (e.g., consistent energy, builds from quiet to loud)
- **Commercial Goals:** [RADIO_FRIENDLY/ARTISTIC/etc.]

**Specific Requirements:**
- [REQUIREMENT_1] (e.g., needs a strong hook within first 30 seconds)
- [REQUIREMENT_2] (e.g., bridge should contrast significantly from verses)
- [REQUIREMENT_3]

Please provide:
1. **Recommended song structure** (with timing estimates)
2. **Section-by-section arrangement notes** (instrumentation, dynamics, vocal approach)
3. **Chord progression suggestions** for each section
4. **Production tips** specific to the genre
5. **Hook and catchiness strategies**
```

---

### 2.3 Chord Progression and Music Theory

---

#### **Template 12: Chord Progression Generator**

**Purpose:** To generate chord progressions tailored to specific moods and genres.

**Template:**
```
Create chord progressions for a [GENRE] song. Act as a music theory expert and composer.

**Musical Requirements:**
- **Key:** [KEY] (major/minor)
- **Genre:** [GENRE]
- **Mood:** [MOOD_DESCRIPTION]
- **Tempo:** [TEMPO] (fast/medium/slow or specific BPM)
- **Complexity Level:** [BEGINNER/INTERMEDIATE/ADVANCED]

**Song Sections Needed:**
- [ ] Verse progression
- [ ] Chorus progression  
- [ ] Bridge progression
- [ ] Pre-chorus (if applicable)
- [ ] Intro/Outro variations

**Preferences:**
- **Chord Types:** [TRIADS_ONLY/SEVENTH_CHORDS/EXTENSIONS_WELCOME]
- **Movement Style:** [SMOOTH_VOICE_LEADING/DRAMATIC_JUMPS/MIXED]
- **Borrowing:** [ALLOW_BORROWED_CHORDS] from related keys
- **Modulation:** [INCLUDE/AVOID] key changes

**Inspiration/Reference:**
- Chord progressions similar to: [REFERENCE_SONGS] (optional)
- Avoid progressions that sound like: [SONGS_TO_AVOID] (optional)

Please provide:
1. **Chord progressions** for each section (both Roman numerals and chord names)
2. **Strumming/rhythm suggestions** appropriate for the genre
3. **Voice leading notes** for smooth transitions
4. **Alternative variations** for added interest
5. **Capo/fingering suggestions** if acoustic guitar is involved
```

---

## 3. Creative Writing Templates

### 3.1 Story Development and Plotting

---

#### **Template 13: Story Concept Generator**

**Purpose:** To generate complete story concepts with plot, characters, and setting.

**Template:**
```
Create a compelling story concept for a [GENRE] [FORMAT]. Act as a creative writing expert and story developer.

**Story Parameters:**
- **Genre:** [GENRE] (e.g., mystery, sci-fi, romance, historical fiction, fantasy)
- **Format:** [FORMAT] (short story, novella, novel, screenplay, etc.)
- **Target Length:** [LENGTH] (word count or page count)
- **Target Audience:** [AUDIENCE] (YA, adult, children, specific demographic)
- **Tone:** [TONE] (dark, humorous, serious, whimsical, gritty)

**Theme/Message Requirements:**
- **Central Theme:** [THEME] (optional - e.g., redemption, coming of age, social justice)
- **Message/Takeaway:** [MESSAGE] (what should readers learn or feel?)

**Setting Preferences:**
- **Time Period:** [TIME] (contemporary, historical period, future, fantasy time)
- **Location:** [SETTING] (urban, rural, fictional world, specific real location)
- **World-building Complexity:** [SIMPLE/MODERATE/EXTENSIVE]

**Story Elements to Include:**
- [REQUIRED_ELEMENT_1] (e.g., must include a mystery, romantic subplot, etc.)
- [REQUIRED_ELEMENT_2]
- [REQUIRED_ELEMENT_3]

**Constraints/Restrictions:**
- Avoid: [ELEMENTS_TO_AVOID]
- Content rating: [RATING] (G, PG, PG-13, R, etc.)

Please provide:
1. **Compelling logline** (1-2 sentences)
2. **Main plot outline** (beginning, middle, end)
3. **Primary characters** (protagonist, antagonist, key supporting characters)
4. **Setting and world details**
5. **Central conflict and stakes**
6. **Unique hook** (what makes this story stand out)
7. **Potential subplots**
```

---

#### **Template 14: Plot Problem Solver**

**Purpose:** To solve specific plotting issues or story problems.

**Template:**
```
I need help solving a plotting issue in my [GENRE] story. Act as a story consultant and plot doctor.

**Current Story Context:**
[BRIEF_SUMMARY_OF_YOUR_STORY_SO_FAR]

**The Problem:**
[DETAILED_DESCRIPTION_OF_THE_PLOTTING_ISSUE]

**Story Details:**
- **Genre:** [GENRE]
- **Target Audience:** [AUDIENCE] 
- **Story Length:** [LENGTH]
- **Point of View:** [POV]
- **Tone:** [TONE]

**Key Characters Involved:**
- **Protagonist:** [BRIEF_DESCRIPTION]
- **Antagonist:** [BRIEF_DESCRIPTION]
- **Others:** [OTHER_RELEVANT_CHARACTERS]

**Constraints:**
- Must maintain: [ELEMENTS_THAT_CANNOT_CHANGE]
- Story structure: [ACTS/CHAPTERS_ESTABLISHED]
- Established character motivations: [KEY_MOTIVATIONS]

**Potential Solutions I've Considered:**
1. [SOLUTION_ATTEMPT_1] - [WHY_IT_DOESN'T_WORK]
2. [SOLUTION_ATTEMPT_2] - [WHY_IT_DOESN'T_WORK]

Please provide:
1. **Analysis of the core issue**
2. **3-5 potential solutions** with pros and cons
3. **Recommended approach** and reasoning
4. **Implementation strategy** (how to execute the solution)
5. **Potential ripple effects** on other story elements
```

---

### 3.2 Character Creation and Development

---

#### **Template 15: Character Development Deep Dive**

**Purpose:** To create rich, multi-dimensional characters with depth and authenticity.

**Template:**
```
Create a detailed character profile for my [GENRE] story. Act as a character development specialist.

**Basic Character Information:**
- **Role in Story:** [PROTAGONIST/ANTAGONIST/SUPPORTING/etc.]
- **Age:** [AGE] or [AGE_RANGE]
- **Gender:** [GENDER]
- **Occupation:** [JOB] (current or most relevant)

**Story Context:**
- **Genre:** [GENRE]
- **Setting:** [TIME_PERIOD_AND_LOCATION]
- **Story Theme:** [MAIN_THEME]
- **Character's Role in Theme:** [HOW_CHARACTER_RELATES_TO_THEME]

**Character Requirements:**
- **Personality Archetype:** [ARCHETYPE] (mentor, rebel, innocent, etc.) - optional
- **Primary Goal:** [WHAT_CHARACTER_WANTS_MOST]
- **Greatest Fear:** [BIGGEST_FEAR]
- **Fatal Flaw:** [CHARACTER_WEAKNESS]
- **Character Arc:** [HOW_SHOULD_CHARACTER_CHANGE] from beginning to end

**Relationships:**
- **Key Relationships:** [IMPORTANT_PEOPLE_IN_CHARACTER'S_LIFE]
- **Conflict Sources:** [WHO_OR_WHAT_OPPOSES_CHARACTER]

**Specific Traits Needed:**
- [REQUIRED_TRAIT_1] (e.g., must be skilled in martial arts)
- [REQUIRED_TRAIT_2] (e.g., has a secret that drives the plot)
- [REQUIRED_TRAIT_3]

Please provide:
1. **Complete character profile** including backstory, personality, appearance
2. **Psychological depth** - motivations, fears, contradictions
3. **Speaking style and mannerisms**
4. **Character arc progression** throughout the story
5. **Relationship dynamics** with other characters
6. **Unique details** that make the character memorable
7. **Potential dialogue samples** in the character's voice
```

---

## 4. Business/Project Templates

### 4.1 Project Planning and Management

---

#### **Template 16: Project Scope and Planning**

**Purpose:** To create comprehensive project plans with clear scope and deliverables.

**Template:**
```
Help me create a comprehensive project plan. Act as an experienced project manager and business analyst.

**Project Overview:**
- **Project Name:** [PROJECT_NAME]
- **Project Type:** [TYPE] (software development, marketing campaign, product launch, etc.)
- **Duration:** [ESTIMATED_TIMELINE]
- **Budget Range:** [BUDGET] (if applicable)
- **Team Size:** [TEAM_SIZE] people

**Business Context:**
- **Primary Goal:** [MAIN_OBJECTIVE]
- **Success Metrics:** [HOW_SUCCESS_WILL_BE_MEASURED]
- **Target Audience/Users:** [WHO_WILL_BENEFIT]
- **Business Value:** [WHY_THIS_PROJECT_MATTERS]

**Project Requirements:**
- **Must Have Features/Deliverables:**
  - [REQUIREMENT_1]
  - [REQUIREMENT_2]
  - [REQUIREMENT_3]
- **Nice to Have Features:**
  - [NICE_TO_HAVE_1]
  - [NICE_TO_HAVE_2]

**Constraints:**
- **Timeline Constraints:** [DEADLINES_OR_TIME_LIMITS]
- **Budget Constraints:** [FINANCIAL_LIMITATIONS]
- **Resource Constraints:** [TEAM_OR_SKILL_LIMITATIONS]
- **Technical Constraints:** [TECHNOLOGY_OR_PLATFORM_LIMITATIONS]

**Stakeholders:**
- **Project Sponsor:** [SPONSOR_ROLE]
- **End Users:** [USER_DESCRIPTION]
- **Other Stakeholders:** [OTHER_INTERESTED_PARTIES]

Please provide:
1. **Detailed project scope** with clear boundaries
2. **Work breakdown structure** (main phases and tasks)
3. **Timeline and milestones** with dependencies
4. **Resource allocation** and team roles
5. **Risk assessment** and mitigation strategies
6. **Communication plan** and reporting structure
7. **Success criteria** and acceptance criteria
```

---

### 4.2 Feature Specification and Requirements

---

#### **Template 17: User Story Creation**

**Purpose:** To create detailed user stories with acceptance criteria for development projects.

**Template:**
```
Create detailed user stories for the following feature. Act as a product manager and business analyst.

**Feature Overview:**
- **Feature Name:** [FEATURE_NAME]
- **Product/System:** [PRODUCT_NAME]
- **Feature Priority:** [HIGH/MEDIUM/LOW]
- **Target Release:** [RELEASE_VERSION_OR_DATE]

**User Context:**
- **Primary User Type:** [USER_ROLE] (e.g., end customer, admin, content creator)
- **User Skill Level:** [TECHNICAL_PROFICIENCY]
- **Usage Context:** [WHEN_AND_WHERE_USED]
- **User Goals:** [WHAT_USER_WANTS_TO_ACCOMPLISH]

**Functional Requirements:**
- [REQUIREMENT_1]
- [REQUIREMENT_2]
- [REQUIREMENT_3]

**Business Requirements:**
- **Business Value:** [WHY_THIS_FEATURE_IS_NEEDED]
- **Success Metrics:** [HOW_SUCCESS_WILL_BE_MEASURED]
- **Business Rules:** [ANY_CONSTRAINTS_OR_RULES]

**Technical Context:**
- **Platform:** [WEB/MOBILE/DESKTOP/API]
- **Integration Points:** [SYSTEMS_TO_INTEGRATE_WITH]
- **Performance Requirements:** [SPEED_OR_SCALE_REQUIREMENTS]

**Design Constraints:**
- [DESIGN_CONSTRAINT_1]
- [DESIGN_CONSTRAINT_2]

Please provide:
1. **Epic-level user story** (high-level feature description)
2. **Detailed user stories** in "As a [user], I want [goal] so that [benefit]" format
3. **Acceptance criteria** for each story (Given/When/Then format)
4. **Edge cases and error scenarios**
5. **Dependencies** on other features or systems
6. **Definition of Done** checklist
7. **Testing scenarios** (positive and negative cases)
```

---

## 5. Learning and Analysis Templates

### 5.1 Research and Analysis

---

#### **Template 18: Comprehensive Research Brief**

**Purpose:** To create structured research plans for investigating topics or problems.

**Template:**
```
Create a comprehensive research plan for investigating [RESEARCH_TOPIC]. Act as a research methodologist and subject matter expert.

**Research Objective:**
- **Primary Question:** [MAIN_RESEARCH_QUESTION]
- **Secondary Questions:**
  - [SECONDARY_QUESTION_1]
  - [SECONDARY_QUESTION_2]
  - [SECONDARY_QUESTION_3]

**Research Context:**
- **Background:** [WHAT_WE_ALREADY_KNOW]
- **Purpose:** [WHY_THIS_RESEARCH_IS_NEEDED]
- **Target Audience:** [WHO_WILL_USE_THE_RESULTS]
- **Deadline:** [WHEN_RESULTS_ARE_NEEDED]

**Scope and Constraints:**
- **Scope:** [WHAT_IS_INCLUDED_IN_THE_RESEARCH]
- **Out of Scope:** [WHAT_IS_EXPLICITLY_EXCLUDED]
- **Resource Constraints:** [TIME/BUDGET/ACCESS_LIMITATIONS]
- **Quality Requirements:** [DEPTH_AND_RELIABILITY_NEEDED]

**Research Focus Areas:**
- [FOCUS_AREA_1] - [WHY_IMPORTANT]
- [FOCUS_AREA_2] - [WHY_IMPORTANT]
- [FOCUS_AREA_3] - [WHY_IMPORTANT]

**Preferred Sources:**
- **Primary Sources:** [ORIGINAL_DATA_SOURCES]
- **Secondary Sources:** [ANALYSIS_AND_COMMENTARY]
- **Source Credibility Requirements:** [QUALITY_STANDARDS]

Please provide:
1. **Detailed research methodology** and approach
2. **Source identification strategy** (where to find information)
3. **Research timeline** with milestones
4. **Data collection framework** (what to look for)
5. **Analysis framework** (how to evaluate findings)
6. **Quality assurance** methods for reliability
7. **Deliverable structure** (how to present findings)
8. **Potential challenges** and mitigation strategies
```

---

### 5.2 Concept Explanation and Tutorial Creation

---

#### **Template 19: Educational Content Creator**

**Purpose:** To create clear, educational explanations of complex concepts.

**Template:**
```
Create educational content explaining [CONCEPT/TOPIC]. Act as an expert educator and curriculum designer.

**Content Specifications:**
- **Topic:** [SPECIFIC_CONCEPT_OR_SKILL]
- **Target Audience:** [AUDIENCE_DESCRIPTION_AND_SKILL_LEVEL]
- **Content Format:** [TUTORIAL/EXPLANATION/GUIDE/COURSE_MODULE]
- **Content Length:** [WORD_COUNT_OR_TIME_ESTIMATE]
- **Delivery Medium:** [WRITTEN/VIDEO_SCRIPT/INTERACTIVE/etc.]

**Learning Objectives:**
After completing this content, learners should be able to:
- [LEARNING_OBJECTIVE_1]
- [LEARNING_OBJECTIVE_2]
- [LEARNING_OBJECTIVE_3]

**Audience Analysis:**
- **Prior Knowledge:** [WHAT_AUDIENCE_ALREADY_KNOWS]
- **Knowledge Gaps:** [WHAT_THEY_DON'T_KNOW]
- **Learning Style Preferences:** [VISUAL/AUDITORY/HANDS_ON/etc.]
- **Common Misconceptions:** [TYPICAL_MISUNDERSTANDINGS]

**Content Requirements:**
- **Complexity Level:** [BEGINNER/INTERMEDIATE/ADVANCED]
- **Practical Application:** [HOW_CONCEPT_IS_USED_IN_REAL_WORLD]
- **Examples Needed:** [TYPES_OF_EXAMPLES_TO_INCLUDE]
- **Interactive Elements:** [EXERCISES/QUIZZES/ACTIVITIES_NEEDED]

**Constraints:**
- **Time Constraints:** [LEARNING_TIME_LIMITATIONS]
- **Prerequisites:** [REQUIRED_PRIOR_KNOWLEDGE]
- **Accessibility:** [SPECIAL_ACCESSIBILITY_NEEDS]

Please provide:
1. **Content outline** with logical progression
2. **Detailed explanation** with clear, simple language
3. **Relevant examples** and analogies
4. **Practical exercises** or applications
5. **Assessment questions** to check understanding
6. **Common pitfalls** and how to avoid them
7. **Additional resources** for deeper learning
8. **Summary** and key takeaways
```

---

## 6. Meta-Prompts

### 6.1 Prompt Creation and Optimization

---

#### **Template 20: Custom Prompt Generator**

**Purpose:** To create specialized prompts for specific tasks or domains.

**Template:**
```
Create a custom prompt template for [SPECIFIC_TASK_OR_DOMAIN]. Act as a prompt engineering expert.

**Task Description:**
[DETAILED_DESCRIPTION_OF_THE_TASK_THE_PROMPT_SHOULD_ACCOMPLISH]

**Use Case Context:**
- **Domain:** [FIELD_OR_INDUSTRY] (e.g., marketing, education, software development)
- **User Type:** [WHO_WILL_USE_THIS_PROMPT] (skill level, role, context)
- **Frequency of Use:** [HOW_OFTEN_PROMPT_WILL_BE_USED]
- **Output Requirements:** [WHAT_TYPE_OF_OUTPUT_IS_EXPECTED]

**Prompt Requirements:**
- **AI Role:** [WHAT_PERSONA_SHOULD_AI_ADOPT]
- **Input Variables:** [WHAT_INFORMATION_USER_NEEDS_TO_PROVIDE]
- **Output Format:** [STRUCTURE_OF_DESIRED_RESPONSE]
- **Quality Standards:** [CRITERIA_FOR_GOOD_OUTPUT]

**Constraints:**
- **Length Limitations:** [MAX_PROMPT_LENGTH_OR_OUTPUT_LENGTH]
- **Complexity Level:** [SIMPLE/MODERATE/COMPLEX]
- **Special Requirements:** [UNIQUE_NEEDS_OR_CONSTRAINTS]

**Examples of Good Outputs:**
[PROVIDE_1_2_EXAMPLES_OF_DESIRED_RESULTS]

Please provide:
1. **Complete prompt template** with clear [VARIABLE] placeholders
2. **Usage instructions** for filling in variables
3. **Example implementation** with variables filled in
4. **Expected output description**
5. **Customization tips** for different use cases
6. **Common pitfalls** to avoid when using the prompt
7. **Variations** for different scenarios or skill levels
```

---

#### **Template 21: Prompt Optimization and Improvement**

**Purpose:** To analyze and improve existing prompts for better results.

**Template:**
```
Analyze and improve the following prompt. Act as a prompt engineering specialist.

**Current Prompt:**
```
[PASTE_YOUR_CURRENT_PROMPT_HERE]
```

**Current Issues:**
- [ISSUE_1] (e.g., outputs are too generic, AI misunderstands intent)
- [ISSUE_2] (e.g., responses lack detail, format is inconsistent)
- [ISSUE_3] (e.g., doesn't work well for all use cases)

**Desired Improvements:**
- [IMPROVEMENT_GOAL_1]
- [IMPROVEMENT_GOAL_2]
- [IMPROVEMENT_GOAL_3]

**Context:**
- **Task Purpose:** [WHAT_THE_PROMPT_SHOULD_ACCOMPLISH]
- **Target Users:** [WHO_USES_THIS_PROMPT]
- **Expected Output:** [WHAT_KIND_OF_RESPONSE_IS_NEEDED]
- **Usage Frequency:** [HOW_OFTEN_IT'S_USED]

**Success Criteria:**
[HOW_WILL_YOU_KNOW_THE_IMPROVED_PROMPT_IS_BETTER]

**Constraints:**
- Keep the core functionality
- Maintain compatibility with [SPECIFIC_REQUIREMENTS]
- [OTHER_CONSTRAINTS]

Please provide:
1. **Analysis** of current prompt strengths and weaknesses
2. **Improved prompt version** with changes highlighted
3. **Explanation** of improvements made and why
4. **Before/after comparison** showing expected improvement
5. **Testing suggestions** to validate improvements
6. **Alternative versions** for different use cases
7. **Best practices** applied in the improvement
```

---

## Conclusion

This collection provides over 20 comprehensive prompt templates across 6 major categories, with more templates to be added in each section. Each template includes:

- Clear purpose and context
- Customizable template text with variables
- Usage instructions and examples
- Expected outputs and customization tips

These templates are designed to be immediately practical and easily adaptable to your specific needs as both a developer and songwriter. Copy any template, fill in the variables with your specific requirements, and use them with your preferred AI tools.

---

#### **Template 22: Architecture and System Design**

**Purpose:** To design software architecture and system components.

**Template:**
```
Design a software architecture for [SYSTEM_TYPE]. Act as a senior software architect.

**System Requirements:**
- **System Purpose:** [WHAT_THE_SYSTEM_DOES]
- **Scale:** [EXPECTED_USERS/LOAD/DATA_VOLUME]
- **Performance Requirements:** [SPEED/THROUGHPUT/LATENCY_NEEDS]
- **Availability Requirements:** [UPTIME_EXPECTATIONS]
- **Security Requirements:** [SECURITY_LEVEL_AND_COMPLIANCE]

**Technical Constraints:**
- **Technology Stack:** [PREFERRED_OR_REQUIRED_TECHNOLOGIES]
- **Platform:** [CLOUD/ON_PREMISE/HYBRID]
- **Budget Constraints:** [COST_LIMITATIONS]
- **Team Expertise:** [TEAM_SKILL_LEVELS]
- **Timeline:** [DEVELOPMENT_TIMELINE]

**Functional Requirements:**
- [CORE_FEATURE_1]
- [CORE_FEATURE_2]
- [CORE_FEATURE_3]
- [INTEGRATION_REQUIREMENTS]

**Non-Functional Requirements:**
- **Scalability:** [GROWTH_EXPECTATIONS]
- **Maintainability:** [MAINTENANCE_CONSIDERATIONS]
- **Reliability:** [ERROR_TOLERANCE]
- **Monitoring:** [OBSERVABILITY_NEEDS]

Please provide:
1. **High-level architecture diagram** (described in text)
2. **Component breakdown** with responsibilities
3. **Data flow** and interaction patterns
4. **Technology recommendations** with justifications
5. **Scalability strategy** for future growth
6. **Security architecture** and considerations
7. **Deployment strategy** and infrastructure needs
8. **Risk assessment** and mitigation strategies
```

---

#### **Template 23: API Design and Documentation**

**Purpose:** To design and document APIs with clear specifications.

**Template:**
```
Design a RESTful API for [API_PURPOSE]. Act as an API architect and technical writer.

**API Overview:**
- **Purpose:** [WHAT_THE_API_DOES]
- **Target Users:** [DEVELOPERS/SYSTEMS_THAT_WILL_USE_IT]
- **Authentication:** [AUTH_METHOD] (API key, OAuth, JWT, etc.)
- **Rate Limiting:** [REQUESTS_PER_MINUTE/HOUR]
- **Versioning Strategy:** [HOW_VERSIONS_WILL_BE_MANAGED]

**Core Resources:**
- **Resource 1:** [RESOURCE_NAME] - [DESCRIPTION]
- **Resource 2:** [RESOURCE_NAME] - [DESCRIPTION]
- **Resource 3:** [RESOURCE_NAME] - [DESCRIPTION]

**Key Operations:**
- [OPERATION_1] (e.g., Create user account)
- [OPERATION_2] (e.g., Retrieve user profile)
- [OPERATION_3] (e.g., Update user settings)
- [OPERATION_4] (e.g., Delete user data)

**Data Requirements:**
- **Input Validation:** [VALIDATION_RULES]
- **Output Formats:** [JSON/XML/etc.]
- **Pagination:** [HOW_LARGE_DATASETS_ARE_HANDLED]
- **Filtering/Sorting:** [QUERY_CAPABILITIES]

**Quality Requirements:**
- **Response Time:** [PERFORMANCE_EXPECTATIONS]
- **Error Handling:** [HOW_ERRORS_ARE_COMMUNICATED]
- **Documentation Style:** [OPENAPI/SWAGGER/CUSTOM]

Please provide:
1. **Complete API specification** with endpoints
2. **Request/response examples** for each endpoint
3. **Error codes and messages** documentation
4. **Authentication flow** explanation
5. **SDK/client library considerations**
6. **Testing strategy** for the API
7. **Versioning and deprecation** policy
```

---

### 1.5 Testing and Quality Assurance

---

#### **Template 24: Test Case Generator**

**Purpose:** To generate comprehensive test cases for software features.

**Template:**
```
Generate comprehensive test cases for [FEATURE_OR_FUNCTION]. Act as a QA engineer and test specialist.

**Feature Under Test:**
[DETAILED_DESCRIPTION_OF_FEATURE_OR_FUNCTION]

**Test Scope:**
- **Functional Testing:** [INCLUDE/EXCLUDE]
- **Performance Testing:** [INCLUDE/EXCLUDE]
- **Security Testing:** [INCLUDE/EXCLUDE]
- **Usability Testing:** [INCLUDE/EXCLUDE]
- **Compatibility Testing:** [INCLUDE/EXCLUDE]

**Test Environment:**
- **Platform(s):** [PLATFORMS_TO_TEST_ON]
- **Browsers/Devices:** [IF_APPLICABLE]
- **Test Data Requirements:** [WHAT_DATA_IS_NEEDED]
- **Prerequisites:** [SETUP_REQUIREMENTS]

**User Scenarios:**
- **Primary User Flow:** [MAIN_USER_JOURNEY]
- **Alternative Flows:** [OTHER_WAYS_USERS_MIGHT_INTERACT]
- **Edge Cases:** [UNUSUAL_BUT_POSSIBLE_SCENARIOS]

**Acceptance Criteria:**
- [CRITERIA_1]
- [CRITERIA_2]
- [CRITERIA_3]

**Risk Areas:**
- [HIGH_RISK_AREA_1] - [WHY_RISKY]
- [HIGH_RISK_AREA_2] - [WHY_RISKY]

Please provide:
1. **Positive test cases** (happy path scenarios)
2. **Negative test cases** (error conditions and invalid inputs)
3. **Edge cases and boundary testing**
4. **Performance test scenarios** (if applicable)
5. **Security test cases** (if applicable)
6. **Test data requirements** and setup instructions
7. **Expected results** for each test case
8. **Priority levels** for test execution
```

---

#### **Template 25: Code Coverage and Testing Strategy**

**Purpose:** To develop comprehensive testing strategies for code projects.

**Template:**
```
Create a testing strategy for my [LANGUAGE] project. Act as a test automation engineer and QA strategist.

**Project Details:**
- **Project Type:** [WEB_APP/MOBILE_APP/API/LIBRARY/etc.]
- **Technology Stack:** [FRAMEWORKS_AND_TOOLS]
- **Team Size:** [NUMBER_OF_DEVELOPERS]
- **Release Frequency:** [HOW_OFTEN_RELEASES_HAPPEN]
- **Quality Requirements:** [QUALITY_STANDARDS]

**Current State:**
- **Existing Tests:** [WHAT_TESTS_ALREADY_EXIST]
- **Current Coverage:** [COVERAGE_PERCENTAGE] (if known)
- **Pain Points:** [CURRENT_TESTING_CHALLENGES]
- **Time Constraints:** [AVAILABLE_TIME_FOR_TESTING]

**Code Characteristics:**
- **Complexity Level:** [SIMPLE/MODERATE/COMPLEX]
- **Critical Components:** [MOST_IMPORTANT_PARTS_TO_TEST]
- **External Dependencies:** [APIS/DATABASES/SERVICES]
- **Performance Requirements:** [SPEED/LOAD_EXPECTATIONS]

**Testing Goals:**
- **Target Coverage:** [DESIRED_COVERAGE_PERCENTAGE]
- **Test Types Needed:** [UNIT/INTEGRATION/E2E/etc.]
- **Automation Level:** [HOW_MUCH_TO_AUTOMATE]
- **CI/CD Integration:** [CONTINUOUS_TESTING_NEEDS]

Please provide:
1. **Complete testing pyramid** strategy
2. **Test types breakdown** (unit, integration, e2e percentages)
3. **Testing framework recommendations**
4. **Test organization** and file structure
5. **Mocking and stubbing** strategy for dependencies
6. **Continuous testing** integration approach
7. **Code coverage targets** by component
8. **Testing best practices** for the team
9. **Test maintenance** strategy
```

---

## Additional Songwriting Templates

#### **Template 26: Rhyme Scheme Developer**

**Purpose:** To develop effective rhyme schemes and improve lyrical flow.

**Template:**
```
Help me develop a rhyme scheme for my song lyrics. Act as a professional lyricist and poetry expert.

**Song Details:**
- **Genre:** [GENRE]
- **Theme:** [SONG_THEME]
- **Mood:** [EMOTIONAL_TONE]
- **Target Verse Length:** [NUMBER_OF_LINES] lines per verse
- **Chorus Length:** [NUMBER_OF_LINES] lines

**Current Lyrics (if any):**
```
[PASTE_EXISTING_LYRICS_OR_CONCEPT]
```

**Rhyme Preferences:**
- **Rhyme Type:** [PERFECT/SLANT/INTERNAL/MIXED]
- **Complexity:** [SIMPLE/MODERATE/COMPLEX]
- **Pattern Preference:** [AABB/ABAB/ABCB/CUSTOM]
- **Syllable Considerations:** [MATCHING/FLEXIBLE]

**Content Requirements:**
- **Key Words/Phrases to Include:** [IMPORTANT_WORDS_TO_FEATURE]
- **Words/Themes to Avoid:** [RESTRICTIONS]
- **Language Style:** [CONVERSATIONAL/POETIC/MODERN/CLASSIC]

**Musical Considerations:**
- **Emphasis Points:** [WHERE_STRONG_BEATS_FALL]
- **Melodic Flow:** [SMOOTH/RHYTHMIC/SYNCOPATED]
- **Breathing Points:** [WHERE_PAUSES_ARE_NEEDED]

Please provide:
1. **Recommended rhyme scheme** with explanation
2. **Alternative rhyme patterns** for variety
3. **Rhyme word suggestions** for key concepts
4. **Internal rhyme opportunities**
5. **Flow improvement suggestions**
6. **Examples** showing the scheme in action
7. **Tips for maintaining natural language** while rhyming
```

---

#### **Template 27: Song Theme and Story Developer**

**Purpose:** To develop compelling themes and narratives for songs.

**Template:**
```
Help me develop a compelling theme and story for a song. Act as a narrative songwriter and storytelling expert.

**Initial Concept:**
[BRIEF_DESCRIPTION_OF_YOUR_SONG_IDEA_OR_INSPIRATION]

**Song Parameters:**
- **Genre:** [MUSICAL_GENRE]
- **Length:** [APPROXIMATE_SONG_LENGTH]
- **Target Audience:** [WHO_SHOULD_CONNECT_WITH_THIS_SONG]
- **Emotional Journey:** [WHERE_SONG_STARTS_AND_ENDS_EMOTIONALLY]

**Theme Requirements:**
- **Main Theme:** [CENTRAL_MESSAGE_OR_CONCEPT]
- **Universal Appeal:** [HOW_OTHERS_CAN_RELATE]
- **Personal Connection:** [WHY_THIS_MATTERS_TO_YOU]
- **Originality:** [HOW_TO_MAKE_IT_UNIQUE]

**Story Elements:**
- **Perspective:** [1ST_PERSON/3RD_PERSON/MULTIPLE]
- **Time Frame:** [SINGLE_MOMENT/JOURNEY/LIFETIME]
- **Setting:** [WHERE_AND_WHEN_STORY_TAKES_PLACE]
- **Characters:** [WHO_IS_INVOLVED]

**Emotional Requirements:**
- **Starting Emotion:** [HOW_SONG_BEGINS]
- **Climax Emotion:** [PEAK_EMOTIONAL_MOMENT]
- **Resolution:** [HOW_SONG_CONCLUDES]
- **Emotional Complexity:** [SIMPLE/LAYERED/CONFLICTED]

**Constraints:**
- **Avoid:** [CLICHES_OR_TOPICS_TO_AVOID]
- **Include:** [ELEMENTS_THAT_MUST_BE_PRESENT]
- **Tone Limitations:** [CONTENT_APPROPRIATENESS]

Please provide:
1. **Detailed theme development** with layers of meaning
2. **Complete story arc** for the song
3. **Character development** (if applicable)
4. **Scene-by-scene breakdown** for verses/chorus/bridge
5. **Emotional progression** through the song
6. **Unique angles** that differentiate from similar songs
7. **Universal connection points** for broad appeal
8. **Potential metaphors and imagery** to support the theme
```

---

#### **Template 28: Genre-Specific Song Structure**

**Purpose:** To create song structures optimized for specific musical genres.

**Template:**
```
Create an optimal song structure for a [GENRE] song. Act as a music producer and genre specialist.

**Song Specifications:**
- **Genre:** [SPECIFIC_GENRE] (be as specific as possible)
- **Sub-genre/Style:** [STYLE_VARIATIONS] if applicable
- **Target Duration:** [SONG_LENGTH] (radio edit, album track, etc.)
- **Commercial Goals:** [RADIO_FRIENDLY/ARTISTIC/STREAMING_OPTIMIZED]

**Song Content:**
- **Theme:** [SONG_THEME_OR_CONCEPT]
- **Energy Level:** [LOW/MEDIUM/HIGH/VARIABLE]
- **Vocal Style:** [VOCAL_APPROACH]
- **Instrumental Focus:** [KEY_INSTRUMENTS_OR_SOUNDS]

**Structure Preferences:**
- **Complexity:** [SIMPLE/STANDARD/COMPLEX]
- **Hook Placement:** [WHERE_MAIN_HOOKS_SHOULD_BE]
- **Dynamic Range:** [CONSISTENT/BUILDING/VARIED]
- **Repetition Tolerance:** [HOW_MUCH_REPETITION_IS_ACCEPTABLE]

**Commercial Considerations:**
- **Streaming Optimization:** [EARLY_HOOK_PLACEMENT]
- **Radio Requirements:** [TIME_CONSTRAINTS]
- **Live Performance:** [CONCERT_SUITABILITY]
- **Dance/Movement:** [GROOVE_REQUIREMENTS]

**Reference Points:**
- **Similar Artists:** [ARTISTS_IN_GENRE] (optional)
- **Successful Songs:** [REFERENCE_TRACKS] (optional)
- **Avoid Comparisons to:** [SONGS_TO_DIFFERENTIATE_FROM]

Please provide:
1. **Detailed song structure** with timing estimates
2. **Section-by-section purpose** and energy mapping
3. **Genre-specific conventions** to follow or break
4. **Hook and catchiness strategies** for the genre
5. **Bridge and breakdown** recommendations
6. **Intro and outro** considerations
7. **Variation suggestions** for different song goals
8. **Production notes** relevant to structure
```

---

## Additional Creative Writing Templates

#### **Template 29: Dialogue Writing Specialist**

**Purpose:** To create authentic, character-driven dialogue.

**Template:**
```
Create authentic dialogue for my story. Act as a dialogue coach and character voice specialist.

**Scene Context:**
- **Setting:** [WHERE_AND_WHEN_SCENE_TAKES_PLACE]
- **Situation:** [WHAT_IS_HAPPENING_IN_THE_SCENE]
- **Purpose:** [WHAT_THE_SCENE_NEEDS_TO_ACCOMPLISH]
- **Tone:** [SERIOUS/HUMOROUS/TENSE/ROMANTIC/etc.]

**Characters in Scene:**
- **Character 1:** [NAME] - [BRIEF_DESCRIPTION_AND_MOTIVATION]
- **Character 2:** [NAME] - [BRIEF_DESCRIPTION_AND_MOTIVATION]
- **Additional Characters:** [OTHER_SPEAKERS] if applicable

**Character Voices:**
- **[CHARACTER_1_NAME] speaks:** [SPEAKING_STYLE_DESCRIPTION]
- **[CHARACTER_2_NAME] speaks:** [SPEAKING_STYLE_DESCRIPTION]
- **Relationship Dynamic:** [HOW_CHARACTERS_RELATE_TO_EACH_OTHER]

**Dialogue Requirements:**
- **Information to Convey:** [WHAT_READERS_NEED_TO_LEARN]
- **Subtext:** [WHAT_CHARACTERS_AREN'T_SAYING_DIRECTLY]
- **Conflict/Tension:** [SOURCE_OF_DRAMATIC_TENSION]
- **Character Development:** [HOW_CHARACTERS_SHOULD_GROW]

**Style Preferences:**
- **Realism Level:** [NATURALISTIC/STYLIZED/HEIGHTENED]
- **Dialect/Accent:** [SPEECH_PATTERNS_TO_INCLUDE]
- **Time Period:** [HISTORICAL_LANGUAGE_CONSIDERATIONS]
- **Genre Conventions:** [DIALOGUE_STYLE_FOR_GENRE]

**Constraints:**
- **Length:** [APPROXIMATE_WORD_COUNT]
- **Content Rating:** [APPROPRIATE_LANGUAGE_LEVEL]
- **Avoid:** [SPECIFIC_SPEECH_PATTERNS_TO_AVOID]

Please provide:
1. **Complete dialogue scene** with action beats
2. **Character voice differentiation** clearly shown
3. **Subtext and layers** of meaning
4. **Natural speech patterns** and interruptions
5. **Emotional progression** through the conversation
6. **Dialogue tags and action** integration
7. **Revision suggestions** for authenticity
```

---

#### **Template 30: Scene Setting and Atmosphere**

**Purpose:** To create vivid, immersive scene descriptions and atmospheric writing.

**Template:**
```
Create vivid scene descriptions and atmosphere for my story. Act as a descriptive writing expert.

**Scene Requirements:**
- **Location:** [SPECIFIC_SETTING_DESCRIPTION]
- **Time Period:** [WHEN_SCENE_TAKES_PLACE]
- **Time of Day/Season:** [TEMPORAL_CONTEXT]
- **Weather/Climate:** [ATMOSPHERIC_CONDITIONS]

**Mood and Atmosphere:**
- **Desired Mood:** [EMOTIONAL_ATMOSPHERE]
- **Genre Tone:** [GENRE_SPECIFIC_ATMOSPHERE]
- **Symbolic Elements:** [WHAT_SETTING_SHOULD_REPRESENT]
- **Foreshadowing:** [HINTS_ABOUT_FUTURE_EVENTS]

**Sensory Details:**
- **Visual Elements:** [WHAT_CHARACTERS_AND_READERS_SEE]
- **Sounds:** [AUDIO_LANDSCAPE]
- **Smells:** [SCENTS_AND_ODORS]
- **Textures:** [THINGS_CHARACTERS_MIGHT_TOUCH]
- **Tastes:** [IF_APPLICABLE]

**Character Interaction:**
- **POV Character:** [WHO_IS_EXPERIENCING_THE_SCENE]
- **Character's Emotional State:** [HOW_EMOTIONS_AFFECT_PERCEPTION]
- **Physical Position:** [WHERE_CHARACTER_IS_IN_THE_SPACE]
- **Movement:** [HOW_CHARACTER_MOVES_THROUGH_SPACE]

**Story Function:**
- **Plot Purpose:** [HOW_SETTING_SERVES_THE_STORY]
- **Character Development:** [WHAT_SETTING_REVEALS_ABOUT_CHARACTERS]
- **Theme Connection:** [HOW_SETTING_SUPPORTS_THEMES]
- **Pacing:** [FAST/SLOW/CONTEMPLATIVE_DESCRIPTION]

**Style Preferences:**
- **Description Length:** [BRIEF/MODERATE/DETAILED]
- **Language Style:** [SIMPLE/LYRICAL/TECHNICAL]
- **Metaphor Use:** [MINIMAL/MODERATE/EXTENSIVE]

Please provide:
1. **Complete scene description** with rich sensory details
2. **Atmospheric elements** that support mood
3. **Character integration** with the environment
4. **Symbolic and thematic** connections
5. **Pacing and rhythm** appropriate for scene
6. **Unique details** that make setting memorable
7. **Revision suggestions** for enhancement
```

---

## Additional Business Templates

#### **Template 31: Marketing Copy Creator**

**Purpose:** To create compelling marketing copy for various purposes.

**Template:**
```
Create compelling marketing copy for [PRODUCT/SERVICE/CAMPAIGN]. Act as a copywriting expert and marketing strategist.

**Product/Service Details:**
- **Name:** [PRODUCT_OR_SERVICE_NAME]
- **Category:** [WHAT_TYPE_OF_OFFERING]
- **Key Features:** [TOP_3_FEATURES_OR_BENEFITS]
- **Unique Selling Proposition:** [WHAT_MAKES_IT_DIFFERENT]
- **Price Point:** [COST_RANGE_OR_STRATEGY]

**Target Audience:**
- **Primary Audience:** [DETAILED_DEMOGRAPHIC_DESCRIPTION]
- **Pain Points:** [PROBLEMS_AUDIENCE_FACES]
- **Motivations:** [WHAT_DRIVES_PURCHASE_DECISIONS]
- **Communication Style:** [HOW_AUDIENCE_PREFERS_TO_BE_ADDRESSED]

**Marketing Goals:**
- **Primary Objective:** [AWARENESS/CONVERSION/RETENTION/etc.]
- **Call to Action:** [WHAT_AUDIENCE_SHOULD_DO]
- **Success Metrics:** [HOW_SUCCESS_WILL_BE_MEASURED]
- **Campaign Duration:** [TIMELINE_CONSIDERATIONS]

**Copy Requirements:**
- **Format:** [EMAIL/WEBPAGE/AD/SOCIAL_POST/BROCHURE/etc.]
- **Length:** [WORD_COUNT_OR_CHARACTER_LIMITS]
- **Tone:** [PROFESSIONAL/CASUAL/URGENT/FRIENDLY/etc.]
- **Brand Voice:** [BRAND_PERSONALITY_DESCRIPTION]

**Competition and Context:**
- **Competitive Advantage:** [HOW_TO_POSITION_AGAINST_COMPETITORS]
- **Market Context:** [CURRENT_MARKET_CONDITIONS]
- **Seasonal Factors:** [TIMING_CONSIDERATIONS]

**Constraints:**
- **Legal Requirements:** [DISCLAIMERS_OR_COMPLIANCE_NEEDS]
- **Brand Guidelines:** [STYLE_OR_MESSAGING_RESTRICTIONS]
- **Budget Implications:** [COST_MESSAGING_CONSIDERATIONS]

Please provide:
1. **Compelling headline** and subheadings
2. **Feature-benefit translations** for key points
3. **Emotional appeal** elements
4. **Social proof** suggestions (testimonials, reviews)
5. **Clear call-to-action** copy
6. **Urgency and scarcity** elements (if appropriate)
7. **A/B testing variations** for key elements
8. **SEO considerations** (if web copy)
```

---

#### **Template 32: Technical Documentation Writer**

**Purpose:** To create clear, comprehensive technical documentation.

**Template:**
```
Create technical documentation for [SYSTEM/PROCESS/TOOL]. Act as a technical writing expert.

**Documentation Subject:**
- **Product/System:** [WHAT_NEEDS_DOCUMENTATION]
- **Version:** [VERSION_NUMBER_OR_CURRENT_STATE]
- **Complexity Level:** [SIMPLE/MODERATE/COMPLEX]
- **Update Frequency:** [HOW_OFTEN_DOCS_NEED_UPDATES]

**Target Audience:**
- **Primary Users:** [DEVELOPERS/ADMINS/END_USERS/etc.]
- **Technical Level:** [BEGINNER/INTERMEDIATE/EXPERT]
- **Use Cases:** [HOW_AUDIENCE_WILL_USE_DOCUMENTATION]
- **Time Constraints:** [TYPICAL_TIME_PRESSURE_FOR_USERS]

**Documentation Scope:**
- **Getting Started:** [INSTALLATION/SETUP_NEEDS]
- **Core Features:** [MAIN_FUNCTIONALITY_TO_DOCUMENT]
- **Advanced Features:** [COMPLEX_OR_OPTIONAL_FUNCTIONALITY]
- **Troubleshooting:** [COMMON_ISSUES_AND_SOLUTIONS]
- **Integration:** [HOW_IT_WORKS_WITH_OTHER_SYSTEMS]

**Format Requirements:**
- **Documentation Type:** [README/WIKI/API_DOCS/USER_MANUAL/etc.]
- **Platform:** [WHERE_DOCS_WILL_BE_HOSTED]
- **Interactivity:** [STATIC/INTERACTIVE/LIVE_EXAMPLES]
- **Media:** [TEXT_ONLY/SCREENSHOTS/VIDEOS/DIAGRAMS]

**Content Structure:**
- **Organization:** [HIERARCHICAL/SEQUENTIAL/MODULAR]
- **Navigation:** [TABLE_OF_CONTENTS/SEARCH/CROSS_REFERENCES]
- **Code Examples:** [LANGUAGE_AND_STYLE_PREFERENCES]
- **Screenshots:** [WHEN_AND_HOW_TO_USE_VISUALS]

**Maintenance:**
- **Version Control:** [HOW_TO_TRACK_CHANGES]
- **Review Process:** [WHO_VALIDATES_ACCURACY]
- **Feedback Collection:** [HOW_USERS_CAN_SUGGEST_IMPROVEMENTS]

Please provide:
1. **Complete documentation structure** and outline
2. **Clear, step-by-step instructions** for key processes
3. **Code examples** with explanations
4. **Troubleshooting section** with common issues
5. **Quick reference** sections for experienced users
6. **Visual aids** recommendations (diagrams, screenshots)
7. **Maintenance strategy** for keeping docs current
8. **User feedback** integration approach
```

---

## Additional Meta-Prompts

#### **Template 33: Prompt Testing and Validation**

**Purpose:** To test and validate prompt effectiveness across different scenarios.

**Template:**
```
Help me test and validate the effectiveness of my prompt. Act as a prompt evaluation expert.

**Prompt to Test:**
```
[PASTE_THE_PROMPT_YOU_WANT_TO_TEST]
```

**Testing Objectives:**
- **Primary Goal:** [WHAT_THE_PROMPT_SHOULD_ACCOMPLISH]
- **Success Criteria:** [HOW_TO_MEASURE_SUCCESS]
- **Quality Standards:** [WHAT_CONSTITUTES_GOOD_OUTPUT]

**Test Scenarios:**
- **Scenario 1:** [TYPICAL_USE_CASE_DESCRIPTION]
- **Scenario 2:** [EDGE_CASE_OR_DIFFICULT_SCENARIO]
- **Scenario 3:** [ALTERNATIVE_USE_CASE]
- **Scenario 4:** [STRESS_TEST_SCENARIO]

**Evaluation Criteria:**
- **Accuracy:** [HOW_CORRECT_SHOULD_OUTPUTS_BE]
- **Consistency:** [SHOULD_SIMILAR_INPUTS_PRODUCE_SIMILAR_OUTPUTS]
- **Completeness:** [SHOULD_OUTPUTS_BE_COMPREHENSIVE]
- **Usability:** [HOW_EASY_TO_USE_SHOULD_OUTPUTS_BE]
- **Creativity:** [LEVEL_OF_ORIGINALITY_EXPECTED]

**Context Variations:**
- **User Skill Levels:** [BEGINNER/INTERMEDIATE/EXPERT_USERS]
- **Input Quality:** [WELL_FORMED/VAGUE/INCOMPLETE_INPUTS]
- **Domain Knowledge:** [DIFFERENT_SUBJECT_AREAS]

**Potential Issues:**
- **Known Weaknesses:** [AREAS_WHERE_PROMPT_MIGHT_FAIL]
- **Ambiguity Points:** [UNCLEAR_INSTRUCTIONS]
- **Missing Elements:** [WHAT_MIGHT_BE_MISSING]

Please provide:
1. **Systematic testing approach** for the prompt
2. **Test cases** with expected outcomes
3. **Evaluation rubric** for rating outputs
4. **Common failure modes** and how to detect them
5. **Improvement recommendations** based on testing
6. **Validation checklist** for ongoing use
7. **Performance benchmarks** to track over time
```

---

#### **Template 34: Domain-Specific Prompt Adapter**

**Purpose:** To adapt general prompts for specific domains or industries.

**Template:**
```
Adapt this general prompt for the [DOMAIN/INDUSTRY] field. Act as a domain expert and prompt engineering specialist.

**Base Prompt:**
```
[PASTE_THE_GENERAL_PROMPT_TO_ADAPT]
```

**Target Domain:**
- **Industry/Field:** [SPECIFIC_DOMAIN]
- **Specialization:** [PARTICULAR_AREA_WITHIN_DOMAIN]
- **Professional Level:** [ENTRY/MID/SENIOR_LEVEL_PROFESSIONALS]
- **Common Use Cases:** [HOW_DOMAIN_EXPERTS_WOULD_USE_THIS]

**Domain-Specific Requirements:**
- **Technical Language:** [INDUSTRY_JARGON_AND_TERMINOLOGY]
- **Standards/Regulations:** [COMPLIANCE_OR_STANDARD_REQUIREMENTS]
- **Best Practices:** [FIELD_SPECIFIC_BEST_PRACTICES]
- **Common Challenges:** [TYPICAL_PROBLEMS_IN_THIS_DOMAIN]

**Professional Context:**
- **Workflow Integration:** [HOW_PROMPT_FITS_INTO_DAILY_WORK]
- **Stakeholder Considerations:** [WHO_ELSE_MIGHT_USE_OUTPUTS]
- **Quality Requirements:** [DOMAIN_SPECIFIC_QUALITY_STANDARDS]
- **Time Constraints:** [TYPICAL_DEADLINES_IN_DOMAIN]

**Domain Knowledge:**
- **Prerequisites:** [ASSUMED_KNOWLEDGE_FOR_USERS]
- **Key Concepts:** [IMPORTANT_DOMAIN_CONCEPTS_TO_INCLUDE]
- **Common Mistakes:** [TYPICAL_ERRORS_IN_THIS_FIELD]
- **Success Metrics:** [HOW_SUCCESS_IS_MEASURED_IN_DOMAIN]

**Output Customization:**
- **Format Preferences:** [DOMAIN_STANDARD_FORMATS]
- **Detail Level:** [APPROPRIATE_DEPTH_FOR_DOMAIN]
- **Action Orientation:** [HOW_OUTPUTS_SHOULD_BE_ACTIONABLE]

Please provide:
1. **Domain-adapted prompt** with field-specific language
2. **Terminology guide** for key domain terms
3. **Context additions** that improve domain relevance
4. **Examples** using domain-specific scenarios
5. **Quality criteria** specific to the field
6. **Common pitfalls** to avoid in this domain
7. **Integration suggestions** for domain workflows
8. **Validation approach** using domain expertise
```

---

## Quick Reference Templates

#### **Template 35: Daily Standup Generator**

**Purpose:** Quick template for generating daily standup updates.

**Template:**
```
Generate my daily standup update. Focus on clarity and brevity.

**Yesterday's Accomplishments:**
- [TASK_1_COMPLETED]
- [TASK_2_COMPLETED]
- [TASK_3_COMPLETED]

**Today's Goals:**
- [PRIORITY_1]
- [PRIORITY_2]
- [PRIORITY_3]

**Blockers/Challenges:**
- [BLOCKER_1] - [HELP_NEEDED]
- [BLOCKER_2] - [HELP_NEEDED]

**Team Dependencies:**
- [WAITING_FOR] from [TEAM_MEMBER]
- [PROVIDING_TO] for [TEAM_MEMBER]

**Notes:**
[ADDITIONAL_CONTEXT_OR_UPDATES]

Format as a brief, professional standup update.
```

---

#### **Template 36: Bug Report Generator**

**Purpose:** Comprehensive bug reporting template.

**Template:**
```
Create a detailed bug report for this issue. Include all necessary information for developers.

**Bug Summary:**
[ONE_LINE_DESCRIPTION_OF_THE_BUG]

**Environment:**
- **Application Version:** [VERSION]
- **Operating System:** [OS_AND_VERSION]
- **Browser:** [BROWSER_AND_VERSION] (if applicable)
- **Device:** [DEVICE_INFO] (if mobile)

**Steps to Reproduce:**
1. [STEP_1]
2. [STEP_2]
3. [STEP_3]

**Expected Behavior:**
[WHAT_SHOULD_HAPPEN]

**Actual Behavior:**
[WHAT_ACTUALLY_HAPPENS]

**Error Messages:**
```
[PASTE_EXACT_ERROR_MESSAGES]
```

**Additional Context:**
- **Frequency:** [HOW_OFTEN_IT_OCCURS]
- **Workaround:** [TEMPORARY_SOLUTION] (if any)
- **Impact:** [HOW_SEVERELY_IT_AFFECTS_USERS]

Format as a clear, actionable bug report with appropriate priority level.
```

---

## Conclusion and Usage Guide

This comprehensive collection now contains **36 detailed prompt templates** covering:

- **Development (12 templates)**: Code generation, debugging, review, documentation, architecture, testing
- **Songwriting (7 templates)**: Lyrics, structure, themes, rhyme schemes, genre-specific approaches
- **Creative Writing (4 templates)**: Story development, characters, dialogue, scene setting
- **Business/Project (6 templates)**: Planning, specifications, marketing, documentation
- **Learning/Analysis (3 templates)**: Research, education, concept explanation
- **Meta-Prompts (4 templates)**: Prompt creation, optimization, testing, domain adaptation

### How to Use These Templates:

1. **Choose the Right Template**: Select based on your specific task and domain
2. **Fill in Variables**: Replace all `[VARIABLE]` placeholders with your specific information
3. **Customize for Context**: Adapt the template to your specific situation and requirements
4. **Iterate and Improve**: Refine your inputs based on the outputs you receive
5. **Build Your Own**: Use the meta-prompts to create entirely new templates for your unique needs

### Best Practices for Template Usage:

- **Be Specific**: The more detailed information you provide, the better the output
- **Provide Context**: Always include relevant background information
- **Set Clear Expectations**: Define what constitutes a successful output
- **Test and Refine**: Try templates with different inputs to understand their capabilities
- **Combine Templates**: Use multiple templates in sequence for complex projects

### Template Categories Quick Reference:

**For Developers:**
- Templates 1-8, 22-25: Code generation, debugging, review, architecture
- Template 36: Bug reporting

**For Songwriters:**
- Templates 9-12, 26-28: Lyrics, structure, themes, and genre-specific guidance

**For Creative Writers:**
- Templates 13-15, 29-30: Story development, characters, dialogue, and setting

**For Project Managers:**
- Templates 16-17, 31-32, 35: Planning, specifications, documentation, and daily updates

**For Researchers and Learners:**
- Templates 18-19: Research planning and educational content creation

**For Prompt Engineers:**
- Templates 20-21, 33-34: Creating, optimizing, testing, and adapting prompts

Remember: These templates are starting points. The most effective prompts are often those that have been customized and refined through experimentation and iteration. Use these as a foundation to build your own prompt engineering expertise!
