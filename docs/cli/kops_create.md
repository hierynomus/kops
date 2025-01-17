
<!--- This file is automatically generated by make gen-cli-docs; changes should be made in the go CLI command code (under cmd/kops) -->

## kops create

Create a resource by command line, filename or stdin.

### Synopsis

Create a resource:
  
  *  cluster
  *  instancegroup
  *  secret

 Create a cluster, instancegroup, keypair, or secret using command line parameters, YAML configuration specification files, or stdin. (Note: keypairs and secrets cannot be created from YAML config files yet).

```
kops create {-f FILENAME}... [flags]
```

### Examples

```
  # Create a cluster from the configuration specification in a YAML file.
  kops create -f my-cluster.yaml
  
  # Create secret from secret spec file.
  kops create -f secret.yaml
  
  # Create an instancegroup based on the YAML passed into stdin.
  cat instancegroup.yaml | kops create -f -
```

### Options

```
  -f, --filename strings   Filename to use to create the resource
  -h, --help               help for create
```

### Options inherited from parent commands

```
      --add_dir_header                   If true, adds the file directory to the header of the log messages
      --alsologtostderr                  log to standard error as well as files (no effect when -logtostderr=true)
      --config string                    yaml config file (default is $HOME/.kops.yaml)
      --log_backtrace_at traceLocation   when logging hits line file:N, emit a stack trace (default :0)
      --log_dir string                   If non-empty, write log files in this directory (no effect when -logtostderr=true)
      --log_file string                  If non-empty, use this log file (no effect when -logtostderr=true)
      --log_file_max_size uint           Defines the maximum size a log file can grow to (no effect when -logtostderr=true). Unit is megabytes. If the value is 0, the maximum file size is unlimited. (default 1800)
      --logtostderr                      log to standard error instead of files (default true)
      --name string                      Name of cluster. Overrides KOPS_CLUSTER_NAME environment variable
      --one_output                       If true, only write logs to their native severity level (vs also writing to each lower severity level; no effect when -logtostderr=true)
      --skip_headers                     If true, avoid header prefixes in the log messages
      --skip_log_headers                 If true, avoid headers when opening log files (no effect when -logtostderr=true)
      --state string                     Location of state storage (kops 'config' file). Overrides KOPS_STATE_STORE environment variable
      --stderrthreshold severity         logs at or above this threshold go to stderr when writing to files and stderr (no effect when -logtostderr=true or -alsologtostderr=false) (default 2)
  -v, --v Level                          number for the log level verbosity
      --vmodule moduleSpec               comma-separated list of pattern=N settings for file-filtered logging
```

### SEE ALSO

* [kops](kops.md)	 - kOps is Kubernetes Operations.
* [kops create cluster](kops_create_cluster.md)	 - Create a Kubernetes cluster.
* [kops create instancegroup](kops_create_instancegroup.md)	 - Create an instancegroup.
* [kops create keypair](kops_create_keypair.md)	 - Add a CA certificate and private key to a keyset.
* [kops create secret](kops_create_secret.md)	 - Create a secret.
* [kops create sshpublickey](kops_create_sshpublickey.md)	 - Create an SSH public key.

