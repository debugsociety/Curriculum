# Entities
Entities are the basic building blocks of data in Drupal.

I like analogies, so:
- Trees are plants.
- Flowers are plants.
All flowers are plants, but not all plants are flowers. There may be countless other types of plants, each with its own characteristics.

Is analogous to saying:
- Users are entities.
- Nodes are entities.
All users are entities, but not all entities are users. There may be countless other types of entities, each with its own characteristics (properties + fields).

## Entity types in core
### Nodes
Drupal ships with an entity type called a 'node'. Furthermore, it provides a user interface for creating types of nodes, called *'Content Types'*.

The vast majority of what you build on Drupal websites centers around building, managing, and displaying nodes.

When creating new or editing existing content types, you will be adding, editing, or removing fields.

A standard Drupal install comes with the Article content type and the Blog post content type. Every article you create is an article 'node'. Every blog post you create is a blog post 'node'.

- All articles are nodes, not all nodes are articles.
- All nodes are entities, not all entities are nodes.

### Users
The second entity type Drupal ships with is 'Users'. Users is what it sounds like - user accounts for your website.

## Properties and Fields
Data is attached to entities using both properties and fields. Building a custom entity type is not a common task, but this information brings you closer to being in control of your system's architecture.

### Fields
Fields are used to store additional information for entities.

Fields store more information than properties, are 'more expensive' to load than properties, and are not loaded for every single request which involves the entity.

Example of fields that could be attached to the 'User' entity type:
1. Address field
2. Phone number field
3. Parent company refence field

### Properties
Properties are used to store the most basic information on entities. Properties come everywhere with the entity, whether you ask for it or not.

Generally speaking:
- A property is generally text, a date, a boolean (true/false), or a number.
- Entities have no more than 1-5 properties attached to them.
- Changing what properties attach to an entity type is not easy or convenient to do.

Example of properties on the 'User' entity type:
1. User ID
2. Username
3. Signature
4. Picture
5. E-mail

### When to use which?
In general, properties are only created at the time you create a new entity type.

*When in doubt, create a field.* 99% of the time, you will only be adding or changing fields. 


		
## Fields

## Custom Entity Types

# Content Types

# Blocks
## Panes
# Features
# Views
# Panels
# Taxonomy
# 

Update core
Update modules
