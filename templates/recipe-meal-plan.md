## Recipe Meal Plan Template

When asked to create a meal plan, output a **copy/paste-ready email format**.
No YAML, frontmatter, or inline metadata.

**General Rules**
- **Plan length:** 4 days starting from the given day (default: tomorrow).
- **Date format:** `Mon 02/03` only.
- **Spacing:** One blank line between days/sections.
- **No shopping list or prep notes** unless requested.

**Meal Logic**
- **Morning:** Default Greek yogurt with fruit. Omit if unchanged.
- **Midday:** Default leftovers. Use `Leftovers — [exact Evening meal]`.
    - Use exact recipe names, no paraphrasing.
    - If previous dinner produced no leftovers (e.g., takeout), choose a new simple meal.
- **Evening:** Main cooking slot. Use links if known; otherwise use plain text.  
    Choose well-known home recipes unless I specify otherwise.

**Recipe Sources (in priority order)**
1. **Conversation history** — existing recipes, preferences, or “Next Time” list
2. **General knowledge** — common home dishes
3. **Web search / tool calls** — use only if source gaps exist or I request a specific recipe or link

**Recipe Linking**
- Link recipe names when the URL is known.
- If not found or searched, output plain text.
- Never invent URLs.

**Sections**
- **Next Time:** Include 4–6 future meal ideas.
    Carry forward unused items unless changed.

**Delivery (in order of preference)**

**Preferred:** HTML → Plain text fallback.

**HTML rules**
- Generate a standalone `.html` file with simple tags: `<h3>`, `<b>`, `<a>`, `<br>`, `<p>`.
- No CSS, classes, or styles.

**Plain text rules**
- Use ALL CAPS headers and day labels (e.g., `MON 02/03`).
- No markdown syntax.
- Place URLs in parentheses.
- One blank line between days/sections.

---
### HTML Template 

```html
<h3>Meal Plan — Week of Mon 02/03 (4 days)</h3>

<p>
<b>Mon 02/03</b><br>
Evening: <a href="https://example.com/beef-stew">Beef stew</a><br>
Midday: Ham sandwich
</p>

<p>
<b>Tue 02/04</b><br>
Evening: Chicken stir fry<br>
Midday: Leftovers — beef stew
</p>

<p>
<b>Wed 02/05</b><br>
Evening: Tacos<br>
Midday: Leftovers — chicken stir fry
</p>

<p>
<b>Thu 02/06</b><br>
Evening: <a href="https://example.com/pork-chops">Cranberry pork chops</a><br>
Midday: Leftovers — tacos
</p>

<p>
<b>Next Time</b>
</p>

● Spaghetti and meatballs<br>
● <a href="https://example.com/grilled-salmon">Grilled salmon</a><br>
● Pot roast<br>
● Loaded baked potato soup<br>
● Sheet pan fajitas<br>
```

### Plain Text Template

```text
MEAL PLAN — WEEK OF MON 02/03 (4 DAYS)

MON 02/03
Evening: Beef stew (https://example.com/beef-stew)
Midday: Ham sandwich

TUE 02/04
Evening: Chicken stir fry
Midday: Leftovers — beef stew

WED 02/05
Evening: Tacos
Midday: Leftovers — chicken stir fry

THU 02/06
Evening: Cranberry pork chops (https://example.com/pork-chops)
Midday: Leftovers — tacos

NEXT TIME
- Spaghetti and meatballs
- Grilled salmon (https://example.com/grilled-salmon)
- Pot roast
- Loaded baked potato soup
- Sheet pan fajitas
```

