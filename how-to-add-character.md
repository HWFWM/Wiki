# How to Add a New Character

Adding a new character to your wiki is simple! Just follow these steps:

## 1. Create a New Markdown File

Create a new markdown file in the `_characters` folder with the format `character-name.md`. For example, `rufus-remore.md`.

## 2. Add the Front Matter

At the top of the file, add the YAML front matter with the character's details. Here's a template you can use:

```yaml
---
name: Character Name
image: character-image.jpg # Optional - upload this to assets/images/
image_credit: Artist Name # Optional
last_updated: YYYY-MM-DD

# Basic Info
aliases: [] # Optional - list of aliases/nicknames
race: ""
gender: ""
profession: ""
rank: ""
world: ""
birthplace: ""

# Physical Attributes (all optional)
physical_attributes:
  hair: 
  eyes: 
  build: 
  notable_features: 
  scars: 
  soul_crest: 

# Abilities (all optional)
abilities:
  known_essences: []
  inherent_gifts: []
  familiars: []
  titles: []

# Family (all optional)
family:
  children: []
  parents: []
  siblings: []
  grandparents: []
  close_relatives: []

# Relationships (all optional)
relationships:
  current_partners: []
  former_partners: []
  short_term_relations: []

# Affiliations (all optional)
affiliations:
  teams:
    - name: 
    - members: []
    - auxiliary_members: []
  notable_affiliations: []
  notable_allies: []
  notable_antagonists: []

# Equipment (all optional)
equipment:
  consumables: []
  weapons: []
  armor: []
  conjured: []
  growth_items: []

# Chapter Appearances (optional)
appearances:
  1: [1, 2, 3] # Book 1, chapters 1, 2, 3
  2: [4, 5, 6] # Book 2, chapters 4, 5, 6
---
```

## 3. Add the Character's Biography

After the front matter, write the character's biography using Markdown formatting. For example:

```markdown
## Biography

Character biography goes here...

### Volume One

Details about the character in Volume One...

### Volume Two

Details about the character in Volume Two...
```

## 4. Add Character Image

If you have an image for the character, add it to the `assets/images/` folder and reference it in the front matter.

## 5. Updating Chapter Appearances

As you read through the books, you can update the character's appearances by adding chapter numbers to the appearances section in the front matter.

## Expanding the Template

If you need to add a new category to all characters, follow these steps:

1. **Add to the character template**: Modify the template above to include your new category
2. **Update the character layout**: Edit `_layouts/character.html` to display the new category
3. **Add to existing characters**: Add the new category to existing character files

For example, to add a "special_abilities" section:

1. Add to the template:
```yaml
# Special Abilities (optional)
special_abilities:
  ability_name: description
```

2. Update `_layouts/character.html` by adding this section after one of the existing sections:
```html
{% if page.special_abilities %}
<div class="special-abilities card">
  <h2>Special Abilities</h2>
  <table>
    {% for ability in page.special_abilities %}
    <tr>
      <th>{{ ability[0] | capitalize }}:</th>
      <td>{{ ability[1] }}</td>
    </tr>
    {% endfor %}
  </table>
</div>
{% endif %}
```

3. Add to existing characters by updating their front matter.

This way, you can easily expand the wiki as needed while maintaining consistency across all character pages.
