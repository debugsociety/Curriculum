# Day 7: Debugging a conflict

## After turning on your classmates' features, you may have seen an error
Each person in the class created a content type with various fields. They then exported them to features, pushed them to git, and shared them with the class. Everyone turned on all of their classmates' features and - boom - your site may have crashed. What now?

## There is no magic in programming
Let's think about this - what just happened?
1. Everyone created a content type
  - no problems so far
2. Everyone added fields to their content types
  - still looking good
3. Everyone exported their content types and fields
  - no errors
4. Everyone enabled their classmates' features. AKA they turned on all of their classmates' content types and fields on
  - :( The site crashed

Okay - all looked good until step 4. My classmates' content types broke my site.

## Analyzing the problem
Turning my classmates' content types on broke the site. Let's turn them off (using drush) and see if that fixes it.
Clear the cache and... site's back!

Steps to resolve:
1. Find out which two features are incompatible
2. Using the UI, enable the first feature module
3. Using the UI, look at the second feature module
  - Does it say why the feature cannot be enabled?
    - The answer should be that the two features each provide a different field with the same machine name
