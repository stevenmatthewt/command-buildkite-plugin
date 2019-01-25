# command-buildkite-plugin
A buildkite plugin to run a shell command

## Use

```yaml
# .buildkite/pipeline.yml
steps:
  - label: "Running a few commands using a plugin"
    plugins:
      stevenmatthewt/command#v0.0.1:
        run: echo "This is the first command"
      stevenmatthewt/command#v0.0.1:
        run: echo "This is the second command"
      stevenmatthewt/command#v0.0.1:
        run: echo "This is the third (and final) command"
```

The purpose of this plugin is to provide a simple way to run commands before or after other plugins. Ordinarily, when running a plugin, the `command` field is ignored and you are unable to execute a command prior to the plugin taking control. However, Buildkite does allow executing plugins, allowing this plugin to be used for this purpose.