# Ingredient Comparison Table Template

## Purpose

Defines the format for comparing ingredients across recipes. This table is used to decide which ingredients and amounts to include in a final recipe. This is a research artifact, not a final recipe.

## Output Rules

- Deliver one complete markdown code block.
- No extra commentary or breaks between sections.

## Section Rules

1. Reviewed Recipes – Numbered list with hyperlinks
2. Ingredient Comparison – Markdown table

## Reviewed Recipes Format

```
#### Reviewed Recipes
- R1 - [Recipe Title](url)
- R2 - [Recipe Title](url)
- R3 - [Recipe Title](url)
- R4 - [Recipe Title](url)
- R5 - [Recipe Title](url)
```

## Ingredient Comparison Table Format

### Columns

| Column | Description |
| ------------ | -------------------------------------------------- |
| Ingredient | Name and preparation, if applicable |
| R1–R5 | Amount from each recipe, blank if absent |

### Row Rules

- One row per unique ingredient.
- Group by type (see below), sorted alphabetically within each.
- Use a header row for each group (name in Ingredient column only).
- Keep prep differences separate (“garlic, minced” ≠ “garlic, sliced”).

### Grouping Order

1. Proteins
2. Vegetables
3. Fruits
4. Dairy
5. Oils & Fats
6. Spices & Seasonings
7. Sauces & Condiments
8. Grains & Starches
9. Liquids
10. Other

Omit any group that has no ingredients.

### Units

Use abbreviations only in the table:

| Abbreviation | Meaning    |
| ------------ | ---------- |
| t            | teaspoon   |
| T            | tablespoon |
| c            | cup        |
| oz           | ounce      |
| lb           | pound      |
| pt           | pint       |
| qt           | quart      |
| gal          | gallon     |
| ml           | milliliter |
| L            | liter      |
| g            | gram       |
| kg           | kilogram   |

Fractions are written inline: `½t`, `¼c`, `1½c`. Do not use superscript
formatting.

If a recipe lists an ingredient without a measurement (e.g., "salt to
taste"), use `tt` (to taste). If a recipe lists a count instead of a
measurement (e.g., "2 cloves garlic"), use the count as-is: `2`.

Leave blank cells empty—no “—”, “n/a”, or “0”.

## AI Agent Instructions

#### Generating the Table

1. Extract all ingredients from each source recipes.
2. Group and sort.
3. Convert to abbreviations.
4. Output the markdown table.
5. Stop after table; await human review.

---

### Markdown Template

```markdown
## Recipe Research

### Reviewed Recipes
- R1 - [Recipe Title](url)
- R2 - [Recipe Title](url)
- R3 - [Recipe Title](url)
- R4 - [Recipe Title](url)
- R5 - [Recipe Title](url)

### Ingredient Comparison
| Ingredient              | R1   | R2   | R3   | R4   | R5   |
| ----------------------- | ---- | ---- | ---- | ---- | ---- |
| **Proteins**            |      |      |      |      |      |
| chicken breast          | 1 lb | 1 lb |      | 12oz | 1 lb |
| ground beef             |      |      | 1 lb |      |      |
| **Vegetables**          |      |      |      |      |      |
| bell pepper, diced      | 1    | 2    | 1    |      | 1    |
| onion, diced            | 1    | 1    | ½    | 1    | 1    |
| **Spices & Seasonings** |      |      |      |      |      |
| cumin                   | 1t   | ½t   |      | 1t   |      |
| garlic, minced          | 2    | 3    | 2    | 2    | 4    |
| paprika                 | 1t   | 1t   | 2t   |      | 1t   |
| salt                    | tt   | 1t   | tt   | tt   | ½t   |
| **Liquids**             |      |      |      |      |      |
| chicken broth           | 2c   | 1½c  |      | 2c   | 2c   |
```



