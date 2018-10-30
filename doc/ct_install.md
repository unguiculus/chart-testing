## ct install

Install and test a chart

### Synopsis

Run 'helm install' and ' helm test' on

* changed charts (default)
* specific charts (--charts)
* all charts (--all)

in given chart directories.

Charts may have multiple custom values files matching the glob pattern
'*-values.yaml' in a directory named 'ci' in the root of the chart's
directory. The chart is installed and tested for each of these files.
If no custom values file is present, the chart is installed and
tested with defaults.

```
ct install [flags]
```

### Options

```
      --all                       Process all charts except those explicitly excluded.
                                  Disables changed charts detection and version increment checking
      --build-id string           An optional, arbitrary identifier that is added to the name of the namespace a
                                  chart is installed into. In a CI environment, this could be the build number or
                                  the ID of a pull request. If not specified, the name of the chart is used.
      --chart-dirs strings        Directories containing Helm charts (default [charts])
      --chart-repos strings       Additional chart repos to add so dependencies can be resolved
      --charts strings            Specific charts to test.
                                  Disables changed charts detection and version increment checking
      --config string             Config file
      --excluded-charts strings   Charts that should be skipped
  -h, --help                      help for install
      --remote string             The name of the Git remote used to identify changed charts (default "origin")
      --target-branch string      The name of the target branch used to identify changed charts (default "master")
      --tiller-namespace string   The namespace of Tiller (default: kube-system) (default "kube-system")
      --timeout duration          The timeout for Helm in seconds (default: 5m) (default 5m0s)
```

### SEE ALSO

* [ct](ct.md)	 - The Helm chart testing tool

###### Auto generated by spf13/cobra on 30-Oct-2018