# ❌ Error Analysis

This section analyzes failure cases to understand model limitations.

---

## 🔍 Common Failure Patterns

### 1. Very Short Inputs
**Example:** "ok", "fine"

- Problem: No semantic signal
- Result: Defaults to neutral/mixed
- Fix:
  - Add fallback rules
  - Use previous state

---

### 2. Ambiguous Reflections
**Example:** "It was a weird day"

- Problem: Emotion unclear
- Result: Misclassification
- Fix:
  - Use contextual metadata more strongly

---

### 3. Conflicting Signals
**Example:**
- High stress + high energy

- Problem: Mixed cues
- Result: Inconsistent prediction
- Fix:
  - Introduce interaction features

---

### 4. Overlapping Emotional Classes
**Example:** calm vs neutral

- Problem: Similar patterns
- Result: confusion
- Fix:
  - Better class separation via embeddings

---

### 5. Noisy Labels
- Some labels may not match text
- Model learns inconsistent mapping

---

### 6. Over-reliance on Keywords
- Words like "tired" dominate prediction
- Ignores context

---

### 7. Weak Metadata Signals
- Missing or default values (-1)
- Reduces model reliability

---

### 8. Misleading Tone
**Example:** sarcastic text

- Model interprets literally

---

### 9. Low Confidence Predictions
- Model unsure but still predicts
- Handled using uncertainty_flag

---

### 10. Edge Cases
- Rare emotional states
- Underrepresented in training

---

## 🧠 Key Insights

- Text is powerful but noisy
- Metadata improves stability
- Uncertainty modeling is critical

---

## 🚀 Improvements

- Use BERT embeddings
- Add context history
- Improve label quality
- Learn decision logic instead of rules
