# monorepo-checkout-buildkite-plugin

## How to use?

So you have a monorepo with many projects (stored under folders). Let's see one example:

```
# you monorepo
projectA/
  bin/command1
projectB/
projectC/
```

If you want to point `BUILDKITE_CHECKOUT_PATH` to a specific folder inside your repo, this
is the plugin to do that:

```yaml
steps:
  - label: "Do something"
    commands:
      - ./bin/command1
    plugins:
      - https://github.com/runlevel5/monorepo-checkout-buildkite-plugin.git:
          folder: "projectA"
```
