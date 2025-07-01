---
description: "Command to objectively evaluate and improve work quality on 5 axes"
---

# quality - Evaluate work quality on 5 axes

Objectively evaluates created stories and scenes, clarifying areas for improvement.

## Argument Processing

Command arguments: $ARGUMENTS

Argument format: [target] [options]

If arguments are given, they are interpreted as follows:
- 1st argument (evaluation target):
  - `scene [scene_name]` → Evaluate a specific scene
  - `story [title]` → Evaluate the entire story
  - `character [name]` → Evaluate character consistency
  - `dialogue [scene]` → Evaluate conversation naturalness
- Additional options:
  - `--detail` → Detailed evaluation report
  - `--fix` → Suggest fixes for problems
  - `--compare` → Compare before and after fixes

Example: `scene Discovery of the letter --detail`

## Usage

```
/quality [target] [options]
```

## Evaluation Targets

- `scene <scene_name>` - Evaluate a specific scene
- `story <title>` - Evaluate the entire story
- `character <name>` - Evaluate character consistency
- `dialogue <scene>` - Evaluate conversation naturalness

## Options

- `--detail` - Detailed evaluation report
- `--fix` - Suggest fixes for problems
- `--compare` - Compare before and after fixes

## 5-Axis Evaluation System (Max 10 points each)

### 1. Character Consistency
```
Evaluation points:
✓ Actions aligned with core motivation
✓ Consistency of speech style and tone
✓ Maintenance of established relationships
✓ Intentional contradictions vs. unintentional blurring
```

### 2. Physical Logic
```
Evaluation points:
✓ Consistency of time progression
✓ Consistency of spatial arrangement
✓ Clarity of cause and effect
✓ Absence of unnatural coincidences
```

### 3. Psychological Naturalness
```
Evaluation points:
✓ Phased depiction of emotional changes
✓ Clarity of motivation
✓ Natural development of relationships
✓ Depth of internal portrayal
```

### 4. Readability
```
Evaluation points:
✓ Rhythm and tempo of writing
✓ Appropriateness of information volume
✓ Smoothness of scene transitions
✓ Clarity of structure
```

### 5. Emotional Impact
```
Evaluation points:
✓ Presence of relatable moments
✓ Unexpected developments
✓ Memorable scenes/lines
✓ Lingering impression after reading
```

## Execution Examples

### Scene Evaluation
```
User: /quality scene "Discovery of the letter"
Assistant: **[Scene Evaluation: Discovery of the letter]**

Overall Evaluation: 42/50 points

1. Character Consistency: 9/10 ⭐⭐⭐⭐⭐
   ✓ Misaki's value of "knowledge sharing" is reflected in her actions.
   ✓ Polite demeanor is consistent.
   △ Became slightly explanatory due to heightened emotions.

2. Physical Logic: 8/10 ⭐⭐⭐⭐
   ✓ Explanation of letter's preservation state is natural.
   ✓ Timeline is clear.
   ✗ Bookstore layout is somewhat unclear.

3. Psychological Naturalness: 9/10 ⭐⭐⭐⭐⭐
   ✓ Change from surprise to acceptance is gradual.
   ✓ Portrayal conveys the weight of 20 years.
   ✓ Relationship with the old woman is natural.

4. Readability: 7/10 ⭐⭐⭐⭐
   ✓ Scene transitions are smooth.
   ✗ Letter content is a bit long.
   △ Tempo drops in the latter half.

5. Emotional Impact: 9/10 ⭐⭐⭐⭐⭐
   ✓ Moved by the connection across time.
   ✓ Unexpected truth.
   ✓ Ending evokes hope.

**[Improvement Suggestions]**
1. Reduce letter content by about 200 characters.
2. Add 1-2 lines describing the bookstore's space.
3. Express explanatory psychological descriptions through actions.
```

### Problem Fixing
```
User: /quality scene "Discovery of the letter" --fix
Assistant: **[Problem Fix Suggestions]**

Problem 1: Explanatory psychological description
Original:
"Misaki felt a complex mix of surprise and nostalgia."

Revised:
"Misaki's hand stopped. The familiar handwriting of 'To Misaki'
spoke to her across twenty years."

Problem 2: Bookstore layout is unclear
Additional description:
"Behind the counter, in front of the shelf lined with literary collections,
the old woman held a single book."

Problem 3: Letter is too long
Summary suggestion:
Describe only the main points of the letter and increase Misaki's reactions.
"Her mother's handwriting spelled out only what was important.
'Books connect people—'
As Misaki read on, a single tear traced down her cheek."
```

### Character Evaluation
```
User: /quality character Asuka Sato
Assistant: **[Character Consistency Evaluation: Asuka Sato]**

Overall Evaluation: Excellent (45/50 points)

✅ Strengths
1. Motivation "I want to expand people's potential by sharing knowledge" is consistent throughout
2. Catchphrase "If you'd like" is used naturally
3. Gesture of pushing up glasses is effective

⚠️ Caution
1. Scene in Chapter 5 where books are handled carelessly
   → May contradict motivation

📊 Detailed Analysis
- Motivation Consistency: 10/10
- Value Expression: 9/10
- Behavior Patterns: 8/10
- Speech Style: 9/10
- Naturalness of Growth: 9/10

**[Suggestion]**
Revise Chapter 5: Handle books carefully even when emotional.
```

## Evaluation Result Management

### Saving Quality Check Records
```
# Record evaluations per work
my-stories/[work-title]/quality-checks/
├── check-2025-06-15.md    # Dated evaluation
├── check-draft.md         # Draft stage evaluation
└── check-final.md         # Final evaluation

# Evaluation template
cp quality-check/checklist.md my-stories/[work-title]/quality-checks/check-[date].md
```

### Tracking Improvements
```markdown
## Evaluation History

### 2025-06-15 First Draft
- Overall: 35/50
- Main issue: Character consistency

### 2025-06-20 Second Draft
- Overall: 42/50
- Improvement: Character revisions complete
- Remaining issue: Deepen emotional portrayal

### 2025-06-25 Final Draft
- Overall: 46/50
- Completeness: Publishable level
```

### Comparing Works
```
# Visualize your own growth
my-stories/quality-summary.md

Work A: 35/50 → 42/50
Work B: 38/50 → 45/50
Work C: 41/50 → 47/50
```

## Improvement Action Plan

### High Priority
1. Correct actions contradicting character motivation
2. Resolve physical contradictions
3. Adjust unnatural emotional changes

### Medium Priority
1. Reduce redundant descriptions
2. Convert explanatory sentences to action descriptions
3. Effective placement of foreshadowing

### Low Priority
1. Standardize writing style
2. Adjust minor phrasing
3. Correct typos and omissions

## Common Problem Patterns

### Lost in the Middle
- Symptom: Important information is missing in the middle part
- Countermeasure: Move important information to the beginning/end

### Character Inconsistency
- Symptom: Personality changes depending on the scene
- Countermeasure: Revisit motivation and revise

### Excessive Explanation
- Symptom: Everything is explained in words
- Countermeasure: Express through actions and scenery

## Quality Improvement Cycle

```
Evaluate → Identify Problems → Create Revisions →
Implement → Re-evaluate → Fine-tune → Complete
```

## Related Commands

- `/character` - Strengthen character consistency
- `/story` - Improve story structure
- `/scene` - Rewrite scenes
- `/revise` - Comprehensive revision

## Remember

📊 Numbers are guidelines. What matters most is resonating with readers' hearts.
📊 Don't aim for perfection. 80 points is good enough for a quality work.
📊 Evaluation is for growth. Don't forget the joy of creation.