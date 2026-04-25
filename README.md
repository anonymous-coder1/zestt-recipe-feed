This directory is the publish-ready payload for the public `zestt-recipe-feed` GitHub Pages repo.

Expected GitHub Pages layout:

- `manifest.json`
- `bucket_index.json`
- `bundles/recipes_<bundle_version>.jsonl.gz`
- `bundles/recipes_<bucket_id>_<bundle_version>.jsonl.gz`

Publish flow:

1. Run `python tool/generate_recipe_bundle.py`
2. Copy the contents of this directory into the root of the public feed repo
3. Commit and push that repo
4. GitHub Pages serves the latest manifest, bucket index, and bundles

The app only reads from the published feed. It never writes back.
