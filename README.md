# Marketplace

Marketplace for Claude Code plugins

## Installing a Plugin

To add an existing marketplace plugin, follow these steps:

```
# Add the marketplace
/plugin marketplace add dojoengine/marketplace

# Install the plugin
/plugin install {plugin}@dojoengine
```

## Adding your Plugin

We welcome community plugins from the Dojo community.

Plugins are added to the marketplace by including them in `.claude-plugin/marketplace.json`.

If you have a plugin to help developers build with Dojo -- helping them understand your game's codebase, your SDK's particular patterns, or anything else, open a PR to add it.

Documentation for Claude Code plugins [can be found here](https://code.claude.com/docs/en/plugins).

## Configuring your Project with the Dojo Marketplace

If you are developing a Dojo game, you can configure your repository to automatically install and enable Dojo-related plugins.

To do this, add the following to your project's `.claude/settings.json`:

```
{
  "extraKnownMarketplaces": {
    "dojoengine": {
      "source": {
        "source": "github",
        "repo": "dojoengine/marketplace"
      }
    }
  },
  "enabledPlugins": {
    "book@dojoengine": true,
    ... other plugins as needed
  }
}
```

With this configuration, the necessary plugins will be automatically enabled when users trust your project folder.

See the full instructions [here](https://code.claude.com/docs/en/plugin-marketplaces#require-marketplaces-for-your-team).
