# Problem 3 — Weather (7 days × 3 states)

In this problem, the table represents **allowed or assigned weather states** for each day.

- Columns → days: Mon, Tue, Wed, Thu, Fri, Sat, Sun  
- Rows → weather states:
  - S — sunny
  - C — cloudy
  - R — rainy  

Marking a cell (X) means that the given state is **selected or allowed** for that day.

---

## Part A — marking events

### 1. Monday is sunny
    Mon Tue Wed Thu Fri Sat Sun
  S  X   .   .   .   .   .   .
  C  .   .   .   .   .   .   . 
  R  .   .   .   .   .   .   .    
  
---

### 2. the weekend (Saturday and Sunday) is rainy
    Mon Tue Wed Thu Fri Sat Sun
  S  .   .   .   .   .   .   .
  C  .   .   .   .   .   .   .  
  R  .   .   .   .   .   x   x             
  
---

### 3. it rains on Wednesday or Friday
    Mon Tue Wed Thu Fri Sat Sun
  S  .   .   .   .   .   .   .
  C  .   .   .   .   .   .   .  
  R  .   .   x   .   x   .   . 

---

### 4. there is no rainy day during the week
    Mon Tue Wed Thu Fri Sat Sun
  S  X   x   x   x   x   x   x
  C  x   x   x   x   x   x   x 
  R  .   .   .   .   .   .   .  

---

### 5. Thursday is not sunny
    Mon Tue Wed Thu Fri Sat Sun
  S  .   .   .   .   .   .   .
  C  .   .   .   x   .   .   .  
  R  .   .   .   x   .   .   . 
  
---

## Part B — interpretation

### Case 1
    Mon Tue Wed Thu Fri Sat Sun
S    .   .   .   .   .   X   X
C    .   .   .   .   .   .   .
R    .   .   .   .   .   .   .

**Interpretation:**

Saturday and Sunday are sunny.

---

### Case 2
    Mon Tue Wed Thu Fri Sat Sun
S    X   X   X   X   X   X   X
C    X   X   X   X   X   X   X
R    .   .   .   .   .   .   .

**Interpretation:**

There is no rainy day during the week.  
Each day is either sunny or cloudy.

---

## Final conclusion

This representation shows that:

- columns represent days,
- rows represent weather states,
- marked cells describe allowed or assigned states,
- verbal statements can be translated into structured graphical form.