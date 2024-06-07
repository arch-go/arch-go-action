# arch-go-action

A GitHub action for integrating [arch-go](https://github.com/fdaines/arch-go) into your CI workflow.

## Usage

```yaml
steps:
  name: Perform architecture check
  uses: dadrus/arch-go-action@master
  with:
    version: v1.5.2        # optional, defaults to latest
    generate_report: true  # optional, defaults to false
    verbose: true          # optional, defaults to false
```

* `version`: The version of arch-go to use. Optional and defaults to `latest`.
* `generate_report`: Whether an HTML report should be generated. Optional and defaults to `false`. If enabled, the generated report will be available as artefact for download.
* `verbose`: Instructs arch-go to generate verbose output, which might be helpful for debugging purposes. Optional and defaults to `false`.

## License

This action is licensed under the [MIT License](https://github.com/dadrus/arch-go-action/blob/main/LICENSE).

## Contributions

Contributions are very welcome!
