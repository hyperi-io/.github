# Labels

`labels.yaml` is the issue label set for every repository in this organisation. hyperi-ci reads it at run time from `<owner>/.github`, path `labels/labels.yaml`, on the default branch. The path and the `schema` key are a contract, and neither moves.

- `schema` is the file format version. hyperi-ci refuses a schema it does not know.
- Change a label here, by pull request. CI parses the file and checks every issue form against it.
- New labels reach repositories when the label reconcile next runs. It creates and updates. It never deletes, and a retired label keeps its name with a `RETIRED: use ...` description.
- An organisation with no `labels/labels.yaml` gets hyperi-ci's packaged default set.
