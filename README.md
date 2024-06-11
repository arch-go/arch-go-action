# arch-go-action

A GitHub action for integrating [arch-go](https://github.com/fdaines/arch-go) into your CI workflow.

The action expects the `arch-go.yml` file (see als [here](https://github.com/fdaines/arch-go/tree/master#file-arch-goyml)), expected by arch-go in the root of the project.

As of today, the action installs arch-go by making use of `go install ...`. To be able to do so, it installs the most recent go version as well.

## Usage

```yaml
steps:
  - name: Perform architecture check
    uses: dadrus/arch-go-action@master
    with:
      version: v1.5.2
      generate-report: true
      verbose: true
      working-directory: ./
```

* `version`: The version of arch-go to use. Optional and defaults to `latest`.
* `generate-report`: Whether an HTML report should be generated. Optional and defaults to `false`. If enabled, the generated report will be available as artefact for download.
* `verbose`: Instructs arch-go to generate verbose output, which might be helpful for debugging purposes. Optional and defaults to `false`.
* `working-directory`: Were to look for the code. Optional and defaults to `./` relative to the default working directory (`github.workspace`, `$GITHUB_WORKSPACE`)

## License

This action is licensed under the [MIT License](https://github.com/dadrus/arch-go-action/blob/main/LICENSE).

## Contributions

Contributions are very welcome!
