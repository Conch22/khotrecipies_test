---
cssclasses: recipe-note
tags: 
meal_type: {{recipeCategory}}
author: {{author}}
cook_time: {{magicTime totalTime}}
url: {{url}}
photo: "{{photoFrontmatter image}}"
---

# [{{{name}}}]({{url}})

{{#if image}}
![{{{name}}}]({{imageLink image}})

{{/if}}

{{#if description}}
{{{description}}}

{{/if}}

> [!recipe-meta] At a Glance
{{#if recipeCategory}}> **Meal type**: {{recipeCategory}}
{{/if}}{{#if totalTime}}> **Cook time**: {{magicTime totalTime}}
{{/if}}{{#if author}}> **Author**: {{author}}
{{/if}}{{#if url}}> **Source**: [Open recipe]({{url}})
{{/if}}

### Ingredients

{{#each recipeIngredient}}
- [ ] {{{this}}}
{{/each}}

### Instructions

{{#each recipeInstructions}}
{{#if this.itemListElement}}
#### {{{this.name}}}
{{#each this.itemListElement}}
- {{{this.text}}}
{{/each}}
{{else if this.text}}
- {{{this.text}}}
{{else}}
- {{{this}}}
{{/if}}
{{/each}}

-----

## Notes
{{#if recipeNotes}}
{{#each recipeNotes}}
- {{{this}}}
{{/each}}
{{/if}}
