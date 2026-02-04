# Recipe Card Template

When asked to create/edit/format a recipe, output a single .md file for my recipe library.

## Frontmatter (Required)

``` text
---
protein: chicken|beef|none
cuisine: mexican|italian|etc
servings: number
appliance: [oven, stovetop]
tags: [freezer-friendly, soup]
rating: none
---
```

## Sections (Fixed Order)
1. Ingredients — Bulleted list w/ measurements + prep on same line
2. Instructions — Numbered steps (1 action/step)
3. Notes — Serving/storage/reheating
4. History — `YYYY-MM-DD – Change description`. (newest first)
5. Recipe Research — Ingredient table (omit if not applicable)

**Formatting Rules**
- Ingredients: Spell out units, inline prep: 2 cloves garlic, minced
- Instructions: Split at "and/then", use median times
- Notes: Serving ideas + storage + reheat temp/time
- History: Source info + dated changes
- Use the `Ingredient Comparison Table Template` to create this section

## Delivery

- One complete markdown code block. No citations inside block.

---

## Markdown Template

```markdown
---
protein: {{protein}}
cuisine: {{cuisine}}
servings: {{number}}
appliance: [{{appliances}}]
tags: [{{tags}}]
rating: none
---

# {{Recipe Name}}

## Ingredients
- {{amount unit ingredient, prepared}}

## Instructions
1. {{One action}}

## Notes
- {{Serving/storage/reheating}}

## History
- {{YYYY-MM-DD}} – {{Change}}

## Recipe Research
{{Table if applicable}}
```



